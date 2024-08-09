---
title: "CPF3303Exception class        | QSYS API Reference Guide"
description: "The exception that is thrown when File &#39;{0}&#39; not found in job &#39;{1}/{2}/{3}&#39; "
last_modified_at: 2024-08-09T16:18:25Z
---

The exception that is thrown when File '{0}' not found in job '{1}/{2}/{3}'

**Namespace:** ASNA.QSys.Runtime.JobSupport
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception) --> [JobException](/reference/runtime/qsys-runtime-job-support/job-exception.html) --> [CPF0000Exception](/reference/runtime/qsys-runtime-job-support/cpf-exceptions/cpf0000-exception.html) --> [CPF3300Exception](/reference/runtime/qsys-runtime-job-support/cpf-exceptions/cpf3300-exception.html)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [CPF3303Exception](#cpf3303exceptionstring-string-string-string-exception)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception)) | Initializes a new instance of the CPF3303Exception class.

### CPF3303Exception([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception))

Initializes a new instance of the CPF3303Exception class.

```cs
CPF3303Exception(String, String, String, String, Exception)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | spoolFile | Name of the spool file not found.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | jobName | Job name where spooled file was searched and not found.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | jobNumber | Job number where spooled file was searched and not found.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | jobUser | Job user name where spooled file was searched and not found.
| [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception) | innerException | The exception that is the cause of the current exception, or a null reference if no inner exception is specified.
