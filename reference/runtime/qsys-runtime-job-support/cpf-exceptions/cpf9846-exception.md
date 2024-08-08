---
title: "CPF9846Exception class        | QSYS API Reference Guide"
description: "The exception that is thrown when Error while processing file {0} in library {1} "
last_modified_at: 2024-08-08T21:41:46Z
---

The exception that is thrown when Error while processing file {0} in library {1}

**Namespace:** ASNA.QSys.Runtime.JobSupport
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception) --> [JobException](/reference/runtime/qsys-runtime-job-support/job-exception.html) --> [CPF0000Exception](/reference/runtime/qsys-runtime-job-support/cpf-exceptions/cpf0000-exception.html) --> [CPF9800Exception](/reference/runtime/qsys-runtime-job-support/cpf-exceptions/cpf9800-exception.html)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [CPF9846Exception](#cpf9846exceptionstring-string-exception)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception)) | Initializes a new instance of the CPF9846Exception class.

### CPF9846Exception([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception))

Initializes a new instance of the CPF9846Exception class.

```cs
CPF9846Exception(String, String, Exception)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | file | The name of the file.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | library | The name of the library.
| [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception) | innerException | The exception that is the cause of the current exception, or a null reference if no inner exception is specified.
