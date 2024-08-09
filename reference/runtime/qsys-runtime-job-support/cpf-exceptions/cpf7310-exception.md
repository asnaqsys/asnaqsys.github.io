---
title: "CPF7310Exception class        | QSYS API Reference Guide"
description: "The exception that is thrown when Member {0} not removed from file {1} in {2} "
last_modified_at: 2024-08-09T17:25:29Z
---

The exception that is thrown when Member {0} not removed from file {1} in {2}

**Namespace:** ASNA.QSys.Runtime.JobSupport
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception) --> [JobException](/reference/runtime/qsys-runtime-job-support/job-exception.html) --> [CPF0000Exception](/reference/runtime/qsys-runtime-job-support/cpf-exceptions/cpf0000-exception.html) --> [CPF7000Exception](/reference/runtime/qsys-runtime-job-support/cpf-exceptions/cpf7000-exception.html)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [CPF7310Exception](#cpf7310exceptionstring-string-string-exception)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception)) | Initializes a new instance of the CPF7310Exception class.

### CPF7310Exception([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception))

Initializes a new instance of the CPF7310Exception class.

```cs
CPF7310Exception(String, String, String, Exception)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | folder | The name of the folder (or library).
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | file | The name of the file.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | member | The name of the member.
| [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception) | innerException | The exception that is the cause of the current exception, or a null reference if no inner exception is specified.
