---
title: CPF2874Exception class
---

The exception that is thrown when Both to-file and from-file are the same. To-file {0} in library {1} is the same as the from-file.

**Namespace:** ASNA.QSys.Runtime.JobSupport
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception) --> [JobException](/reference/runtime/qsys-runtime-job-support/job-exception.html) --> [CPF0000Exception](/reference/runtime/qsys-runtime-job-support/cpf0000-exception.html) --> [CPF2800Exception](/reference/runtime/qsys-runtime-job-support/cpf2800-exception.html)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [CPF2874Exception](#cpf2874exceptionstring-string-exception)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception)) | Initializes a new instance of the CPF2874Exception class.

### CPF2874Exception([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception))

Initializes a new instance of the CPF2874Exception class.

```cs
CPF2874Exception(String, String, Exception)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | library | The name of the library.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | file | The name of the file.
| [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception) | innerException | The exception that is the cause of the current exception, or a null reference if no inner exception is specified.
