---
title: "FixedDecimal<T1, T2> struct   | QSYS API Reference Guide"
description: "Holds a fixed-decimal value with the specified number of digits and decimal positions. "
last_modified_at: 2024-08-09T17:25:29Z
---

Holds a fixed-decimal value with the specified number of digits and decimal positions.

**Namespace:** ASNA.QSys.Runtime
**Assembly:** ASNA.QSys.Runtime.dll

<br>
<br>

## Properties

| Type | Name | Description
| --- | --- | --- 
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | Decimals | Gets the number of decimal positions in this FixedDecimal number. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | Digits | Gets the number of digits in this FixedDecimal number. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | Length | Gets the length of this FixedDecimal. |
| [Decimal](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types) | Value | Gets the value of this FixedDecimal as a decimal. |
| [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) | ValueAsObject | Gets the value of this FixedDecimal as an object. |

## Methods

| Signature | Description |
| --- | --- |
| [CompareTo](#int-comparetoobject-obj)([Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | Compare to object.
| [Convert](#ifixedsizetype-decimal-convertdecimal-value)([Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal)) | Convert to IFixedSizeType. 
| [Equals](#bool-equalsobject-obj)([Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | Determines whether two FixedDecimals have the same value.
| [GetHashCode()](#int-gethashcode) | Returns the hash code for this instance.
| [MergeLeft](#fixeddecimal-tdigits-tdecimals-mergeleftstring-s-bool-pad)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Merge left.
| [MergeRight](#fixeddecimal-tdigits-tdecimals-mergerightstring-s-bool-pad)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Merge right.
| [ToPackedRepresentation()](#string-topackedrepresentation) | Convert this FixedDecimal to its packed representation.
| [ToString()](#string-tostring) | Convert to string.

### int CompareTo([object obj](https://docs.microsoft.com/en-us/dotnet/api/system.object))

Compare to object.

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

### IFixedSizeType\<decimal\> Convert([decimal value](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types))

Convert to IFixedSizeType. 

```cs
IFixedSizeType<decimal> Convert(decimal value)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | value | The value to convert.

#### Returns

| Type | Description
| --- | ---
| [IFixedSizeType`1](/reference/runtime/qsys-runtime/i-fixed-size-type-1.html) | The resulting IFixedSizeType.

### bool Equals([object obj](https://docs.microsoft.com/en-us/dotnet/api/system.object))

Determines whether two FixedDecimals have the same value.

```cs
bool Equals(object obj)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) | obj | Object to test.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | true if the value of the value parameter is the same as this string; otherwise, false.

### int GetHashCode()

Returns the hash code for this instance.

```cs
int GetHashCode()
```

### FixedDecimal\<TDigits, TDecimals\> MergeLeft([string s](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [bool pad](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Merge left.

```cs
FixedDecimal<TDigits, TDecimals> MergeLeft(string s, bool pad)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | s | Input string.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | pad | True is padding with zeroes. Default is false.

#### Returns

| Type | Description
| --- | ---
| [FixedDecimal`2](/reference/runtime/qsys-runtime/fixed-decimal-2.html) | The FixedDecimal result.

### FixedDecimal\<TDigits, TDecimals\> MergeRight([string s](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [bool pad](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Merge right.

```cs
FixedDecimal<TDigits, TDecimals> MergeRight(string s, bool pad)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | s | Input string.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | pad | True if padding with zeroes. Default is false.

#### Returns

| Type | Description
| --- | ---
| [FixedDecimal`2](/reference/runtime/qsys-runtime/fixed-decimal-2.html) | The FixedDecimal result.

### string ToPackedRepresentation()

Convert this FixedDecimal to its packed representation.

```cs
string ToPackedRepresentation()
```

### string ToString()

Convert to string.

```cs
string ToString()
```
