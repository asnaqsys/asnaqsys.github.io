---
title: "InteractiveJob class          | QSYS API Reference Guide"
description: "Defines the core behavior of an interactive job. "
last_modified_at: 2024-08-09T16:18:25Z
---

Defines the core behavior of an interactive job.

**Namespace:** ASNA.QSys.Runtime.JobSupport
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [Job](/reference/runtime/qsys-runtime-job-support/job.html)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [InteractiveJob()](#interactivejob) | Called from constructors in derived classes to initialize the InteractiveJob class with a configuration from appsettings. 
| [InteractiveJob](#interactivejobjobconfig)([JobConfig](/reference/runtime/qsys-runtime-job-support/job-config.html)) | Called from constructors in derived classes to initialize the InteractiveJob class.

### InteractiveJob()

Called from constructors in derived classes to initialize the InteractiveJob class with a configuration from appsettings. 

```cs
InteractiveJob()
```

### InteractiveJob([JobConfig](/reference/runtime/qsys-runtime-job-support/job-config.html))

Called from constructors in derived classes to initialize the InteractiveJob class.

```cs
InteractiveJob(JobConfig)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [JobConfig](/reference/runtime/qsys-runtime-job-support/job-config.html) | jobConfig | The configuration values for the new interactive job.

## Properties

| Type | Name | Description
| --- | --- | --- 
| [InteractiveJob](/reference/runtime/qsys-runtime-job-support/interactive-job.html) | CurrentInteractiveJob | Gets the current web job associated with the invoking thread. |
| [WebDevice](/reference/runtime/qsys-runtime-job-support/web-device.html) | Device | Gets the device associated with the job. |
| [ExecuteState](/reference/runtime/qsys-runtime-job-support/execute-state.html) | ExecuteState | Gets the execution status of the job. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | UserDeviceID | Gets or sets the User Device Identifier associated with this Job. It is typically a combination of the Users IP address and the Browser (UA) hash. |

## Methods

| Signature | Description |
| --- | --- |
| [AcceptCommands()](#string-acceptcommands) | Set the job in a state of accepting commands sent from the UI website.
| [EndPrograms()](#void-endprograms) | Deactivates all programs in the job, closes the device and calls Dispose().
| [ExecuteStartupProgram()](#void-executestartupprogram) | When overridden in a derived class, executes the first program in the job.
| [GetJobSessionString](#string-getjobsessionstringstring-sessionid)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Gets a string with the serialized job session.
| [GetSessionValue](#string-getsessionvaluestring-sessionkey)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Get a the value of a string in the website's session.
| [InitJobSessionStore](#void-initjobsessionstorestring-sessionid)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Associate the JobSessionStore as belonging to the provided sessionId.
| [RequestShutdown()](#void-requestshutdown) | Requests an orderly shutdown of the job but it forcibly shuts it down if not completed after a time period.
| [RequestShutdown()](#void-requestshutdown) | Requests an orderly shutdown of the job but it forcibly shuts it down if not completed after a time period.
| [RequestYellowService](#string--requestyellowservicestring-command-string-parm1-string-parm2-string-parm3-string--otherparms)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Request a service to be performed by the UI website.
| [SetJobSessionString](#bool-setjobsessionstringstring-sessionid-string-jobsessionstring)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Sets the job session from a serialized string.
| [SetProgram](#void-setprogramstring-programname)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Records the name of the program that is currently running in the job.
| [SetSessionValue](#void-setsessionvaluestring-sessionkey-string-sessionvalue)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Sets the string value in the website's session.  The value may override an existing one.
| [SetUserDeviceID](#bool-setuserdeviceidstring-initialdeviceid)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Sets the UserDeviceID for the first time.
| [ShowPage](#string-showpagestring-outsidepage-string-parameter)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Display an arbitrary page to the user.
| [ShutDown()](#void-shutdown) | Forcibly shuts down the job.
| [Start](#webdevice-startstring-jobname-socket-socket-semaphoreslim-jobendedsemaphore-concurrentqueue-int-endedjobsqueue)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Socket](https://learn.microsoft.com/en-us/dotnet/api/system.net.sockets.socket?view=net-8.0), [SemaphoreSlim](https://learn.microsoft.com/en-us/dotnet/api/system.threading.semaphoreslim?view=net-8.0), [ConcurrentQueue\<Int32\>](https://learn.microsoft.com/en-us/dotnet/api/system.collections.concurrent.concurrentqueue-1?view=net-8.0)) | Starts the execution of the InteractiveJob on a newly created thread.

### string AcceptCommands()

Set the job in a state of accepting commands sent from the UI website.

```cs
string AcceptCommands()
```

### void EndPrograms()

Deactivates all programs in the job, closes the device and calls Dispose().

```cs
void EndPrograms()
```

### void ExecuteStartupProgram()

When overridden in a derived class, executes the first program in the job.

```cs
void ExecuteStartupProgram()
```

### string GetJobSessionString([string sessionID](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Gets a string with the serialized job session.

```cs
string GetJobSessionString(string sessionID)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | sessionID | The job's session id.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | A string with the serialized job session. May returns de special value *INVALIDSESSIONID.

### string GetSessionValue([string sessionKey](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Get a the value of a string in the website's session.

```cs
string GetSessionValue(string sessionKey)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | sessionKey | The key of the string value to retrieve.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The value of the string corresponding to the session key. Returns null if the key doesn't exist.

### void InitJobSessionStore([string sessionID](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Associate the JobSessionStore as belonging to the provided sessionId.

```cs
void InitJobSessionStore(string sessionID)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | sessionID | The ID of the session serving this job.

### void RequestShutdown()

Requests an orderly shutdown of the job but it forcibly shuts it down if not completed after a time period.

```cs
void RequestShutdown()
```

### void RequestShutdown()

Requests an orderly shutdown of the job but it forcibly shuts it down if not completed after a time period.

```cs
void RequestShutdown()
```

### String\[\] RequestYellowService([string command](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string parm1](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string parm2](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string parm3](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [String\[\] otherParms](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Request a service to be performed by the UI website.

```cs
String[] RequestYellowService(string command, string parm1, string parm2, string parm3, String[] otherParms)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | command | The service to be performed.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | parm1 | If any, the first parameter passed to the service.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | parm2 | If any, the second parameter passed to the service.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | parm3 | If any, the third parameter passed to the service.
| [String\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.string) | otherParms | If any, an array of other parameters to be passsed to the service.

#### Returns

| Type | Description
| --- | ---
| [String\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The result of the command.

### bool SetJobSessionString([string sessionID](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string jobSessionString](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Sets the job session from a serialized string.

```cs
bool SetJobSessionString(string sessionID, string jobSessionString)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | sessionID | The job's session id.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | jobSessionString | The serialized version of the contents of the new job session.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | True if the sessionID corresponds to the job session, otherwise false.

### void SetProgram([string programName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Records the name of the program that is currently running in the job.

```cs
void SetProgram(string programName)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | programName | The name of the current program.

### void SetSessionValue([string sessionKey](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string sessionValue](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Sets the string value in the website's session.  The value may override an existing one.

```cs
void SetSessionValue(string sessionKey, string sessionValue)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | sessionKey | The key associated with the string value to be stored.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | sessionValue | The string value to set.

### bool SetUserDeviceID([string initialDeviceID](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Sets the UserDeviceID for the first time.

```cs
bool SetUserDeviceID(string initialDeviceID)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | initialDeviceID | The initial ID.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | true if the job's UserDeviceID was null; otherwise false.

### string ShowPage([string outsidePage](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string parameter](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Display an arbitrary page to the user.

```cs
string ShowPage(string outsidePage, string parameter)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | outsidePage | Route of page to be shown.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | parameter | Parameter to be passed. Defaults to "". 

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The string set when the shown page returned.

### void ShutDown()

Forcibly shuts down the job.

```cs
void ShutDown()
```

### WebDevice Start([string jobName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [Socket socket](https://learn.microsoft.com/en-us/dotnet/api/system.net.sockets.socket?view=net-8.0), [SemaphoreSlim jobEndedSemaphore](https://learn.microsoft.com/en-us/dotnet/api/system.threading.semaphoreslim?view=net-8.0), [ConcurrentQueue\<int\> endedJobsQueue](https://learn.microsoft.com/en-us/dotnet/api/system.collections.concurrent.concurrentqueue-1?view=net-8.0))

Starts the execution of the InteractiveJob on a newly created thread.

```cs
WebDevice Start(string jobName, Socket socket, SemaphoreSlim jobEndedSemaphore, ConcurrentQueue<int> endedJobsQueue)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | jobName | The job name to be associated with this running job.
| [Socket](https://learn.microsoft.com/en-us/dotnet/api/system.net.sockets.socket?view=net-8.0) | socket | The socket used to communicate with the website providing the user interface display pages.
| [SemaphoreSlim](https://learn.microsoft.com/en-us/dotnet/api/system.threading.semaphoreslim?view=net-8.0) | jobEndedSemaphore | The semaphore to signal that the job has ended.
| [ConcurrentQueue\<Int32\>](https://learn.microsoft.com/en-us/dotnet/api/system.collections.concurrent.concurrentqueue-1?view=net-8.0) | endedJobsQueue | The queue to register the ended job.

#### Returns

| Type | Description
| --- | ---
| [WebDevice](/reference/runtime/qsys-runtime-job-support/web-device.html) | The device assigned to the job.
