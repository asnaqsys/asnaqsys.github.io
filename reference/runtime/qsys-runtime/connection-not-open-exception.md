---
title: "ConnectionNotOpenException class"
description: "File -filename- cannot be opened because a connection to database -database- has not been established exception. "
last_modified_at: 2024-08-09T17:25:29Z
---

File -filename- cannot be opened because a connection to database -database- has not been established exception.

**Namespace:** ASNA.QSys.Runtime
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception) --> [RuntimeException](/reference/runtime/qsys-runtime/runtime-exception.html)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [ConnectionNotOpenException](#connectionnotopenexceptionstring-string)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Constructor that takes the -filename- with non-established connection to -database name-, causing an exception.

### ConnectionNotOpenException([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Constructor that takes the -filename- with non-established connection to -database name-, causing an exception.

```cs
ConnectionNotOpenException(String, String)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | FileName | Filename.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | DBName | Database name.
