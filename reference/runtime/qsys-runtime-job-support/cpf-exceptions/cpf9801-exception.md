---
title: "CPF9801Exception class        | QSYS API Reference Guide"
description: "The exception that is thrown when Object {0} in library {1} not found. "
last_modified_at: 2024-08-09T17:25:29Z
---

The exception that is thrown when Object {0} in library {1} not found.

**Namespace:** ASNA.QSys.Runtime.JobSupport
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception) --> [JobException](/reference/runtime/qsys-runtime-job-support/job-exception.html) --> [CPF0000Exception](/reference/runtime/qsys-runtime-job-support/cpf-exceptions/cpf0000-exception.html) --> [CPF9800Exception](/reference/runtime/qsys-runtime-job-support/cpf-exceptions/cpf9800-exception.html)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [CPF9801Exception](#cpf9801exceptionstring-string-exception)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception)) | Initializes a new instance of the CPF9801Exception class.

### CPF9801Exception([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception))

Initializes a new instance of the CPF9801Exception class.

```cs
CPF9801Exception(String, String, Exception)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | folder | The name of the folder (or library) where object was searched.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | nameobject | The name of the object not found.
| [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception) | innerException | The exception that is the cause of the current exception, or a null reference if no inner exception is specified.
