---
title: "Yellow and Blue Protocol"
description: The TCP message format used between the website and an interactive job.
---

The website and an interactive job exchange screens over a TCP socket. [Yellow and Blue Threads](yellow-blue-threads.html) describes which threads take part. This page describes the messages on that socket.


## Framing

The same framing is implemented by the socket helpers in `ASNA.QSys.Expo.Model`, `ASNA.QSys.MonaServer`, and `ASNA.QSys.Runtime`. A connection stays open across commands. When the yellow side finishes with a socket it keeps it briefly and reuses it, and the Monarch Application Server thread blocks until the next command arrives on that connection.

Every value is big-endian.

* An `Int32` is four bytes, high byte first, with no length prefix.
* A string is an `Int32` byte count followed by that many UTF-8 bytes.
* A byte block has the same shape: an `Int32` count followed by that many bytes.

## Commands

Commands fall into two groups. **Server** commands are addressed to MonaServer itself and do not name a job. The rest are **Job** commands which name a job that is already running. Job commands are classified by what they do with that job: present a screen, read or write the job session, call the host, or shut the job down.

| Command | Mnemonic | Classification |
| --- | --- | --- |
| [Handshake](#shk-handshake) | `SHK` | Server |
| [Start New Job](#snj-start-new-job) | `SNJ` | Server |
| [Get Job List](#gjl-get-job-list) | `GJL` | Server |
| [Stop MonaServer](#sms-stop-monaserver) | `SMS` | Server |
| [Feed Job Data](#fjd-feed-job-data) | `FJD` | Screen |
| [Get Current Display File](#gcd-get-current-display-file) | `GCD` | Screen |
| [Get Job Session](#gjs-get-job-session) | `GJS` | Job session |
| [Set Job Session](#sjs-set-job-session) | `SJS` | Job session |
| [Call Host Program](#chp-call-host-program) | `CHP` | Host service |
| [Get Host File](#ghf-get-host-file) | `GHF` | Host service |
| [Request Job Shutdown](#rjs-request-job-shutdown) | `RJS` | Shutdown |

The first value of a request is a command string. MonaServer reads that string and dispatches it.

Server commands carry the fields defined for that command. Job commands share a header:

1. The command string.
2. The RPC version string `1.1`.
3. The job number, as a string.
4. A parameter string. Several commands pack multiple fields into this string, separated by commas.

The reply is written on the same connection. `GCD`, `GJS`, and `SJS` are answered by the MonaServer connection thread. `FJD`, `CHP`, and `GHF` wake the blue thread, and the blue thread writes the reply.

## Server Commands

Server commands are addressed to MonaServer itself and do not name a job. The website sends `SHK` and `SNJ` but it does not send `GJL` or `SMS` as these are intended for administration type utilities.

### SHK, handshake

Sent once before the first `SNJ`. The yellow side writes:

1. `SHK`
2. RPC version `1.0`
3. The yellow protocol version, `1.0.0.0`

The server answers with its protocol version string, `1.0.0.0`, and an `Int32` status. `1` means compatible and `2` means incompatible. The current server always answers compatible.

### SNJ, start new job

The yellow side writes:

1. `SNJ`
2. RPC version `1.1`
3. The ASP.NET session id
4. A description of the browser
5. A description of the web server
6. The device serial
7. The entry point, `assemblyPath,class,jobName`

The server answers with an `Int32` job number. The job number `-1` is followed by `*AbEnd`, the exception message, and the stack. On success the blue thread is started with this socket, and the next message the yellow side reads on it is the first [screen message](#screen-message).

### GJL, get job list

`GJL` lists the jobs MonaServer is hosting. The yellow path in the website does not send it.

### SMS, stop MonaServer

`SMS` tells MonaServer to stop listening and to request shutdown of the jobs it hosts. The yellow path in the website does not send it.

## Screen Commands

Screen commands name a running job and carry a display file between the yellow thread and that job. Both are answered with a [screen message](#screen-message).

### FJD, feed job data

This is the message that resumes a program blocked in a workstation read. The parameter string has six comma-separated fields:

1. Attention key (AID)
2. Cursor position
3. Field name
4. Subfile cursor RRN
5. Lowest subfile RRN
6. Active window cursor

After the header, the yellow side writes one byte block: the changed rows of the display-file `DataSet`, as a DiffGram. The connection thread copies those rows onto the workstation file and signals the blue thread. The blue thread's reply is the next screen, on this same socket.

If the job or its active display file cannot be found, the server writes a raw `Int32` instead of a screen: `1` when there is no job, `2` when there is no active display file.

### GCD, get current display file

The parameter string is empty. The connection thread answers at once with a screen message, read from the display file the job is already presenting. The blue thread stays in display-wait. A browser reload of an existing job uses this command.

## Job session Commands

Job session commands read or write the serialized state stored for the job, keyed by the ASP.NET session id.

### GJS, get job session

`GJS` carries the ASP.NET session id in the parameter string. The server returns the serialized job-session string.

### SJS, set job session

`SJS` carries the session id in the parameter string, then the serialized job-session string. Success is an empty string in reply.

## Host service Commands

Host service commands ask the blue thread to call a program or read a file on the host. The connection thread records the request on the display file and wakes the blue thread, which writes the reply.

### CHP, call host program

The parameter string is `hostFilePath,programName` followed by the program arguments, still comma-separated. The blue thread replies with an `Int32` host status, a result string, and a byte block.

### GHF, get host file

The parameter string is the host file path. The yellow side reads an `Int32` status, a string, and the file bytes.

## Shutdown Commands

### RJS, request job shutdown

The header is followed by a parameter string. The server calls `RequestShutdown` on the job, which wakes the blue thread so the job can unwind. This command has no reply payload.

## Screen message

A screen message is the display-file payload carried back to the yellow side. It is the reply to `SNJ`, a Server command, and to `FJD` and `GCD`, the Screen commands, so it is not part of a single command classification.

The message is a string, then a byte block.

* A page name, then the visible records of the display-file `DataSet` written with its XML schema. A record format that is on screen is included. A subfile is included together with the controller that owns it. The `DataSet` extended property `lastformatname` is the last format the program wrote.
* `*AbEnd`, then the message string and the stack string. The yellow side renders the abnormal-end page.
* `*DeviceClosed` when the job closes the device. The yellow side treats that as end of job.
* `ExpiredSession`, which the yellow side handles like an abnormal end.

The `DataSet` is written into a memory buffer and that buffer is sent, so the byte count can be larger than the XML document. The reader parses the XML and ignores the unused trailing bytes.
