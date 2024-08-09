---
title: "CharArray<T> struct           | QSYS API Reference Guide"
description: "Represents a unidimensional fixed-size array of characters. "
last_modified_at: 2024-08-09T16:18:25Z
---

Represents a unidimensional fixed-size array of characters.

**Namespace:** ASNA.QSys.Runtime
**Assembly:** ASNA.QSys.Runtime.dll

<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [CharArray](#chararraychar)([Char\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.char)) | Initializes a CharArray out of an array of char elements.

### CharArray([Char\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.char))

Initializes a CharArray out of an array of char elements.

```cs
CharArray(Char[])
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Char\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.char) | array | The array of char elements

## Properties

| Type | Name | Description
| --- | --- | --- 
| [Char\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.char) | Array | Gets the array that holds the values of the CharArray. |
| [Char](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/char) | Item | Indexer over the array, gets or sets the element at that position. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | Length | Gets the number of elements in the CharArray. |

## Methods

| Signature | Description |
| --- | --- |
| [Clear()](#void-clear) | Clears all elements of the array to their default value.
| [CopyFrom](#void-copyfromchar--sourcearray-int-targetstartat)([Char\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.char), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Copy elements of a char[] into this array, starting at the given position.
| [GetEnumerator()](#ienumerator-char-getenumerator) | Get an IEnumerator to iterate over the elements of the array.
| [Sort](#void-sortbool-ascending-int-start-int-length)([Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Order elements of the array according to their value.

### void Clear()

Clears all elements of the array to their default value.

```cs
void Clear()
```

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

### IEnumerator<char> GetEnumerator()

Get an IEnumerator to iterate over the elements of the array.

```cs
IEnumerator<char> GetEnumerator()
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
