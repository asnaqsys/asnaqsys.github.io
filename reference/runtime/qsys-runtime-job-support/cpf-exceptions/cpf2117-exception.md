---
title: "CPF2117Exception class        | QSYS API Reference Guide"
description: "The exception that is thrown when {0} Objects of type {1} were deleted but {2} were not deleted. "
last_modified_at: 2024-08-09T16:18:25Z
---

The exception that is thrown when {0} Objects of type {1} were deleted but {2} were not deleted.

**Namespace:** ASNA.QSys.Runtime.JobSupport
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception) --> [JobException](/reference/runtime/qsys-runtime-job-support/job-exception.html) --> [CPF0000Exception](/reference/runtime/qsys-runtime-job-support/cpf-exceptions/cpf0000-exception.html) --> [CPF2100Exception](/reference/runtime/qsys-runtime-job-support/cpf-exceptions/cpf2100-exception.html)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [CPF2117Exception](#cpf2117exceptionint32-string-int32-exception)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception)) | Initializes a new instance of the CPF2117Exception class.

### CPF2117Exception([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception))

Initializes a new instance of the CPF2117Exception class.

```cs
CPF2117Exception(Int32, String, Int32, Exception)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | deleted | The number of objects deleted.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | objectType | The type of objects deleted.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | notDeleted | The number of objects not deleted.
| [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception) | innerException | The exception that is the cause of the current exception, or a null reference if no inner exception is specified.
