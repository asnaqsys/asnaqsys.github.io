---
title: CPF2139Exception class
description: "The exception that is thrown when Rename of library {0} failed. "
last_modified_at: 2024-06-28T18:18:37Z
---

The exception that is thrown when Rename of library {0} failed.

**Namespace:** ASNA.QSys.Runtime.JobSupport
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception) --> [JobException](/reference/runtime/qsys-runtime-job-support/job-exception.html) --> [CPF0000Exception](/reference/runtime/qsys-runtime-job-support/cpf-exceptions/cpf0000-exception.html) --> [CPF2100Exception](/reference/runtime/qsys-runtime-job-support/cpf-exceptions/cpf2100-exception.html)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [CPF2139Exception](#cpf2139exceptionstring-exception)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception)) | Initializes a new instance of the CPF2139Exception class.

### CPF2139Exception([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception))

Initializes a new instance of the CPF2139Exception class.

```cs
CPF2139Exception(String, Exception)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | folder | The name of the folder (or library).
| [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception) | innerException | The exception that is the cause of the current exception, or a null reference if no inner exception is specified.
