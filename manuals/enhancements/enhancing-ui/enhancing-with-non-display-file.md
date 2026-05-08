---
title: "Enhancing Applications using Non-Display File Pages"
description: "Discover how to use non-display files to enhance your applications, improving data handling and user experience."
---

## The Job

Monarch-based programs execute within the context of a Monarch Job and conform to certain conventions allowing the program to be the target of a *CALL* operation. The Job provides a program with a connection to the database, with a set of _global_ variables shared amongst all the programs in the Job (the LDA and the LDC), and with a mechanism to support instantiation based on activation groups, which is particularly important in supporting the call commands.

A Job also provides an interactive program with the infrastructure supporting the program's Workstation file. Refer to [Program User Interface](/concepts/architecture/program-user-interface.html) for a description of the interaction of the website with a Job and its Programs.

Each Job and its programs run in a dedicated thread separate from where the website executes.  This thread is known in Monarch as the **Blue Thread**, and Razor Pages run in a worker thread of the website which Monarch calls the **Yellow Thread**.

## Job States

A Job may be in anyone of these general *states*:

*   **A**. Just created
*   **B**. Executing a Program
*   **C**. Waiting for input from the user

After a Job has been created, it is in state **A (Just created)** and transitions to state **B (Executing a Program)** when the `Job.Start()` method is executed and it calls the first program. 

As long as one of the Job's programs is executing code it remains in  state **B (Executing a Program)** until one of the program tries to interact with the user by executing a `READ` or `EXFMT` operation on a Workstation format in which case the Job goes into state **C (Waiting for input from the user)**. When the user responds to the UI, then the program continues execution and the job goes back to state **B (Executing a Program)**.

The process described above is the normal sequence of execution for most jobs. There is an alternative workflow for a job in which the job waits for some external command to request a particular program to be executed.  The external command is normally sent from a *regular* page of the website, for example from a menu page.

In order to invoke a program from within the model of a non-displayfile page, it is necessary to have a Job provide the context where the program will execute. This Job should be in a state able to accept requests to execute arbitrary programs outside of the normal calling graph created by program calls.

### Accepting Commands
The cooperation of the Job is essential so a program within the Job, or the job itself, must make the Job enter a new state:

*   **D**. Accepting Commands

In this state, the Job can accept commands. To enter this state execute either the `InteractiveJob.AcceptCommands()` or the `InteractiveJob.ShowPage()` method.

While the job is in state **D (Accepting Commands)**, a website page can use the methods in the class `ASNA.QSys.Expo.Model.Command` to invoke programs in the job; the Command class also provides methods to interact with the LDA and the LDC and to let the job know to transition back from state **D (Accepting Commands)** to state **B (Executing a Program)**.

### Facilities Summary


