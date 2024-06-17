---
title: FixedTimestampArray<T1, T2> struct
description: Defines the functionality of a fixed-sized unidimensional array of FixedTimestamp elements.
---

Defines the functionality of a fixed-sized unidimensional array of FixedTimestamp elements.

**Namespace:** ASNA.QSys.Runtime
**Assembly:** ASNA.QSys.Runtime.dll

<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [FixedTimestampArray](#fixedtimestamparraydatetime)([DateTime\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.datetime)) | Initializes a FixedTimestampArray out of an array of System.DateTime elements.

### FixedTimestampArray([DateTime\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.datetime))

Initializes a FixedTimestampArray out of an array of System.DateTime elements.

```cs
FixedTimestampArray(DateTime[])
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DateTime\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | array | The array of System.DateTime elements.

## Properties

| Type | Name | Description
| --- | --- | --- 
| [FixedTimestamp`1\[\]](/reference/runtime/qsys-runtime/fixed-timestamp-1.html) | Array | Gets the array that holds the values of the FixedTimestampArray. |
| [FixedTimestamp\<TSeparator\>](/reference/runtime/qsys-runtime/fixed-timestamp-1.html) | Item | Indexer over the array, gets or sets the element at that position. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | Length | Gets the number of elements in the FixedTimestampArray. |

## Methods

| Signature | Description |
| --- | --- |
| [Clear()](#void-clear) | Clears all elements of the array to their default value.
| [CopyFrom](#void-copyfromdatetime--sourcearray-int-targetstartat)([DateTime\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Copy elements of a DateTime[] into this array, starting at the given position.
| [GetEnumerator()](#ienumerator-fixedtimestamp-tseparator--getenumerator) | Get an IEnumerator to iterate over the elements of the array.
| [Sort](#void-sortbool-ascending-int-start-int-length)([Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Order elements of the array according to their value.

### void Clear()

Clears all elements of the array to their default value.

```cs
void Clear()
```

### void CopyFrom([DateTime\[\] sourceArray](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [int targetStartAt](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Copy elements of a DateTime[] into this array, starting at the given position.

```cs
void CopyFrom(DateTime[] sourceArray, int targetStartAt)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DateTime\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | sourceArray | The array from where to copy.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetStartAt | The starting index in this array. Default is 0.

### IEnumerator<FixedTimestamp<TSeparator>> GetEnumerator()

Get an IEnumerator to iterate over the elements of the array.

```cs
IEnumerator<FixedTimestamp<TSeparator>> GetEnumerator()
```

### void Sort([bool ascending](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [int start](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int length](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Order elements of the array according to their value.

```cs
void Sort(bool ascending, int start, int length)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | ascending | True for ascending order. Default is true.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | start | Index of the element where the sort starts. Default is 0.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | length | How many elements to sort. Default is -1, sort the whole array.
