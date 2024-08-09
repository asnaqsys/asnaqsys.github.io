---
title: "IndicatorArrayInDS<T> struct  | QSYS API Reference Guide"
description: "Describes a fixed size array of Indicators contained in a DataStructure. "
last_modified_at: 2024-08-09T16:18:25Z
---

Describes a fixed size array of Indicators contained in a DataStructure.

**Namespace:** ASNA.QSys.Runtime
**Assembly:** ASNA.QSys.Runtime.dll

<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [IndicatorArrayInDS](#indicatorarrayindsdatastructure-int32-int32)([DataStructure](/reference/runtime/qsys-runtime/data-structure.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Constructs a fixed size array of Indicators in a Data Structure.
| [IndicatorArrayInDS](#indicatorarrayindsmultidatastructure-int32-int32)([MultiDataStructure](/reference/runtime/qsys-runtime/multi-data-structure.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Constructs a fixed size array of Indicators in a Multiple Occurrence Data Structure.

### IndicatorArrayInDS([DataStructure](/reference/runtime/qsys-runtime/data-structure.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

Constructs a fixed size array of Indicators in a Data Structure.

```cs
IndicatorArrayInDS(DataStructure, Int32, Int32)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DataStructure](/reference/runtime/qsys-runtime/data-structure.html) | parent | The DataStructure containing this array of Indicators.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | startPos | The starting position of the array within the DataStructure buffer.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | skipPositions | For non-contiguous arrays, the number of position between two consecutive array elements.

### IndicatorArrayInDS([MultiDataStructure](/reference/runtime/qsys-runtime/multi-data-structure.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

Constructs a fixed size array of Indicators in a Multiple Occurrence Data Structure.

```cs
IndicatorArrayInDS(MultiDataStructure, Int32, Int32)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [MultiDataStructure](/reference/runtime/qsys-runtime/multi-data-structure.html) | parent | The MultiDataStructure containing this array of Indicators.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | startPos | The starting position of the array within the DataStructure buffer.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | skipPositions | For non-contiguous arrays, the number of position between two consecutive array elements.

## Properties

| Type | Name | Description
| --- | --- | --- 
| [Indicator](/reference/runtime/qsys-runtime/indicator.html) | Item | Indexer over the array, gets or sets the Indicator element at that position. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | Length | Gets the total number of elements in the array. |
| [DataStructure](/reference/runtime/qsys-runtime/data-structure.html) | ParentDS | Gets the Data Structure to which this field belongs. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | SkipPositions | For non-contiguous arrays, gets the number of buffer positions between consecutive array elements. 0 otherwise. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | StartPosition | Gets the Data Structure buffer position where this array starts. |

## Methods

| Signature | Description |
| --- | --- |
| [Clear()](#void-clear) | Sets all array elements to '0' (*OFF).
| [CopyFrom](#void-copyfromindicator--sourcearray-int-targetstartat)([Indicator\[\]](/reference/runtime/qsys-runtime/indicator.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Copies elements from an Indicator[] into this array.
| [CopyFrom](#void-copyfromchar--sourcearray-int-targetstartat)([Char\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.char), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Copies elements from a char[] into this array.
| [GetEnumerator()](#ienumerator-indicator-getenumerator) | Returns an enumerator that iterates through the array.
| [GetStartingPosition](#int-getstartingpositionint-index)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Gets the starting position in the DataStructure buffer of the element indicated by the index parameter.
| [op_Explicit](#char--op-explicitindicatorarrayinds-tdim-array)([IndicatorArrayInDS\<TDim\>](/reference/runtime/qsys-runtime/indicator-array-in-ds-1.html)) | Casting operator to char[]. Returns a copy of the array as a char[].
| [op_Implicit](#indicatorarray-tdim-op-implicitindicatorarrayinds-tdim-array)([IndicatorArrayInDS\<TDim\>](/reference/runtime/qsys-runtime/indicator-array-in-ds-1.html)) | Casting operator to IndicatorArray. Returns a copy of the array as an IndicatorArray.
| [Sort](#void-sortbool-ascending-int-start-int-length)([Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Sorts a range of elements in the array in ascending or descending order.

### void Clear()

Sets all array elements to '0' (*OFF).

```cs
void Clear()
```

### void CopyFrom([Indicator\[\] sourceArray](/reference/runtime/qsys-runtime/indicator.html), [int targetStartAt](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Copies elements from an Indicator[] into this array.

```cs
void CopyFrom(Indicator[] sourceArray, int targetStartAt)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Indicator\[\]](/reference/runtime/qsys-runtime/indicator.html) | sourceArray | The array to copy from.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetStartAt | The index in this array where the copying should start.

### void CopyFrom([Char\[\] sourceArray](https://docs.microsoft.com/en-us/dotnet/api/system.char), [int targetStartAt](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Copies elements from a char[] into this array.

```cs
void CopyFrom(Char[] sourceArray, int targetStartAt)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Char\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.char) | sourceArray | The array to copy from.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetStartAt | The index in this array where the copying should start.

### IEnumerator<Indicator> GetEnumerator()

Returns an enumerator that iterates through the array.

```cs
IEnumerator<Indicator> GetEnumerator()
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

### Char\[\] op_Explicit([IndicatorArrayInDS\<TDim\> array](/reference/runtime/qsys-runtime/indicator-array-in-ds-1.html))

Casting operator to char[]. Returns a copy of the array as a char[].

```cs
Char[] op_Explicit(IndicatorArrayInDS<TDim> array)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [IndicatorArrayInDS\<TDim\>](/reference/runtime/qsys-runtime/indicator-array-in-ds-1.html) | array | The array to copy.

#### Returns

| Type | Description
| --- | ---
| [Char\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.char) | 

### IndicatorArray\<TDim\> op_Implicit([IndicatorArrayInDS\<TDim\> array](/reference/runtime/qsys-runtime/indicator-array-in-ds-1.html))

Casting operator to IndicatorArray. Returns a copy of the array as an IndicatorArray.

```cs
IndicatorArray<TDim> op_Implicit(IndicatorArrayInDS<TDim> array)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [IndicatorArrayInDS\<TDim\>](/reference/runtime/qsys-runtime/indicator-array-in-ds-1.html) | array | The array to copy.

#### Returns

| Type | Description
| --- | ---
| [IndicatorArray`1](/reference/runtime/qsys-runtime/indicator-array-1.html) | 

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
