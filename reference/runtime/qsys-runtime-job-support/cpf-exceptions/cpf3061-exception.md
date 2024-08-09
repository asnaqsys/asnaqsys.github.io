---
title: "CPF3061Exception class        | QSYS API Reference Guide"
description: "The exception that is thrown when Record format {0} not found for outfile {1}. "
last_modified_at: 2024-08-09T17:25:29Z
---

The exception that is thrown when Record format {0} not found for outfile {1}.

**Namespace:** ASNA.QSys.Runtime.JobSupport
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception) --> [JobException](/reference/runtime/qsys-runtime-job-support/job-exception.html) --> [CPF0000Exception](/reference/runtime/qsys-runtime-job-support/cpf-exceptions/cpf0000-exception.html) --> [CPF3000Exception](/reference/runtime/qsys-runtime-job-support/cpf-exceptions/cpf3000-exception.html)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [CPF3061Exception](#cpf3061exceptionstring-string-exception)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception)) | Initializes a new instance of the CPF3061Exception class.

### CPF3061Exception([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception))

Initializes a new instance of the CPF3061Exception class.

```cs
CPF3061Exception(String, String, Exception)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | recordFormat | The name of the format not found.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | fileName | The file name.
| [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception) | innerException | The exception that is the cause of the current exception, or a null reference if no inner exception is specified.
