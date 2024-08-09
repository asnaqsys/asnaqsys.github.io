---
title: "FixedArray<T1, T2> struct     | QSYS API Reference Guide"
description: "Defines the functionality of a fixed-sized unidimensional array. "
last_modified_at: 2024-08-09T17:25:29Z
---

Defines the functionality of a fixed-sized unidimensional array.

**Namespace:** ASNA.QSys.Runtime
**Assembly:** ASNA.QSys.Runtime.dll

<br>
<br>

## Properties

| Type | Name | Description
| --- | --- | --- 
| [T\[\]](https://learn.microsoft.com/en-us/dotnet/api/system.type?view=net-8.0) | Array | Gets the array that holds the T elements of the FixedArray. |
| [T](https://learn.microsoft.com/en-us/dotnet/api/system.type?view=net-8.0) | Item | Indexer over the array, gets or sets the element at that position. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | Length | Gets the number of elements in the FixedArray. |
| [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) | ValueAsObject | Gets a copy of the array that holds the T elements, as an object. |

## Methods

| Signature | Description |
| --- | --- |
| [Clear()](#void-clear) | Clears all elements of the array to their default value.
| [CompareTo](#int-comparetoobject-obj)([Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | Compare To object. 
| [CopyFrom](#void-copyfromt--sourcearray-int-targetstartat)([T\[\]](https://learn.microsoft.com/en-us/dotnet/api/system.type?view=net-8.0), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Copy elements of a T[] into this array, starting at the given position.
| [GetEnumerator()](#ienumerator-t-getenumerator) | Get an IEnumerator to iterate over the elements of the array.
| [Initialize](#void-initializet-val)([T](https://learn.microsoft.com/en-us/dotnet/api/system.type?view=net-8.0)) | Initializes all elements of the array to the given value.
| [op_Explicit](#t--op-explicitfixedarray-tdim-t-fixedarray)([FixedArray\<TDim, T\>](/reference/runtime/qsys-runtime/fixed-array-2.html)) | Explicit cast from FixedArray to T[]
| [op_Implicit](#fixedarray-tdim-t-op-implicitt--array)([T\[\]](https://learn.microsoft.com/en-us/dotnet/api/system.type?view=net-8.0)) | Implicit cast from T[] to FixedArray.
| [Sort](#void-sortbool-ascending-int-start-int-length)([Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Order elements of the array according to their value, using the default comparison for type T.

### void Clear()

Clears all elements of the array to their default value.

```cs
void Clear()
```

### int CompareTo([object obj](https://docs.microsoft.com/en-us/dotnet/api/system.object))

Compare To object. 

```cs
int CompareTo(object obj)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) | obj | Object to compare.

#### Returns

| Type | Description
| --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | A 32-bit signed integer that indicates whether this instance precedes, follows, or appears in the same position in the sort order as the obj parameter.

### void CopyFrom([T\[\] sourceArray](https://learn.microsoft.com/en-us/dotnet/api/system.type?view=net-8.0), [int targetStartAt](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Copy elements of a T[] into this array, starting at the given position.

```cs
void CopyFrom(T[] sourceArray, int targetStartAt)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [T\[\]](https://learn.microsoft.com/en-us/dotnet/api/system.type?view=net-8.0) | sourceArray | The array from where to copy.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetStartAt | The starting index in this array. Default is 0.

### IEnumerator<T> GetEnumerator()

Get an IEnumerator to iterate over the elements of the array.

```cs
IEnumerator<T> GetEnumerator()
```

### void Initialize([T val](https://learn.microsoft.com/en-us/dotnet/api/system.type?view=net-8.0))

Initializes all elements of the array to the given value.

```cs
void Initialize(T val)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [T](https://learn.microsoft.com/en-us/dotnet/api/system.type?view=net-8.0) | val | The value to copy into all array elements.

### T\[\] op_Explicit([FixedArray\<TDim, T\> fixedArray](/reference/runtime/qsys-runtime/fixed-array-2.html))

Explicit cast from FixedArray to T[]

```cs
T[] op_Explicit(FixedArray<TDim, T> fixedArray)
```

### FixedArray\<TDim, T\> op_Implicit([T\[\] array](https://learn.microsoft.com/en-us/dotnet/api/system.type?view=net-8.0))

Implicit cast from T[] to FixedArray.

```cs
FixedArray<TDim, T> op_Implicit(T[] array)
```

### void Sort([bool ascending](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [int start](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int length](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Order elements of the array according to their value, using the default comparison for type T.

```cs
void Sort(bool ascending, int start, int length)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | ascending | True for ascending order. Default is true.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | start | Index of the element where the sort starts. Default is 0.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | length | How many elements to sort. Default is -1, sort the whole array.
