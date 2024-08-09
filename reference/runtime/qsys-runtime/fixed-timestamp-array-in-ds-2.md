---
title: "FixedTimestampArrayInDS<T1, T2> struct"
description: "Describes a fixed size array of FixedTimestamp contained in a DataStructure. "
last_modified_at: 2024-08-09T17:25:29Z
---

Describes a fixed size array of FixedTimestamp contained in a DataStructure.

**Namespace:** ASNA.QSys.Runtime
**Assembly:** ASNA.QSys.Runtime.dll

<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [FixedTimestampArrayInDS](#fixedtimestamparrayindsdatastructure-int32-int32)([DataStructure](/reference/runtime/qsys-runtime/data-structure.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Constructs a fixed size array of FixedTimestamp in a Data Structure.
| [FixedTimestampArrayInDS](#fixedtimestamparrayindsmultidatastructure-int32-int32)([MultiDataStructure](/reference/runtime/qsys-runtime/multi-data-structure.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Constructs a fixed size array of FixedTimestamp in a Multiple Occurrence Data Structure.

### FixedTimestampArrayInDS([DataStructure](/reference/runtime/qsys-runtime/data-structure.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

Constructs a fixed size array of FixedTimestamp in a Data Structure.

```cs
FixedTimestampArrayInDS(DataStructure, Int32, Int32)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DataStructure](/reference/runtime/qsys-runtime/data-structure.html) | parent | The DataStructure containing this array of FixedTimestamp.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | startPos | The starting position of the array within the DataStructure buffer.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | skipPositions | For non-contiguous arrays, the number of position between two consecutive array elements.

### FixedTimestampArrayInDS([MultiDataStructure](/reference/runtime/qsys-runtime/multi-data-structure.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

Constructs a fixed size array of FixedTimestamp in a Multiple Occurrence Data Structure.

```cs
FixedTimestampArrayInDS(MultiDataStructure, Int32, Int32)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [MultiDataStructure](/reference/runtime/qsys-runtime/multi-data-structure.html) | parent | The MultiDataStructure containing this array of FixedTimestamp.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | startPos | The starting position of the array within the DataStructure buffer.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | skipPositions | For non-contiguous arrays, the number of position between two consecutive array elements.

## Properties

| Type | Name | Description
| --- | --- | --- 
| [FixedTimestamp\<TSeparator\>](/reference/runtime/qsys-runtime/fixed-timestamp-1.html) | Item | Indexer over the array, gets or sets the FixedTimestamp element at that position. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | Length | Gets the total number of elements in the array. |
| [DataStructure](/reference/runtime/qsys-runtime/data-structure.html) | ParentDS | Gets the Data Structure to which this field belongs. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | SkipPositions | For non-contiguous arrays, gets the number of buffer positions between consecutive array elements. 0 otherwise. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | StartPosition | Gets the Data Structure buffer position where this array starts. |

## Methods

| Signature | Description |
| --- | --- |
| [Clear()](#void-clear) | Sets all array elements to the Timestamp default value.
| [CopyFrom](#void-copyfromdatetime--sourcearray-int-targetstartat)([DateTime\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Copies elements from a DateTime[] into this array.
| [GetEnumerator()](#ienumerator-fixedtimestamp-tseparator--getenumerator) | Returns an enumerator that iterates through the array.
| [GetStartingPosition](#int-getstartingpositionint-index)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Gets the starting position in the DataStructure buffer of the element indicated by the index parameter.
| [op_Explicit](#datetime--op-explicitfixedtimestamparrayinds-tdim-tseparator-array)([FixedTimestampArrayInDS\<TDim, TSeparator\>](/reference/runtime/qsys-runtime/fixed-timestamp-array-in-ds-2.html)) | Casting operator to DateTime[]. Returns a copy of the array as a DateTime[].
| [op_Implicit](#fixedtimestamparray-tdim-tseparator-op-implicitfixedtimestamparrayinds-tdim-tseparator-array)([FixedTimestampArrayInDS\<TDim, TSeparator\>](/reference/runtime/qsys-runtime/fixed-timestamp-array-in-ds-2.html)) | Casting operator to FixedTimestampArray. Returns a copy of the array as a FixedTimestampArray.
| [Sort](#void-sortbool-ascending-int-start-int-length)([Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Sorts a range of elements in the array in ascending or descending order.

### void Clear()

Sets all array elements to the Timestamp default value.

```cs
void Clear()
```

### void CopyFrom([DateTime\[\] sourceArray](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [int targetStartAt](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Copies elements from a DateTime[] into this array.

```cs
void CopyFrom(DateTime[] sourceArray, int targetStartAt)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DateTime\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | sourceArray | The array to copy from.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetStartAt | The index in this array where the copying should start.

### IEnumerator<FixedTimestamp<TSeparator>> GetEnumerator()

Returns an enumerator that iterates through the array.

```cs
IEnumerator<FixedTimestamp<TSeparator>> GetEnumerator()
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

### DateTime\[\] op_Explicit([FixedTimestampArrayInDS\<TDim, TSeparator\> array](/reference/runtime/qsys-runtime/fixed-timestamp-array-in-ds-2.html))

Casting operator to DateTime[]. Returns a copy of the array as a DateTime[].

```cs
DateTime[] op_Explicit(FixedTimestampArrayInDS<TDim, TSeparator> array)
```

### FixedTimestampArray\<TDim, TSeparator\> op_Implicit([FixedTimestampArrayInDS\<TDim, TSeparator\> array](/reference/runtime/qsys-runtime/fixed-timestamp-array-in-ds-2.html))

Casting operator to FixedTimestampArray. Returns a copy of the array as a FixedTimestampArray.

```cs
FixedTimestampArray<TDim, TSeparator> op_Implicit(FixedTimestampArrayInDS<TDim, TSeparator> array)
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
