---
title: FixedDecimal<T,U> Class
---

Holds a fixed-decimal value with the specified number of digits and decimal positions.

**Namespace:** ASNA.QSys.Runtime <br/>
**Assembly:** ASNA.QSys.Runtime

<br>
<br>

## Remarks

Holds a fixed-decimal value with the specified number of digits and decimal positions.

[//]: # ($$TODO: Complete the Remarks section.)

<br>
<br>

## Properties

| Type | Name | Description | Indexer
| --- | --- | --- | --- 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | Decimals | Gets the number of decimal positions in this FixedDecimal number. | 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | Digits | Gets the number of digits in this FixedDecimal number. | 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | Length | Gets the length of this FixedDecimal. | 
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | Value | Gets the value of this FixedDecimal as a decimal. | 
| [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) | ValueAsObject | Gets the value of this FixedDecimal as an object. | 

<br>
<br>

## Methods

| Type | Name | Description | Return Description 
| --- | --- | --- | --- 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | [CompareTo](#comparetoobject)([Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | Compare to object. | A 32-bit signed integer that indicates whether this instance precedes, follows, or appears in the same position in the sort order as the obj parameter.
| [IFixedSizeType&lt;Decimal&gt;](/reference/asna-qsys-runtime/i-fixed-size-type.html) | [Convert](#convertdecimal)([Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal)) | Convert to IFixedSizeType. | The resulting IFixedSizeType.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | [Equals](#equalsdecimal>)([Decimal&gt;](/reference/asna-qsys-runtime/i-fixed-size-type.html)) | Determines whether two IFixedSizeType objects have the same value. | True if the value of the value parameter is the same as this IFixedSizeType; otherwise, false.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | [Equals](#equalsobject)([Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | Determines whether two FixedDecimals have the same value. | true if the value of the value parameter is the same as this string; otherwise, false.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | [GetHashCode](#gethashcode)() | Returns the hash code for this instance. | A hash code for the current FixedDecimal.
| [FixedDecimal](/reference/asna-qsys-runtime/classes/fixed-decimal.html) | [MergeLeft](#mergeleftstring-boolean)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Merge left. | The FixedDecimal result.
| [FixedDecimal](/reference/asna-qsys-runtime/classes/fixed-decimal.html) | [MergeRight](#mergerightstring-boolean)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Merge right. | The FixedDecimal result.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [ToPackedRepresentation](#topackedrepresentation)() | Convert this FixedDecimal to its packed representation. | The string containing the packed representation.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [ToString](#tostring)() | Convert to string. | The resulting numeric string, formatted in the current culture.

<br>
<br>

### CompareTo([Object](https://docs.microsoft.com/en-us/dotnet/api/system.object))

Compare to object.

```cs
CompareTo(Object obj);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) | obj | The object to compare against. 

#### Returns

[Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)

A 32-bit signed integer that indicates whether this instance precedes, follows, or appears in the same position in the sort order as the obj parameter.


<br>
<br>

### Convert([Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal))

Convert to IFixedSizeType.

```cs
Convert(Decimal value);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | value | The value to convert. 

#### Returns

[IFixedSizeType&lt;Decimal&gt;](/reference/asna-qsys-runtime/i-fixed-size-type.html)

The resulting IFixedSizeType.


<br>
<br>

### Equals([Decimal&gt;](/reference/asna-qsys-runtime/i-fixed-size-type.html))

Determines whether two IFixedSizeType objects have the same value.

```cs
Equals(Runtime.IFixedSizeType<System.Decimal> other);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Decimal&gt;](/reference/asna-qsys-runtime/i-fixed-size-type.html) | other | The decimal to compare to. 

#### Returns

[Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)

True if the value of the value parameter is the same as this IFixedSizeType; otherwise, false.


<br>
<br>

### Equals([Object](https://docs.microsoft.com/en-us/dotnet/api/system.object))

Determines whether two FixedDecimals have the same value.

```cs
Equals(Object obj);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) | obj | Object to test. 

#### Returns

[Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)

true if the value of the value parameter is the same as this string; otherwise, false.


<br>
<br>

### GetHashCode()

Returns the hash code for this instance.

```cs
GetHashCode();
```

#### Returns

[Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)

A hash code for the current FixedDecimal.


<br>
<br>

### MergeLeft([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Merge left.

```cs
MergeLeft(String s, Boolean pad);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | s | Input string. 
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | pad | True is padding with zeroes. Default is false. 

#### Returns

[FixedDecimal](/reference/asna-qsys-runtime/classes/fixed-decimal.html)

The FixedDecimal result.


<br>
<br>

### MergeRight([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Merge right.

```cs
MergeRight(String s, Boolean pad);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | s | Input string. 
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | pad | True if padding with zeroes. Default is false. 

#### Returns

[FixedDecimal](/reference/asna-qsys-runtime/classes/fixed-decimal.html)

The FixedDecimal result.


<br>
<br>

### ToPackedRepresentation()

Convert this FixedDecimal to its packed representation.

```cs
ToPackedRepresentation();
```

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

The string containing the packed representation.


<br>
<br>

### ToString()

Convert to string.

```cs
ToString();
```

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

The resulting numeric string, formatted in the current culture.


<br>
<br>

