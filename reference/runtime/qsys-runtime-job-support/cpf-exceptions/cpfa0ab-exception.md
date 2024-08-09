---
title: "CPFA0ABException class        | QSYS API Reference Guide"
description: "The exception that is thrown when Operation failed for object. Object is {0} "
last_modified_at: 2024-08-09T17:25:29Z
---

The exception that is thrown when Operation failed for object. Object is {0}

**Namespace:** ASNA.QSys.Runtime.JobSupport
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception) --> [JobException](/reference/runtime/qsys-runtime-job-support/job-exception.html) --> [CPF0000Exception](/reference/runtime/qsys-runtime-job-support/cpf-exceptions/cpf0000-exception.html) --> [CPFA000Exception](/reference/runtime/qsys-runtime-job-support/cpf-exceptions/cpfa000-exception.html)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [CPFA0ABException](#cpfa0abexceptionstring-exception)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception)) | Initializes a new instance of the CPFA0ABException class.

### CPFA0ABException([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception))

Initializes a new instance of the CPFA0ABException class.

```cs
CPFA0ABException(String, Exception)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | objectName | The name of the object.
| [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception) | innerException | The exception that is the cause of the current exception, or a null reference if no inner exception is specified.
