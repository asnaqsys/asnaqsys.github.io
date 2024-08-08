---
title: "CPF3492Exception class        | QSYS API Reference Guide"
description: "The exception that is thrown when Not authorized to spooled file {0} "
last_modified_at: 2024-08-08T21:41:46Z
---

The exception that is thrown when Not authorized to spooled file {0}

**Namespace:** ASNA.QSys.Runtime.JobSupport
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception) --> [JobException](/reference/runtime/qsys-runtime-job-support/job-exception.html) --> [CPF0000Exception](/reference/runtime/qsys-runtime-job-support/cpf-exceptions/cpf0000-exception.html) --> [CPF3400Exception](/reference/runtime/qsys-runtime-job-support/cpf-exceptions/cpf3400-exception.html)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [CPF3492Exception](#cpf3492exceptionstring-exception)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception)) | Initializes a new instance of the CPF3492Exception class.

### CPF3492Exception([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception))

Initializes a new instance of the CPF3492Exception class.

```cs
CPF3492Exception(String, Exception)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | filePath | The unathorized spooled file path.
| [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception) | innerException | The exception that is the cause of the current exception, or a null reference if no inner exception is specified.
