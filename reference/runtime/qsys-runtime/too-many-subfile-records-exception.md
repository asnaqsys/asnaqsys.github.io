---
title: "TooManySubfileRecordsException class"
description: "Record -rrn- does not fit in subfile -subfile name- on file -filename- exception. "
last_modified_at: 2024-08-09T16:18:25Z
---

Record -rrn- does not fit in subfile -subfile name- on file -filename- exception.

**Namespace:** ASNA.QSys.Runtime
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception) --> [RuntimeException](/reference/runtime/qsys-runtime/runtime-exception.html)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [TooManySubfileRecordsException](#toomanysubfilerecordsexceptionint32-string-string)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Constructor that takes the invalid -rrn- for -subfile name- on file -filename- that caused the exception. 

### TooManySubfileRecordsException([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Constructor that takes the invalid -rrn- for -subfile name- on file -filename- that caused the exception. 

```cs
TooManySubfileRecordsException(Int32, String, String)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | rrn | Relative Record Number.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | SubfileName | Subfile name.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | FileName | Filename.
