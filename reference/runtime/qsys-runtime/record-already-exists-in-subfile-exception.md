---
title: "RecordAlreadyExistsInSubfileException class"
description: "Record already exists in subfile: -subfile record name- exception. "
last_modified_at: 2024-08-08T21:41:46Z
---

Record already exists in subfile: -subfile record name- exception.

**Namespace:** ASNA.QSys.Runtime
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception) --> [RuntimeException](/reference/runtime/qsys-runtime/runtime-exception.html)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [RecordAlreadyExistsInSubfileException](#recordalreadyexistsinsubfileexceptionstring)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Constructor that takes the -subfile name- on an operation that cannot accept duplicate records.

### RecordAlreadyExistsInSubfileException([String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Constructor that takes the -subfile name- on an operation that cannot accept duplicate records.

```cs
RecordAlreadyExistsInSubfileException(String)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | FileName | Subfile record name.
