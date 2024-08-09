---
title: "DimArrayTypeAttribute class   | QSYS API Reference Guide"
description: "A non-RPG class may stamp an array member with this attribute to be considered as a fixed-sized array by a consumer RPG program. "
last_modified_at: 2024-08-09T16:18:25Z
---

A non-RPG class may stamp an array member with this attribute to be considered as a fixed-sized array by a consumer RPG program.

**Namespace:** ASNA.QSys.Runtime
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [Attribute](https://docs.microsoft.com/en-us/dotnet/api/system.attribute)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [DimArrayTypeAttribute](#dimarraytypeattributeint32)([Int32\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Initializes a DimArrayTypeAttribute object. The attribute describes the item as a fixed-size array.

### DimArrayTypeAttribute([Int32\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

Initializes a DimArrayTypeAttribute object. The attribute describes the item as a fixed-size array.

```cs
DimArrayTypeAttribute(Int32[])
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | dims | The dimensions of the array.

## Properties

| Type | Name | Description
| --- | --- | --- 
| [Int32\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | Dimensions | Gets the dimensions of the array. |
