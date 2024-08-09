---
title: "CPF3360Exception class        | QSYS API Reference Guide"
description: "The exception that is thrown when Output queue {0} not deleted. Output queue in use. "
last_modified_at: 2024-08-09T17:25:29Z
---

The exception that is thrown when Output queue {0} not deleted. Output queue in use.

**Namespace:** ASNA.QSys.Runtime.JobSupport
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception) --> [JobException](/reference/runtime/qsys-runtime-job-support/job-exception.html) --> [CPF0000Exception](/reference/runtime/qsys-runtime-job-support/cpf-exceptions/cpf0000-exception.html) --> [CPF3300Exception](/reference/runtime/qsys-runtime-job-support/cpf-exceptions/cpf3300-exception.html)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [CPF3360Exception](#cpf3360exceptionstring-exception)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception)) | Initializes a new instance of the CPF3360Exception class.

### CPF3360Exception([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception))

Initializes a new instance of the CPF3360Exception class.

```cs
CPF3360Exception(String, Exception)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | outputQueueName | Name of busy output queue.
| [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception) | innerException | The exception that is the cause of the current exception, or a null reference if no inner exception is specified.
