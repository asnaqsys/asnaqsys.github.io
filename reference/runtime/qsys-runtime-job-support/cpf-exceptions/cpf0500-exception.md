---
title: "CPF0500Exception class | QSYS API Reference Guide"
description: "Defines the core behavior of CPF05xx exceptions. "
last_modified_at: 2024-07-09T17:00:49Z
---

Defines the core behavior of CPF05xx exceptions.

**Namespace:** ASNA.QSys.Runtime.JobSupport
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception) --> [JobException](/reference/runtime/qsys-runtime-job-support/job-exception.html) --> [CPF0000Exception](/reference/runtime/qsys-runtime-job-support/cpf-exceptions/cpf0000-exception.html)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [CPF0500Exception](#cpf0500exceptionstring-exception)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception)) | Initializes a new instance of the CPF0500Exception class.

### CPF0500Exception([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception))

Initializes a new instance of the CPF0500Exception class.

```cs
CPF0500Exception(String, Exception)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | message | The exception that is the cause of the current exception, or a null reference if no inner exception is specified.
| [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception) | inner | The error message that explains the reason for the exception.
