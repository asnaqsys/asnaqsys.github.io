---
title: "IDSField interface            | QSYS API Reference Guide"
description: "Describes the common operations over a field in a Data Structure. "
last_modified_at: 2024-08-09T17:25:29Z
---

Describes the common operations over a field in a Data Structure.

**Namespace:** ASNA.QSys.Runtime
**Assembly:** ASNA.QSys.Runtime.dll

**Extends:** doesn't extend any other interfaces.
<br>
<br>

## Properties

| Type | Name | Description
| --- | --- | --- 
| [ILayout](/reference/runtime/qsys-runtime/i-layout.html) | Layout | Gets the field Layout. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | Length | Gets the field length. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | Name | Gets the name of the field. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | Start | Gets the starting position in the Data Structure buffer. |
| [Type](https://docs.microsoft.com/en-us/dotnet/api/system.type) | Type | Gets the type of the field |
| [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) | Value | Gets or sets the value of the field. |

## Methods

| Signature | Description |
| --- | --- |
| [ClearField()](#void-clearfield) | Clears the field to its default value.
| [Clone()](#idsfield-clone) | Creates a copy of this IDSField object
| [SetStartingPosition](#void-setstartingpositionint-start)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Sets the field starting position in the Data Structure buffer.

### void ClearField()

Clears the field to its default value.

```cs
void ClearField()
```

### IDSField Clone()

Creates a copy of this IDSField object

```cs
IDSField Clone()
```

### void SetStartingPosition([int start](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Sets the field starting position in the Data Structure buffer.

```cs
void SetStartingPosition(int start)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | start | The starting position of this field in the DataStructure buffer
