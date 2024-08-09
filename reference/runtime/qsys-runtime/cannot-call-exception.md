---
title: "CannotCallException class     | QSYS API Reference Guide"
description: "Exception thrown when trying to use a multidimensional multi data structure in a CALL. "
last_modified_at: 2024-08-09T17:25:29Z
---

Exception thrown when trying to use a multidimensional multi data structure in a CALL.

**Namespace:** ASNA.QSys.Runtime
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception) --> [RuntimeException](/reference/runtime/qsys-runtime/runtime-exception.html)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [CannotCallException](#cannotcallexceptionint32)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Constructs an exception that is thrown when trying to use a multidimensional multi data structure in a CALL.

### CannotCallException([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

Constructs an exception that is thrown when trying to use a multidimensional multi data structure in a CALL.

```cs
CannotCallException(Int32)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | rank | The rank of the multidimensional multi data structure.
