---
title: "DSField class                 | QSYS API Reference Guide"
description: "Describes a field in a Data Structure. "
last_modified_at: 2024-08-09T17:25:29Z
---

Describes a field in a Data Structure.

**Namespace:** ASNA.QSys.Runtime
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>

## Remarks
Use this class when defining a field-base layout for a Data Structure.

<br>
<br>

## Properties

| Type | Name | Description
| --- | --- | --- 
| [ILayout](/reference/runtime/qsys-runtime/i-layout.html) | Layout | Gets the Layout of this field. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | Length | Gets the length of the field. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | Name | Gets the name of the field. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | Start | Gets the position of the field in the Data Structure buffer. |
| [Type](https://docs.microsoft.com/en-us/dotnet/api/system.type) | Type | Gets the field type. |
| [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) | Value | Gets or sets the field value. |

## Methods

| Signature | Description |
| --- | --- |
| [ClearField()](#void-clearfield) | Sets the field value to its default according to its type.
| [Clone()](#idsfield-clone) | Creates a copy of this IDSField object
| [SetStartingPosition](#void-setstartingpositionint-start)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Sets the value of Start, the staring position of the field in the Data Structure buffer.

### void ClearField()

Sets the field value to its default according to its type.

```cs
void ClearField()
```

### IDSField Clone()

Creates a copy of this IDSField object

```cs
IDSField Clone()
```

### void SetStartingPosition([int start](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Sets the value of Start, the staring position of the field in the Data Structure buffer.

```cs
void SetStartingPosition(int start)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | start | The starting position of this field in the DataStructure buffer
