---
title: "UpdateWithoutAPriorInputOperationException class"
description: "Update subfile record without a prior input operation. "
last_modified_at: 2024-08-09T16:18:25Z
---

Update subfile record without a prior input operation.

**Namespace:** ASNA.QSys.Runtime
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception) --> [RuntimeException](/reference/runtime/qsys-runtime/runtime-exception.html)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [UpdateWithoutAPriorInputOperationException](#updatewithoutapriorinputoperationexceptionstring-int32)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Constructor that takes the -subfile name- and optionally -rrn- where an input operation without prior update cause an exception.

### UpdateWithoutAPriorInputOperationException([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

Constructor that takes the -subfile name- and optionally -rrn- where an input operation without prior update cause an exception.

```cs
UpdateWithoutAPriorInputOperationException(String, Int32)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | FileName | Subfile name.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | baseOneRrn | Relative Record Number or Zero if no RRN identified.
