---
title: "CPF2151Exception class        | QSYS API Reference Guide"
description: "The exception that is thrown when Operation failed for {1} in {0} type{2} "
last_modified_at: 2024-08-08T21:41:46Z
---

The exception that is thrown when Operation failed for {1} in {0} type{2}

**Namespace:** ASNA.QSys.Runtime.JobSupport
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception) --> [JobException](/reference/runtime/qsys-runtime-job-support/job-exception.html) --> [CPF0000Exception](/reference/runtime/qsys-runtime-job-support/cpf-exceptions/cpf0000-exception.html) --> [CPF2100Exception](/reference/runtime/qsys-runtime-job-support/cpf-exceptions/cpf2100-exception.html)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [CPF2151Exception](#cpf2151exceptionstring-string-string-exception)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception)) | Initializes a new instance of the CPF2151Exception class.

### CPF2151Exception([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception))

Initializes a new instance of the CPF2151Exception class.

```cs
CPF2151Exception(String, String, String, Exception)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | folder | The name of the folder (or library).
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | obj | The name of the object.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | type | The type of object.
| [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception) | innerException | The exception that is the cause of the current exception, or a null reference if no inner exception is specified.
