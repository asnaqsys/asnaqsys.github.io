---
title: "CPF3429Exception class        | QSYS API Reference Guide"
description: "The exception that is thrown when File {0} number {1} cannot be displayed, copied or sent. "
last_modified_at: 2024-08-09T16:18:25Z
---

The exception that is thrown when File {0} number {1} cannot be displayed, copied or sent.

**Namespace:** ASNA.QSys.Runtime.JobSupport
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception) --> [JobException](/reference/runtime/qsys-runtime-job-support/job-exception.html) --> [CPF0000Exception](/reference/runtime/qsys-runtime-job-support/cpf-exceptions/cpf0000-exception.html) --> [CPF3400Exception](/reference/runtime/qsys-runtime-job-support/cpf-exceptions/cpf3400-exception.html)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [CPF3429Exception](#cpf3429exceptionstring-int32-exception)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception)) | Initializes a new instance of the CPF3429Exception class.

### CPF3429Exception([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception))

Initializes a new instance of the CPF3429Exception class.

```cs
CPF3429Exception(String, Int32, Exception)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | file | The name of the file.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | number | The spool file number.
| [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception) | innerException | The exception that is the cause of the current exception, or a null reference if no inner exception is specified.
