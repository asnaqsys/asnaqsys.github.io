---
title: "InvalidRRNException class     | QSYS API Reference Guide"
description: "Invalid RRN Value: -rrn- on file: -filename- exception. "
last_modified_at: 2024-08-09T17:25:29Z
---

Invalid RRN Value: -rrn- on file: -filename- exception.

**Namespace:** ASNA.QSys.Runtime
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception) --> [RuntimeException](/reference/runtime/qsys-runtime/runtime-exception.html)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [InvalidRRNException](#invalidrrnexceptionint32-string)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Constructor that takes the -rrn-

### InvalidRRNException([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Constructor that takes the -rrn-

```cs
InvalidRRNException(Int32, String)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | rrn | Relative Record Number.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | FileName | Filename.
