---
title: "CPF1028Exception class        | QSYS API Reference Guide"
description: "The exception that is thrown when {0} not valid for parameter SYSVAL. "
last_modified_at: 2024-08-08T21:41:46Z
---

The exception that is thrown when {0} not valid for parameter SYSVAL.

**Namespace:** ASNA.QSys.Runtime.JobSupport
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception) --> [JobException](/reference/runtime/qsys-runtime-job-support/job-exception.html) --> [CPF0000Exception](/reference/runtime/qsys-runtime-job-support/cpf-exceptions/cpf0000-exception.html) --> [CPF1000Exception](/reference/runtime/qsys-runtime-job-support/cpf-exceptions/cpf1000-exception.html)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [CPF1028Exception](#cpf1028exceptionstring-exception)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception)) | Initializes a new instance of the CPF1028Exception class.

### CPF1028Exception([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception))

Initializes a new instance of the CPF1028Exception class.

```cs
CPF1028Exception(String, Exception)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | systemValue | The invalid system value.
| [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception) | innerException | The exception that is the cause of the current exception, or a null reference if no inner exception is specified.
