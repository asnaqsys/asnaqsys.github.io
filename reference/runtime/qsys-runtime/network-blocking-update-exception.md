---
title: "NetworkBlockingUpdateException class"
description: "Network Blocking is not allowed for -filename- because it is opened for *UPDATE. "
last_modified_at: 2024-08-09T17:25:29Z
---

Network Blocking is not allowed for -filename- because it is opened for *UPDATE.

**Namespace:** ASNA.QSys.Runtime
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception) --> [RuntimeException](/reference/runtime/qsys-runtime/runtime-exception.html)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [NetworkBlockingUpdateException](#networkblockingupdateexceptionstring)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Constructor that takes -filename- attempting to request invalid Network Blocking exception.

### NetworkBlockingUpdateException([String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Constructor that takes -filename- attempting to request invalid Network Blocking exception.

```cs
NetworkBlockingUpdateException(String)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | FileName | Filename
