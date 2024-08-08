---
title: "NetworkBlockingOutputException class"
description: "Network Blocking is not allowed for *OUTPUT if CacheWrites is *NO on file -filename-. "
last_modified_at: 2024-08-08T21:41:46Z
---

Network Blocking is not allowed for *OUTPUT if CacheWrites is *NO on file -filename-.

**Namespace:** ASNA.QSys.Runtime
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception) --> [RuntimeException](/reference/runtime/qsys-runtime/runtime-exception.html)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [NetworkBlockingOutputException](#networkblockingoutputexceptionstring)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Constructor that takes *OUTPUT with no CacheWrites -filename- causing invalid Network Blocking exception.

### NetworkBlockingOutputException([String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Constructor that takes *OUTPUT with no CacheWrites -filename- causing invalid Network Blocking exception.

```cs
NetworkBlockingOutputException(String)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | FileName | Filename
