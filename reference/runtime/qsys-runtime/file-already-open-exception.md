---
title: "FileAlreadyOpenException class"
description: "File -filename- is already open exception. "
last_modified_at: 2024-08-09T16:18:25Z
---

File -filename- is already open exception.

**Namespace:** ASNA.QSys.Runtime
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception) --> [RuntimeException](/reference/runtime/qsys-runtime/runtime-exception.html)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [FileAlreadyOpenException](#filealreadyopenexceptionstring)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Constructor that takes the name of the open file that was expected to be closed causing the exception. 

### FileAlreadyOpenException([String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Constructor that takes the name of the open file that was expected to be closed causing the exception. 

```cs
FileAlreadyOpenException(String)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | FileName | Offending filename.
