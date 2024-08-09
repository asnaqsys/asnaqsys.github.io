---
title: "DSArrayField class            | QSYS API Reference Guide"
description: "Describes a Data Structure field that is an array. "
last_modified_at: 2024-08-09T17:25:29Z
---

Describes a Data Structure field that is an array.

**Namespace:** ASNA.QSys.Runtime
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>

## Properties

| Type | Name | Description
| --- | --- | --- 
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | ElementLength | Length of the individual array elements. |
| [ILayout](/reference/runtime/qsys-runtime/i-layout.html) | Layout | Gets the ILayout of the array elements. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | Length | Length of the array. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | Name | Name of this array field. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | Start | Gets the starting position of this array field in the Data Structure buffer. |
| [Type](https://docs.microsoft.com/en-us/dotnet/api/system.type) | Type | Gets the type of the array. |
| [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) | Value | Gets a copy of the array, or sets the array elements. |

## Methods

| Signature | Description |
| --- | --- |
| [ClearField()](#void-clearfield) | Sets all elements of the array to their default value.
| [Clone()](#idsfield-clone) | Creates a copy of this IDSField object
| [SetStartingPosition](#void-setstartingpositionint-start)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Sets the starting position of this field within the Data Structure buffer.

### void ClearField()

Sets all elements of the array to their default value.

```cs
void ClearField()
```

### IDSField Clone()

Creates a copy of this IDSField object

```cs
IDSField Clone()
```

### void SetStartingPosition([int start](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Sets the starting position of this field within the Data Structure buffer.

```cs
void SetStartingPosition(int start)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | start | Starting position.
