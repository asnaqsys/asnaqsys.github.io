---
title: "CPF0555Exception class        | QSYS API Reference Guide"
description: "The exception that is thrown when Date not in specified format or date not valid: {0} "
last_modified_at: 2024-08-09T17:25:29Z
---

The exception that is thrown when Date not in specified format or date not valid: {0}

**Namespace:** ASNA.QSys.Runtime.JobSupport
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception) --> [JobException](/reference/runtime/qsys-runtime-job-support/job-exception.html) --> [CPF0000Exception](/reference/runtime/qsys-runtime-job-support/cpf-exceptions/cpf0000-exception.html) --> [CPF0500Exception](/reference/runtime/qsys-runtime-job-support/cpf-exceptions/cpf0500-exception.html)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [CPF0555Exception](#cpf0555exceptionstring-exception)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception)) | Initializes a new instance of the CPF0555Exception class.

### CPF0555Exception([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception))

Initializes a new instance of the CPF0555Exception class.

```cs
CPF0555Exception(String, Exception)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | date | The invalid date.
| [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception) | innerException | The exception that is the cause of the current exception, or a null reference if no inner exception is specified.
