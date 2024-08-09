---
title: "FixedStringArray<T1, T2> struct"
description: "Defines the functionality of a fixed-sized unidimensional array of FixedString elements. "
last_modified_at: 2024-08-09T16:18:25Z
---

Defines the functionality of a fixed-sized unidimensional array of FixedString elements.

**Namespace:** ASNA.QSys.Runtime
**Assembly:** ASNA.QSys.Runtime.dll

<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [FixedStringArray](#fixedstringarraystring)([String\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Initializes a FixedStringArray out of an array of string elements.

### FixedStringArray([String\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Initializes a FixedStringArray out of an array of string elements.

```cs
FixedStringArray(String[])
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.string) | array | The array of string elements.

## Properties

| Type | Name | Description
| --- | --- | --- 
| [FixedString`1\[\]](/reference/runtime/qsys-runtime/fixed-string-1.html) | Array | Gets the array that holds the values of the FixedStringArray. |
| [FixedString\<TLen\>](/reference/runtime/qsys-runtime/fixed-string-1.html) | Item | Indexer over the array, gets or sets the element at that position. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | Length | Gets the number of elements in the FixedStringArray. |

## Methods

| Signature | Description |
| --- | --- |
| [Clear()](#void-clear) | Clears all elements of the array to their default value. Set each element of the array to blanks.
| [CopyFrom](#void-copyfromstring--sourcearray-int-targetstartat)([String\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Copy elements of a string[] into this array, starting at the given position.
| [GetEnumerator()](#ienumerator-fixedstring-tlen--getenumerator) | Get an IEnumerator to iterate over the elements of the array.
| [Sort](#void-sortbool-ascending-int-start-int-length)([Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Order elements of the array lexicographically according to their value.

### void Clear()

Clears all elements of the array to their default value. Set each element of the array to blanks.

```cs
void Clear()
```

### void CopyFrom([String\[\] sourceArray](https://docs.microsoft.com/en-us/dotnet/api/system.string), [int targetStartAt](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Copy elements of a string[] into this array, starting at the given position.

```cs
void CopyFrom(String[] sourceArray, int targetStartAt)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.string) | sourceArray | The array from where to copy.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetStartAt | The starting index in this array. Default is 0.

### IEnumerator<FixedString<TLen>> GetEnumerator()

Get an IEnumerator to iterate over the elements of the array.

```cs
IEnumerator<FixedString<TLen>> GetEnumerator()
```

### void Sort([bool ascending](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [int start](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int length](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Order elements of the array lexicographically according to their value.

```cs
void Sort(bool ascending, int start, int length)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | ascending | True for ascending order. Default is true.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | start | Index of the element where the sort starts. Default is 0.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | length | How many elements to sort. Default is -1, sort the whole array.
