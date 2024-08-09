---
title: "CPFA030Exception class        | QSYS API Reference Guide"
description: "The exception that is thrown when Object {0} already in use. "
last_modified_at: 2024-08-09T16:18:25Z
---

The exception that is thrown when Object {0} already in use.

**Namespace:** ASNA.QSys.Runtime.JobSupport
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception) --> [JobException](/reference/runtime/qsys-runtime-job-support/job-exception.html) --> [CPF0000Exception](/reference/runtime/qsys-runtime-job-support/cpf-exceptions/cpf0000-exception.html) --> [CPFA000Exception](/reference/runtime/qsys-runtime-job-support/cpf-exceptions/cpfa000-exception.html)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [CPFA030Exception](#cpfa030exceptionstring-exception)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception)) | Initializes a new instance of the CPFA030Exception class.

### CPFA030Exception([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception))

Initializes a new instance of the CPFA030Exception class.

```cs
CPFA030Exception(String, Exception)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | nameobj | The name of the object already in use.
| [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception) | innerException | The exception that is the cause of the current exception, or a null reference if no inner exception is specified.
