---
title: "StructureType class           | QSYS API Reference Guide"
description: "Represents a structured type in a DataLink connection, which can contain multiple other types. "
last_modified_at: 2024-08-09T17:25:07Z
---

Represents a structured type in a DataLink connection, which can contain multiple other types.

**Namespace:** ASNA.DataGate.DataLink
**Assembly:** ASNA.QSys.DataGate.Client.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>
## Thread Safety

Any public static (Shared) members of this type are safe for multithreaded operations. Any instance members are not guaranteed to be thread safe.


## Constructors

| Name | Description |
| --- | --- |
| [StructureType](#structuretypestring-int32-object)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Object\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | Initializes a new instance of the  class with the specified name, number of elements, and members.

### StructureType([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Object\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.object))

Initializes a new instance of the  class with the specified name, number of elements, and members.

```cs
StructureType(String, Int32, Object[])
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | name | The name of the structure.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | cElems | The number of elements in the structure.
| [Object\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.object) | members | The members of the structure.
