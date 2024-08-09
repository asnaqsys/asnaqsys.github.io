---
title: "RequiredOpenConnectionException class"
description: "Operation not available on un-opened Database -database name- exception. "
last_modified_at: 2024-08-09T16:18:25Z
---

Operation not available on un-opened Database -database name- exception.

**Namespace:** ASNA.QSys.Runtime
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception) --> [RuntimeException](/reference/runtime/qsys-runtime/runtime-exception.html)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [RequiredOpenConnectionException](#requiredopenconnectionexceptionstring)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Constructor that takes un-opened -database name- causing an exception.

### RequiredOpenConnectionException([String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Constructor that takes un-opened -database name- causing an exception.

```cs
RequiredOpenConnectionException(String)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | DBName | Database name.
