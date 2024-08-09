---
title: "CPF3340Exception class        | QSYS API Reference Guide"
description: "The exception that is thrown when *ONLY specified, but more than one file with specified name &#39;{0}&#39; found in job &#39;{1}/{2}/{3}&#39; "
last_modified_at: 2024-08-09T16:18:25Z
---

The exception that is thrown when *ONLY specified, but more than one file with specified name '{0}' found in job '{1}/{2}/{3}'

**Namespace:** ASNA.QSys.Runtime.JobSupport
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception) --> [JobException](/reference/runtime/qsys-runtime-job-support/job-exception.html) --> [CPF0000Exception](/reference/runtime/qsys-runtime-job-support/cpf-exceptions/cpf0000-exception.html) --> [CPF3300Exception](/reference/runtime/qsys-runtime-job-support/cpf-exceptions/cpf3300-exception.html)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [CPF3340Exception](#cpf3340exceptionstring-string-string-string-exception)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception)) | Initializes a new instance of the CPF3340Exception class.

### CPF3340Exception([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception))

Initializes a new instance of the CPF3340Exception class.

```cs
CPF3340Exception(String, String, String, String, Exception)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | spoolFile | Name of the spool file not found.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | jobName | Job name where spooled file was searched and more than one found.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | jobNumber | Job number where spooled file was searched and more than one found.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | jobUser | Job user name where spooled file was searched and more than one found.
| [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception) | innerException | The exception that is the cause of the current exception, or a null reference if no inner exception is specified.
