---
title: "CPF338CException class        | QSYS API Reference Guide"
description: "The exception that is thrown when Internal spool control file/folder &#39;{0}&#39; not accessible. "
last_modified_at: 2024-08-09T16:18:25Z
---

The exception that is thrown when Internal spool control file/folder '{0}' not accessible.

**Namespace:** ASNA.QSys.Runtime.JobSupport
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception) --> [JobException](/reference/runtime/qsys-runtime-job-support/job-exception.html) --> [CPF0000Exception](/reference/runtime/qsys-runtime-job-support/cpf-exceptions/cpf0000-exception.html) --> [CPF3300Exception](/reference/runtime/qsys-runtime-job-support/cpf-exceptions/cpf3300-exception.html)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [CPF338CException](#cpf338cexceptionstring-exception)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception)) | Initializes a new instance of the CPF338CException class.

### CPF338CException([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception))

Initializes a new instance of the CPF338CException class.

```cs
CPF338CException(String, Exception)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | resourcePath | The path to the file or folder that is not accesible.
| [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception) | innerException | The exception that is the cause of the current exception, or a null reference if no inner exception is specified.
