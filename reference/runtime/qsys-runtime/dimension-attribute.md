---
title: "DimensionAttribute class      | QSYS API Reference Guide"
description: "A non-RPG class, property or field may be stamped with this attribute to indicate a consumer RPG program to consider it as an array with the specified"
last_modified_at: 2024-08-08T21:41:46Z
---

A non-RPG class, property or field may be stamped with this attribute to indicate a consumer RPG program to consider it as an array with the specified dimension.

**Namespace:** ASNA.QSys.Runtime
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [Attribute](https://docs.microsoft.com/en-us/dotnet/api/system.attribute)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [DimensionAttribute](#dimensionattributeint32-int32)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Initializes a DimensionAttribute object. Describes the item as a fixed-size array with the specified dimensions.

### DimensionAttribute([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

Initializes a DimensionAttribute object. Describes the item as a fixed-size array with the specified dimensions.

```cs
DimensionAttribute(Int32, Int32)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | dimNumber | The dimension number.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | count | The count of elements in the dimension.

## Properties

| Type | Name | Description
| --- | --- | --- 
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | Count | Gets the count of elements in the dimension. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | DimNumber | Gets the dimension number. |
