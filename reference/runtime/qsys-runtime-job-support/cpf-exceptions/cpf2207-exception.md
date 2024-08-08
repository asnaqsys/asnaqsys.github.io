---
title: "CPF2207Exception class        | QSYS API Reference Guide"
description: "The exception that is thrown when Not authorized to use object {0} type {1} "
last_modified_at: 2024-08-08T21:41:46Z
---

The exception that is thrown when Not authorized to use object {0} type {1}

**Namespace:** ASNA.QSys.Runtime.JobSupport
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception) --> [JobException](/reference/runtime/qsys-runtime-job-support/job-exception.html) --> [CPF0000Exception](/reference/runtime/qsys-runtime-job-support/cpf-exceptions/cpf0000-exception.html) --> [CPF2200Exception](/reference/runtime/qsys-runtime-job-support/cpf-exceptions/cpf2200-exception.html)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [CPF2207Exception](#cpf2207exceptionstring-string-exception)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception)) | Initializes a new instance of the CPF2207Exception class.

### CPF2207Exception([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception))

Initializes a new instance of the CPF2207Exception class.

```cs
CPF2207Exception(String, String, Exception)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | objectName | The unauthorized object name.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | objectType | The unauthorized object type.
| [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception) | innerException | The exception that is the cause of the current exception, or a null reference if no inner exception is specified.
