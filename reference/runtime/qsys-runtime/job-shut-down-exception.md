---
title: "JobShutDownException class    | QSYS API Reference Guide"
description: "The exception that is thrown to end a job. "
last_modified_at: 2024-08-09T16:18:25Z
---

The exception that is thrown to end a job.

**Namespace:** ASNA.QSys.Runtime
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception) --> [RuntimeException](/reference/runtime/qsys-runtime/runtime-exception.html) --> [EndOperationException](/reference/runtime/qsys-runtime/end-operation-exception.html)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [JobShutDownException](#jobshutdownexceptionstring-exception)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception)) | Initializes a new instance of the JobShutDownException class.

### JobShutDownException([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception))

Initializes a new instance of the JobShutDownException class.

```cs
JobShutDownException(String, Exception)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | Message | Message explaining the end operation.
| [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception) | InnerException | Original exception.
