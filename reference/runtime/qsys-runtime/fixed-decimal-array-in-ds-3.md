---
title: "FixedDecimalArrayInDS<T1, T2, T3> struct"
description: "Describes a fixed size array of FixedDecimal contained in a DataStructure. "
last_modified_at: 2024-08-09T16:18:25Z
---

Describes a fixed size array of FixedDecimal contained in a DataStructure.

**Namespace:** ASNA.QSys.Runtime
**Assembly:** ASNA.QSys.Runtime.dll

<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [FixedDecimalArrayInDS](#fixeddecimalarrayindsmultidatastructure-layouttype-int32-int32)([MultiDataStructure](/reference/runtime/qsys-runtime/multi-data-structure.html), [LayoutType](/reference/runtime/qsys-runtime/layout-type.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Constructs a fixed size array of FixedDecimal in a Multiple Occurrence Data Structure.
| [FixedDecimalArrayInDS](#fixeddecimalarrayindsdatastructure-layouttype-int32-int32)([DataStructure](/reference/runtime/qsys-runtime/data-structure.html), [LayoutType](/reference/runtime/qsys-runtime/layout-type.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Constructs a fixed size array of FixedDecimal in a Data Structure.

### FixedDecimalArrayInDS([MultiDataStructure](/reference/runtime/qsys-runtime/multi-data-structure.html), [LayoutType](/reference/runtime/qsys-runtime/layout-type.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

Constructs a fixed size array of FixedDecimal in a Multiple Occurrence Data Structure.

```cs
FixedDecimalArrayInDS(MultiDataStructure, LayoutType, Int32, Int32)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [MultiDataStructure](/reference/runtime/qsys-runtime/multi-data-structure.html) | parent | The MultiDataStructure containing this array of FixedDecimal.
| [LayoutType](/reference/runtime/qsys-runtime/layout-type.html) | decimalType | The LayoutType describing the kind of fixed decimals, zoned, packed, or binary, the array contains.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | startPos | The starting position of the array within the DataStructure buffer.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | skipPositions | For non-contiguous arrays, the number of position between two consecutive array elements.

### FixedDecimalArrayInDS([DataStructure](/reference/runtime/qsys-runtime/data-structure.html), [LayoutType](/reference/runtime/qsys-runtime/layout-type.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

Constructs a fixed size array of FixedDecimal in a Data Structure.

```cs
FixedDecimalArrayInDS(DataStructure, LayoutType, Int32, Int32)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DataStructure](/reference/runtime/qsys-runtime/data-structure.html) | parent | The DataStructure containing this array of FixedDecimal.
| [LayoutType](/reference/runtime/qsys-runtime/layout-type.html) | decimalType | The LayoutType describing the kind of fixed decimals, zoned, packed, or binary, the array contains.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | startPos | The starting position of the array within the DataStructure buffer.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | skipPositions | For non-contiguous arrays, the number of position between two consecutive array elements.

## Properties

| Type | Name | Description
| --- | --- | --- 
| [FixedDecimal\<TDigits, TDecimals\>](/reference/runtime/qsys-runtime/fixed-decimal-2.html) | Item | Indexer over the array, gets or sets the FixedDecimal element at that position. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | Length | Gets the total number of elements in the array. |
| [DataStructure](/reference/runtime/qsys-runtime/data-structure.html) | ParentDS | Gets the Data Structure to which this field belongs. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | SkipPositions | For non-contiguous arrays, gets the number of buffer positions between consecutive array elements. 0 otherwise. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | StartPosition | Gets the Data Structure buffer position where this array starts. |

## Methods

| Signature | Description |
| --- | --- |
| [Clear()](#void-clear) | Sets all array elements to 0.
| [CopyFrom](#void-copyfromdecimal--sourcearray-int-targetstartat)([Decimal\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Copies elements from a decimal[] into this array.
| [GetEnumerator()](#ienumerator-fixeddecimal-tdigits-tdecimals--getenumerator) | Returns an enumerator that iterates through the array.
| [GetStartingPosition](#int-getstartingpositionint-index)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Gets the starting position in the DataStructure buffer of the element indicated by the index parameter.
| [op_Explicit](#decimal--op-explicitfixeddecimalarrayinds-tdim-tdigits-tdecimals-array)([FixedDecimalArrayInDS\<TDim, TDigits, TDecimals\>](/reference/runtime/qsys-runtime/fixed-decimal-array-in-ds-3.html)) | Casting operator to decimal[]. Returns a copy of the array as a decimal[].
| [Sort](#void-sortbool-ascending-int-start-int-length)([Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Sorts a range of elements in the array in ascending or descending order.

### void Clear()

Sets all array elements to 0.

```cs
void Clear()
```

### void CopyFrom([Decimal\[\] sourceArray](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [int targetStartAt](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Copies elements from a decimal[] into this array.

```cs
void CopyFrom(Decimal[] sourceArray, int targetStartAt)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Decimal\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | sourceArray | The array to copy from.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetStartAt | The index in this array where the copying should start.

### IEnumerator<FixedDecimal<TDigits, TDecimals>> GetEnumerator()

Returns an enumerator that iterates through the array.

```cs
IEnumerator<FixedDecimal<TDigits, TDecimals>> GetEnumerator()
```

### int GetStartingPosition([int index](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Gets the starting position in the DataStructure buffer of the element indicated by the index parameter.

```cs
int GetStartingPosition(int index)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | index | The index of the desired element.

#### Returns

| Type | Description
| --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | The position in the buffer of the element at the given index.

### Decimal\[\] op_Explicit([FixedDecimalArrayInDS\<TDim, TDigits, TDecimals\> array](/reference/runtime/qsys-runtime/fixed-decimal-array-in-ds-3.html))

Casting operator to decimal[]. Returns a copy of the array as a decimal[].

```cs
Decimal[] op_Explicit(FixedDecimalArrayInDS<TDim, TDigits, TDecimals> array)
```

### void Sort([bool ascending](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [int start](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int length](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Sorts a range of elements in the array in ascending or descending order.

```cs
void Sort(bool ascending, int start, int length)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | ascending | True (default) for ascending.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | start | The starting index of the range to sort. Default is 0.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | length | The number of elements in the range to sort. Default is -1, which means sort all elements.
