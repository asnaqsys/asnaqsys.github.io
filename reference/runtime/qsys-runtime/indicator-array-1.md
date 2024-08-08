---
title: "IndicatorArray<T> struct      | QSYS API Reference Guide"
description: "Defines the functionality of a fixed-sized unidimensional array of Indicator elements. "
last_modified_at: 2024-08-08T21:41:46Z
---

Defines the functionality of a fixed-sized unidimensional array of Indicator elements.

**Namespace:** ASNA.QSys.Runtime
**Assembly:** ASNA.QSys.Runtime.dll

<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [IndicatorArray](#indicatorarrayindicator)([Indicator\[\]](/reference/runtime/qsys-runtime/indicator.html)) | Initializes an IndicatorArray using a .Net array of Indicator elements.
| [IndicatorArray](#indicatorarraychar)([Char\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.char)) | Initializes an IndicatorArray using a .Net array of char elements.

### IndicatorArray([Indicator\[\]](/reference/runtime/qsys-runtime/indicator.html))

Initializes an IndicatorArray using a .Net array of Indicator elements.

```cs
IndicatorArray(Indicator[])
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Indicator\[\]](/reference/runtime/qsys-runtime/indicator.html) | array | The Indicator[] obect from which to initialize this IndicatorArray.

### IndicatorArray([Char\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.char))

Initializes an IndicatorArray using a .Net array of char elements.

```cs
IndicatorArray(Char[])
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Char\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.char) | array | The char[] obect from which to initialize this IndicatorArray.

## Properties

| Type | Name | Description
| --- | --- | --- 
| [Indicator\[\]](/reference/runtime/qsys-runtime/indicator.html) | Array | Gets the array that holds the values of the IndicatorArray. |
| [Indicator](/reference/runtime/qsys-runtime/indicator.html) | Item | Indexer over the array, gets or sets the element at that position. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | Length | Gets the number of elements in the IndicatorArray. |

## Methods

| Signature | Description |
| --- | --- |
| [Clear()](#void-clear) | Clears all elements of the array to their default value.
| [CopyFrom](#void-copyfromindicator--sourcearray-int-targetstartat)([Indicator\[\]](/reference/runtime/qsys-runtime/indicator.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Copy elements of a Indicator[] into this array, starting at the given position.
| [CopyFrom](#void-copyfromchar--sourcearray-int-targetstartat)([Char\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.char), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Copy elements of a char[] into this array, starting at the given position.
| [GetEnumerator()](#ienumerator-indicator-getenumerator) | Get an IEnumerator to iterate over the elements of the array.
| [Sort](#void-sortbool-ascending-int-start-int-length)([Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Order elements of the array according to their value.

### void Clear()

Clears all elements of the array to their default value.

```cs
void Clear()
```

### void CopyFrom([Indicator\[\] sourceArray](/reference/runtime/qsys-runtime/indicator.html), [int targetStartAt](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Copy elements of a Indicator[] into this array, starting at the given position.

```cs
void CopyFrom(Indicator[] sourceArray, int targetStartAt)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Indicator\[\]](/reference/runtime/qsys-runtime/indicator.html) | sourceArray | The array from where to copy.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetStartAt | The starting index in this array. Default is 0.

### void CopyFrom([Char\[\] sourceArray](https://docs.microsoft.com/en-us/dotnet/api/system.char), [int targetStartAt](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Copy elements of a char[] into this array, starting at the given position.

```cs
void CopyFrom(Char[] sourceArray, int targetStartAt)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Char\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.char) | sourceArray | The array from where to copy.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetStartAt | The starting index in this array. Default is 0.

### IEnumerator<Indicator> GetEnumerator()

Get an IEnumerator to iterate over the elements of the array.

```cs
IEnumerator<Indicator> GetEnumerator()
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
