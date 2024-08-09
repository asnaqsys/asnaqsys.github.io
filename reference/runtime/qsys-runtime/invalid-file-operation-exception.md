---
title: "InvalidFileOperationException class"
description: "Invalid Operation: -operation- on file: -filename- exception. "
last_modified_at: 2024-08-09T16:18:25Z
---

Invalid Operation: -operation- on file: -filename- exception.

**Namespace:** ASNA.QSys.Runtime
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception) --> [RuntimeException](/reference/runtime/qsys-runtime/runtime-exception.html)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [InvalidFileOperationException](#invalidfileoperationexceptionstring-string)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Constructor that takes the -operation- attempting to execute on -filename- that caused an exception.

### InvalidFileOperationException([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Constructor that takes the -operation- attempting to execute on -filename- that caused an exception.

```cs
InvalidFileOperationException(String, String)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | Operation | Operation name.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | FileName | Filename.
