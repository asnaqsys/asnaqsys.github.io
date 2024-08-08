---
title: "CPF3357Exception class        | QSYS API Reference Guide"
description: "The exception that is thrown when Output queue {0} does not exist. "
last_modified_at: 2024-08-08T21:41:46Z
---

The exception that is thrown when Output queue {0} does not exist.

**Namespace:** ASNA.QSys.Runtime.JobSupport
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception) --> [JobException](/reference/runtime/qsys-runtime-job-support/job-exception.html) --> [CPF0000Exception](/reference/runtime/qsys-runtime-job-support/cpf-exceptions/cpf0000-exception.html) --> [CPF3300Exception](/reference/runtime/qsys-runtime-job-support/cpf-exceptions/cpf3300-exception.html)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [CPF3357Exception](#cpf3357exceptionstring-exception)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception)) | Initializes a new instance of the CPF3357Exception class.

### CPF3357Exception([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception))

Initializes a new instance of the CPF3357Exception class.

```cs
CPF3357Exception(String, Exception)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | outputQueueName | Name of output queue not found.
| [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception) | innerException | The exception that is the cause of the current exception, or a null reference if no inner exception is specified.
