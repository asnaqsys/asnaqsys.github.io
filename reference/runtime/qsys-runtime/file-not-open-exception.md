---
title: "FileNotOpenException class    | QSYS API Reference Guide"
description: "File -filename- is not open exception. "
last_modified_at: 2024-08-09T16:18:25Z
---

File -filename- is not open exception.

**Namespace:** ASNA.QSys.Runtime
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception) --> [RuntimeException](/reference/runtime/qsys-runtime/runtime-exception.html)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [FileNotOpenException](#filenotopenexceptionstring)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Constructor that takes the name of the file used on operations that required the file to be opened.

### FileNotOpenException([String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Constructor that takes the name of the file used on operations that required the file to be opened.

```cs
FileNotOpenException(String)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | FileName | Offending filename.
