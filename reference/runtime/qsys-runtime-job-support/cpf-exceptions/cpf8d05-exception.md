---
title: "CPF8D05Exception class        | QSYS API Reference Guide"
description: "The exception that is thrown when Library {0} already exists. "
last_modified_at: 2024-08-08T21:41:46Z
---

The exception that is thrown when Library {0} already exists.

**Namespace:** ASNA.QSys.Runtime.JobSupport
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception) --> [JobException](/reference/runtime/qsys-runtime-job-support/job-exception.html) --> [CPF0000Exception](/reference/runtime/qsys-runtime-job-support/cpf-exceptions/cpf0000-exception.html) --> [CPF8D00Exception](/reference/runtime/qsys-runtime-job-support/cpf-exceptions/cpf8d00-exception.html)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [CPF8D05Exception](#cpf8d05exceptionstring-exception)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception)) | Initializes a new instance of the CPF8D05Exception class.

### CPF8D05Exception([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception))

Initializes a new instance of the CPF8D05Exception class.

```cs
CPF8D05Exception(String, Exception)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | folder | The name of the folder (or library).
| [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception) | innerException | The exception that is the cause of the current exception, or a null reference if no inner exception is specified.
