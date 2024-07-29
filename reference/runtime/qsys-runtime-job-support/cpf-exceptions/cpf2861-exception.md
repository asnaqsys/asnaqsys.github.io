---
title: "CPF2861Exception class        | QSYS API Reference Guide"
description: "The exception that is thrown when To-file {0} in {1} not found or not created. "
last_modified_at: 2024-07-29T23:19:52Z
---

The exception that is thrown when To-file {0} in {1} not found or not created.

**Namespace:** ASNA.QSys.Runtime.JobSupport
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception) --> [JobException](/reference/runtime/qsys-runtime-job-support/job-exception.html) --> [CPF0000Exception](/reference/runtime/qsys-runtime-job-support/cpf-exceptions/cpf0000-exception.html) --> [CPF2800Exception](/reference/runtime/qsys-runtime-job-support/cpf-exceptions/cpf2800-exception.html)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [CPF2861Exception](#cpf2861exceptionstring-string-exception)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception)) | Initializes a new instance of the CPF2861Exception class.

### CPF2861Exception([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception))

Initializes a new instance of the CPF2861Exception class.

```cs
CPF2861Exception(String, String, Exception)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | library | The name of the library.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | file | The name of the file.
| [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception) | innerException | The exception that is the cause of the current exception, or a null reference if no inner exception is specified.