|  | Enter Command Mode <br/> Blue Thread | Exit Command Mode <br/> Yellow Thread | Execute Commands <br/> Yellow Thread |
| -------- | ------------------ | ----------------- | -------------------|
| **Description** | Prepares a job to accept commands | Returns a Job to procedural processing | Allows code in website to invoke a function within a Job, particularly program calls.
| **Class** | [Runtime.InteractiveJob](/runtime/qsys-runtime-job-support/interactive-job.html) | [Expo.Model.Command](/reference/expo/qsys-expo-model/command.html) | [Expo.Model.Command](/reference/expo/qsys-expo-model/command.html)
| **Methods** | [ShowPage](/reference/runtime/qsys-runtime-job-support/interactive-job.html#string-showpagestring-outsidepage-string-parameter) <br/> [AcceptCommands](/reference/runtime/qsys-runtime-job-support/interactive-job.html#string-acceptcommands) | [Return](/reference/runtime/qsys-runtime/return.html) |  ["CALL"](/reference/runtime/qsys-runtime/call.html) <br/>["SETLDAFIELD"](/reference/runtime/qsys-runtime-job-support/job.html#void-setldafieldint-start-int-length-string-newvalue) <br/> ["GETLDAFIELD"](/reference/runtime/qsys-runtime-job-support/job.html#string-getldafieldint-start-int-length) <br/>                     "INVQCMDEXC" <br/> "GETLDAFIELD"<br/>"SETLDAFIELD" <br/> "GETLDCOBJECT" <br/>                     "SETLDCOBJECT": <br/> "RMVLDCOBJECT" <br/> "RQSSHTDOWN" <br/> "RETURN" <br/> 

## A Word About Session Values
Before getting into how to enter command mode and call programs from the yellow thread into the blue thread, we have to discuss the use of the ASP.NET Core [Session](//learn.microsoft.com/en-us/aspnet/core/fundamentals/app-state) object.

ASP.NET Core maintains session state by providing a cookie to the client (the browser) that contains a Session ID. Cookies are not share between different browsers (say Chrome and Edge), but they are share amongst all the Tabs and instances of a particular browser. The effect of the sharing of the Session ID cookie is the sharing of the Session object between all the browser instances and Tabs.

If you have configured your application to [run multiple jobs](/manuals/configuration/multiple-jobs-one-browser.html) from a single browser, you will have to take special care to not use Session values.

If your web pages needs to keep data on a per job basis, use the [JobSession](/reference/expo/qsys-expo-model/job-session.html) facilities provided via the [Command.JobSession](/reference/expo/qsys-expo-model/command.html#properties) property.

## Enter Command Mode (Blue thread)

### ShowPage and AcceptCommands

The ShowPage and AcceptCommands commands prepare a job to accept commands. 

```cs

    public string ShowPage(string outsidePage, string parameter);

    public string AcceptCommands(string parameter);
```            

`ShowPage` receives a URL or one of the websites non-displayfile pages route and sends a request to the webserver to redirect the browser to the passed URL or page.  After that, `ShowPage` enters the same serving cycle used by `AcceptCommands`.

`AcceptCommands` enters a cycle of serving commands sent by the yellow thread, the serving cycle ends when a `Return` command is received and control passes back to the program that invoked `AcceptCommnads`. The `Return` method has a string parameter which is made available to the blue thread as the returned value of `AcceptCommands` and `ShowPage`.

Both of these methods accept a single string parameter; the parameter will be stored in the JobSession object where the website page can retrieve it.  Using the Monarch [JobSession](/reference/expo/qsys-expo-model/job-session.html) class, the string parameter can be retrieved via the `CommandParm` property like this:

```cs
    var command = Command.GetCommandFromRequest(HttpContext);
    ...
    string parmeters = command.JobSession.CommandParm;
    command.JobSession.CommandParm = string.Empty;
```
## Execute Commands (Yellow thread)

Once a Job is accepting commands, the website can send requests for the job to execute.  The request are manipulations of the LDC and the LDA, calls to programs, requesting a shutdown of the job, and finally returning to normal procedural execution of programs.

### Call Command
`Call` can invoke both kinds of programs: interactive and non-interactive. Programs receive parameters by reference, i.e. Page models can send and receive data to/from the called programs; the arguments are stored in an array of strings. The called program can define its parameter list only using fields of type character and decimal (zoned, packed, binary, and decimal).

```cs
    public void Call(string assemblyName, string programName, string[] args)
```

Interactive calls **require** a callback Page route where control will be relinquished once the called program finish execution. Calling interactive programs effectively means a transfer of control, first to the interactive program being called, and then to the callback Page. Calls that invoke interactive programs can send data into the program via parameters but there output parameter list will be sent to the callback page by storing the array in the `Command.JobSession.CommandParm` property in the form of a multiple line string with each parameter in a separate line.

```cs
    public void Call(string assemblyName, string programName, string[] parms string callbackPage)
```

### CallSilent Command

`CallSilent` invokes an interactive program from a non-display file Razor Page (yellow thread) but prevents the display of the program's display file to the browser.

```cs
    public WebDisplayFileProxy CallSilent( string assemblyPath, string programName, string[] parms )
```
When the interactive program performs an `EXFMT` (or `READ`), it will wait for input but will not display a page, instead, `CallSilent` will return the WebDisplayFileProxy object allowing the caller to inspect the dataset containing the data tables of the record formats written by the interactive program on the blue thread.

The caller of `CallSilent` is responsible for feeding input to the waiting interactive program. This is done by updating the appropriate rows of the data tables of the WebDisplayFileProxy and then executing the method `PushKeyFocus`.

### PushKeyFocus Command

`PushKeyFocus` is invoked from the yellow thread to provide input to the blue thread program waiting for input. It sets the parameter values and returns a WebDisplayFile with the focus set as dictated by the parameters.

```cs
    public Expo.Model.WebDisplayFile PushKeyFocus(
    Expo.Model.AidKey key, short virtualRowCol, string fieldName)
```

This method does not affect the indicators that would normally be set/reset if the display file would have gone to the browser. In particular, no numeric indicator will be set based on the key "pressed". The waiting program must base its actions on the feedback AID or the `IN_xx_` indicators.


## Exit Command Mode (Yellow Thread)

### Return Command

Returns a Job to procedural processing thus exiting command mode.

```cs
public void Return(string result)
```

When a Razor Page wants to return the Job to the **B (Executing a Program)** state to continue its procedural processing, it invokes this command, passing a string back to the original code in the blue thread that prepared the job to accept commands. The string parameter is made available to the blue thread as the returned value of `AcceptCommands` and `ShowPage`.

## See Also

* [Calling a Program from a Non-DisplayFile Page](/manuals/enhancements/enhancing-ui/calling-program-from-non-displayfile-page.html)
* [Showing a Non-DisplayFile Page](/manuals/enhancements/enhancing-ui/enhancing-with-non-display-file.html)
* [Command Class](/reference/expo/qsys-expo-model/command.html)
* [Interactive Job Class](/reference/runtime/qsys-runtime-job-support/interactive-job.html)
* [LocalDataCollection Class](/reference/runtime/qsys-runtime-job-support/local-data-collection.html)



