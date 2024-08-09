---
title: "Indicator struct              | QSYS API Reference Guide"
description: "This class represents an IBM i RPG Indicator.  "
last_modified_at: 2024-08-09T16:18:25Z
---

This class represents an IBM i RPG Indicator. 

**Namespace:** ASNA.QSys.Runtime
**Assembly:** ASNA.QSys.Runtime.dll

<br>
<br>

## Properties

| Type | Name | Description
| --- | --- | --- 
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | Length | Gets or Sets the size in bytes of an Indicator.  |
| [Char](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/char) | Value | Gets or sets the value of an Indicator. |
| [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) | ValueAsObject | Gets the value of an Indicator as object. |

## Methods

| Signature | Description |
| --- | --- |
| [CompareTo](#int-comparetoobject-obj)([Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | Compares this instance with a specified object returns an integer that indicates whether this instance precedes, follows, or appears in the same position in the sort order as the specified object.
| [Convert](#ifixedsizetype-char-convertchar-value)([Char](https://docs.microsoft.com/en-us/dotnet/api/system.char)) | Convert char to Indicator.
| [op_Explicit](#bool-op-explicitindicator-i)([Indicator](/reference/runtime/qsys-runtime/indicator.html)) | Gets the value of an Indicator as a boolean type.
| [op_LogicalNot](#bool-op-logicalnotindicator-i)([Indicator](/reference/runtime/qsys-runtime/indicator.html)) | Operator negate.
| [ToString()](#string-tostring) | Convert to string.

### int CompareTo([object obj](https://docs.microsoft.com/en-us/dotnet/api/system.object))

Compares this instance with a specified object returns an integer that indicates whether this instance precedes, follows, or appears in the same position in the sort order as the specified object.

```cs
int CompareTo(object obj)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) | obj | The object to compare against.

#### Returns

| Type | Description
| --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | A 32-bit signed integer that indicates whether this instance precedes, follows, or appears in the same position in the sort order as the obj parameter.

### IFixedSizeType\<char\> Convert([char value](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/char))

Convert char to Indicator.

```cs
IFixedSizeType<char> Convert(char value)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Char](https://docs.microsoft.com/en-us/dotnet/api/system.char) | value | Input char.

#### Returns

| Type | Description
| --- | ---
| [IFixedSizeType`1](/reference/runtime/qsys-runtime/i-fixed-size-type-1.html) | A new Indicator instance with the char value.

### bool op_Explicit([Indicator i](/reference/runtime/qsys-runtime/indicator.html))

Gets the value of an Indicator as a boolean type.

```cs
bool op_Explicit(Indicator i)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Indicator](/reference/runtime/qsys-runtime/indicator.html) | i | Input indicator

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | 

### bool op_LogicalNot([Indicator i](/reference/runtime/qsys-runtime/indicator.html))

Operator negate.

```cs
bool op_LogicalNot(Indicator i)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Indicator](/reference/runtime/qsys-runtime/indicator.html) | i | Input indicator.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | True if indicator was false, False otherwise.

### string ToString()

Convert to string.

```cs
string ToString()
```
