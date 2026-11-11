---
title: "Yellow and Blue Threads"
description: How the ASP.NET request thread and the interactive job thread cooperate across one user interaction.
---

An interactive Monarch application is served by two kinds of threads. The procedural program runs on a thread that lives for the whole job. Each browser request runs on a thread that ASP.NET lends for that request only. Monarch calls the job thread the **blue thread** and the request thread the **yellow thread**.

The [program user interface](program-user-interface.html) describes what those threads exchange: a workstation file on the blue side and a Razor Display Page on the yellow side, with a `DataSet` crossing between them. The [application architecture](application-architecture.html) describes where the job is hosted. This page describes how the two threads take turns.

## The blue thread

Starting a job sends a *start new job* request to the [Monarch Application Server](application-architecture.html#monarch-application-server). The server builds the interactive job and calls `InteractiveJob.Start`, which creates a new thread, names it `Job:` followed by the job name, and starts it.

That thread runs `ExecuteStartupProgram` and then whatever programs the startup program calls. The call stack, activation groups, open files, library list, and local data area all live on this thread. There is one blue thread per interactive job, and it stays alive until the job ends.

The blue thread runs the procedural code only until the program reads a workstation record and no input row is waiting. At that point it writes the current screen to the website and blocks. Its execution status becomes display-wait. The program is suspended inside the read, with its stack intact, until the website delivers the user's input.

## The yellow thread

ASP.NET Core assigns a thread-pool thread to each browser request and takes it back when the response has been written. `YellowPageModel`, the base of a migrated Razor page, runs on that thread. Monarch calls it the yellow thread.

A yellow thread does four things, then it is gone:

1. It accepts the GET or POST and binds the posted fields into the page model.
2. It sends that input to the job, or starts the job when this session does not have one yet.
3. It waits until the blue thread produces the next screen.
4. It turns that screen into HTML, or into a redirect when the program wrote a different display file, and completes the HTTP response.

The next click is a different yellow thread. Nothing about the program is stored on the yellow thread. The job handle in the ASP.NET session is what connects a new yellow thread to the blue thread that is still waiting.

## How a screen round-trip works

The website and the job talk over a TCP socket. The messages on that socket are described in [Yellow and Blue Protocol](yellow-blue-protocol.html). That remains true when the application server runs inside the website process. `HostName` `*InProcess` tells site startup to start MonaServer on a background thread in that process and to connect to it through the loopback address. `*LoopBack` and a remote host name are the same conversation with a different peer. See [In-Process and Out-of-Process](application-architecture.html#in-process).

The socket is accepted by a MonaServer connection thread. That thread is neither the yellow thread nor the blue thread. It reads the request, finds the job, and wakes the blue thread. The yellow thread spends its wait blocked on a socket read, waiting for the screen the blue thread will write.

### The first request

1. The yellow thread for the first GET finds no job for the session.
2. It connects to MonaServer and asks it to start a job, passing the ASP.NET session id and the job's entry point.
3. MonaServer creates the blue thread and returns the job number. The yellow thread stores that job number in the session and then waits on the socket.
4. The blue thread runs from the startup program until the first workstation read. It writes the page name and the visible records of the display-file `DataSet`, then blocks in display-wait.
5. The yellow thread's read completes. It loads the page model from the `DataSet`, the Razor view renders the HTML, and ASP.NET reclaims the yellow thread.

### A later request

1. A new yellow thread receives the POST. It copies the posted model into the display-file `DataSet`, including the attention key, the cursor, and the changed rows.
2. It sends that input to MonaServer and waits on the socket again.
3. The connection thread locates the job, copies the input onto the workstation file the program is reading, and signals that data is ready for the program.
4. The blue thread resumes at the read, runs until the next read that needs the user, and writes the next screen on the socket.
5. The yellow thread receives that screen and finishes the response.

While the yellow thread is waiting, the blue thread is either still in display-wait or running the next stretch of procedural code. The two threads overlap only for the duration of the request. After the response is sent, only the blue thread remains, parked inside its read.

If the program writes a different workstation file, the yellow thread answers the browser with a redirect. The browser's following GET is another yellow thread. That thread asks MonaServer for the job's current display file and renders the new page.

Some blue-thread requests never become a browser page. A prompt such as reading or writing a session value is answered by the same yellow thread, which then waits again for a real screen. The browser is contacted only when the blue thread has produced a display file for the user.

## When the job ends

A normal end closes the device. The yellow thread that is waiting sees the device close, and the response navigates to the end-of-job page. The blue thread leaves `Execute`, and MonaServer removes the job from its job table.

An exception on the blue thread is written to the socket as an abnormal end, with the message and the stack. The waiting yellow thread renders the abnormal-end page.

If the user stops sending requests, the blue thread stays in display-wait. MonaServer's idle timer calls `RequestShutdown` on jobs that have been idle longer than the configured timeout. That wakes the blue thread so it can unwind instead of waiting forever. The timeout is the `JobIdleTimeout` value in the MonaServer settings, in minutes.

## What each thread is responsible for

| | Blue thread | Yellow thread |
| --- | --- | --- |
| Created by | `InteractiveJob.Start` when MonaServer starts the job | The ASP.NET Core thread pool, for one request |
| Lifetime | The whole interactive job | The GET or POST that is in flight |
| Runs | The procedural program and its call stack | `YellowPageModel` and the Razor view |
| Waits in | The workstation read, in display-wait | A socket read for the next screen |
| Keeps | Activations, open files, library list, local data area | Nothing after the response is sent |
| Hands off through | The screen `DataSet` written to the socket | The posted input `DataSet` sent to MonaServer |
