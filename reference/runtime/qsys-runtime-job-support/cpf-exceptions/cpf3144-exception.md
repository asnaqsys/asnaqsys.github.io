---
title: "CPF3144Exception class        | QSYS API Reference Guide"
description: "The exception that is thrown when Member {0} not cleared or initialized. "
last_modified_at: 2024-08-09T16:18:25Z
---

The exception that is thrown when Member {0} not cleared or initialized.

**Namespace:** ASNA.QSys.Runtime.JobSupport
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception) --> [JobException](/reference/runtime/qsys-runtime-job-support/job-exception.html) --> [CPF0000Exception](/reference/runtime/qsys-runtime-job-support/cpf-exceptions/cpf0000-exception.html) --> [CPF3100Exception](/reference/runtime/qsys-runtime-job-support/cpf-exceptions/cpf3100-exception.html)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [CPF3144Exception](#cpf3144exceptionstring-exception)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception)) | Initializes a new instance of the CPF3144Exception class.

### CPF3144Exception([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception))

Initializes a new instance of the CPF3144Exception class.

```cs
CPF3144Exception(String, Exception)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | member | The name of the member.
| [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception) | innerException | The exception that is the cause of the current exception, or a null reference if no inner exception is specified.
