---
title: "OSExecute class               | QSYS API Reference Guide"
description: "This class contains methods to start an external process. "
last_modified_at: 2024-08-09T16:18:25Z
---

This class contains methods to start an external process.

**Namespace:** ASNA.QSys.Runtime
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>

## Methods

| Signature | Description |
| --- | --- |
| [Run](#void-runstring-commandline-string-directory-string-operationstring-processwindowstyle-windowstyle-bool-wait)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [ProcessWindowStyle](https://learn.microsoft.com/en-us/dotnet/api/system.diagnostics.processwindowstyle?view=net-8.0), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Starts an external process using the arguments to construct a System.Diagnostics.ProcessStartInfo object and direct how the process is started.

### void Run([string commandLine](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string directory](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string operationString](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [ProcessWindowStyle windowStyle](https://learn.microsoft.com/en-us/dotnet/api/system.diagnostics.processwindowstyle?view=net-8.0), [bool wait](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Starts an external process using the arguments to construct a System.Diagnostics.ProcessStartInfo object and direct how the process is started.

```cs
void Run(string commandLine, string directory, string operationString, ProcessWindowStyle windowStyle, bool wait)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | commandLine | The command line to launch. It may be the name of a file that the system will open in the corresponding default application,            or it can be an application with its arguments.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | directory | The working directory for the new process.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | operationString | This corresponds to System.Diagnostics.ProcessStartInfo.Verb, which is the action to take when opening the indicated document or application.
| [ProcessWindowStyle](https://learn.microsoft.com/en-us/dotnet/api/system.diagnostics.processwindowstyle?view=net-8.0) | windowStyle | The ProcessWindowStyle value that selects the window style of the new process.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | wait | Indicates whether to wait for the process to finish.
