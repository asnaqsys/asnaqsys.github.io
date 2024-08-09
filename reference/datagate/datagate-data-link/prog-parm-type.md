---
title: "ProgParmType class            | QSYS API Reference Guide"
description: "Represents the type of a program parameter in a DataLink connection. "
last_modified_at: 2024-08-09T16:18:40Z
---

Represents the type of a program parameter in a DataLink connection.

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
| [ProgParmType](#progparmtypestring-int32-fieldtype)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [FieldType](/reference/datagate/datagate-common/field-type.html)) | Initializes a new instance of the  class with the specified name, number of elements, and field type.

### ProgParmType([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [FieldType](/reference/datagate/datagate-common/field-type.html))

Initializes a new instance of the  class with the specified name, number of elements, and field type.

```cs
ProgParmType(String, Int32, FieldType)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | name | The name of the program parameter.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | cElems | The number of elements in the program parameter.
| [FieldType](/reference/datagate/datagate-common/field-type.html) | type | The field type of the program parameter.
