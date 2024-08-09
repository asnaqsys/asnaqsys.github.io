---
title: "CPF2472Exception class        | QSYS API Reference Guide"
description: "The exception that is thrown when Invalid wait time specified: {0} "
last_modified_at: 2024-08-09T16:18:25Z
---

The exception that is thrown when Invalid wait time specified: {0}

**Namespace:** ASNA.QSys.Runtime.JobSupport
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception) --> [JobException](/reference/runtime/qsys-runtime-job-support/job-exception.html) --> [CPF0000Exception](/reference/runtime/qsys-runtime-job-support/cpf-exceptions/cpf0000-exception.html) --> [CPF2400Exception](/reference/runtime/qsys-runtime-job-support/cpf-exceptions/cpf2400-exception.html)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [CPF2472Exception](#cpf2472exceptiondecimal-exception)([Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception)) | Initializes a new instance of the CPF2472Exception class.

### CPF2472Exception([Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception))

Initializes a new instance of the CPF2472Exception class.

```cs
CPF2472Exception(Decimal, Exception)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | wait | The invalid wait time.
| [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception) | innerException | The exception that is the cause of the current exception, or a null reference if no inner exception is specified.
