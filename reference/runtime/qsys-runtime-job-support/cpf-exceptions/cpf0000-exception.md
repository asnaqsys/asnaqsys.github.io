---
title: "CPF0000Exception class        | QSYS API Reference Guide"
description: "Defines the core behavior of all the CPFxxxx exceptions. "
last_modified_at: 2024-08-09T17:25:29Z
---

Defines the core behavior of all the CPFxxxx exceptions.

**Namespace:** ASNA.QSys.Runtime.JobSupport
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception) --> [JobException](/reference/runtime/qsys-runtime-job-support/job-exception.html)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [CPF0000Exception](#cpf0000exceptionstring-exception)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception)) | Called from constructors in derived classes to initializes the CPF0000Exception class.

### CPF0000Exception([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception))

Called from constructors in derived classes to initializes the CPF0000Exception class.

```cs
CPF0000Exception(String, Exception)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | message | The exception that is the cause of the current exception, or a null reference if no inner exception is specified.
| [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception) | inner | The error message that explains the reason for the exception.
