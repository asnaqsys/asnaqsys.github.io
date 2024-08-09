---
title: "CharArrayInDS<T> struct       | QSYS API Reference Guide"
description: "Describes a fixed size array of characters contained in a DataStructure. "
last_modified_at: 2024-08-09T16:18:25Z
---

Describes a fixed size array of characters contained in a DataStructure.

**Namespace:** ASNA.QSys.Runtime
**Assembly:** ASNA.QSys.Runtime.dll

<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [CharArrayInDS](#chararrayindsdatastructure-int32-int32)([DataStructure](/reference/runtime/qsys-runtime/data-structure.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Constructs a fixed size array of characters in a Data Structure.
| [CharArrayInDS](#chararrayindsmultidatastructure-int32-int32)([MultiDataStructure](/reference/runtime/qsys-runtime/multi-data-structure.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Constructs a fixed size array of characters in a Multiple Occurrence Data Structure.

### CharArrayInDS([DataStructure](/reference/runtime/qsys-runtime/data-structure.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

Constructs a fixed size array of characters in a Data Structure.

```cs
CharArrayInDS(DataStructure, Int32, Int32)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DataStructure](/reference/runtime/qsys-runtime/data-structure.html) | parent | The DataStructure containing this array of characters.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | startPos | The starting position of the array within the DataStructure buffer.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | skipPositions | For non-contiguous arrays, the number of position between two consecutive array elements.

### CharArrayInDS([MultiDataStructure](/reference/runtime/qsys-runtime/multi-data-structure.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

Constructs a fixed size array of characters in a Multiple Occurrence Data Structure.

```cs
CharArrayInDS(MultiDataStructure, Int32, Int32)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [MultiDataStructure](/reference/runtime/qsys-runtime/multi-data-structure.html) | parent | The MultiDataStructure containing this array of characters.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | startPos | The starting position of the array within the DataStructure buffer.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | skipPositions | For non-contiguous arrays, the number of position between two consecutive array elements.

## Properties

| Type | Name | Description
| --- | --- | --- 
| [Char](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/char) | Item | Indexer over the array, gets or sets the char element at that position. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | Length | Gets the total number of elements in the array. |
| [DataStructure](/reference/runtime/qsys-runtime/data-structure.html) | ParentDS | Gets the Data Structure to which this field belongs. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | SkipPositions | For non-contiguous arrays, gets the number of buffer positions between consecutive array elements. 0 otherwise. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | StartPosition | Gets the Data Structure buffer position where this array starts. |

## Methods

| Signature | Description |
| --- | --- |
| [Clear()](#void-clear) | Sets all array elements to blank.
| [CopyFrom](#void-copyfromchar--sourcearray-int-targetstartat)([Char\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.char), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Copies elements from a char[] into this array.
| [Equals](#bool-equalsobject-obj)([Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | Equality comparer.
| [GetEnumerator()](#ienumerator-char-getenumerator) | Returns an enumerator that iterates through the array.
| [GetHashCode()](#int-gethashcode) | Computes the hashcode.
| [GetStartingPosition](#int-getstartingpositionint-index)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Gets the starting position in the DataStructure buffer of the element indicated by the index parameter.
| [op_Equality](#bool-op-equalitychararrayinds-tdim-left-chararrayinds-tdim-right)([CharArrayInDS\<TDim\>](/reference/runtime/qsys-runtime/char-array-in-ds-1.html), [CharArrayInDS\<TDim\>](/reference/runtime/qsys-runtime/char-array-in-ds-1.html)) | Operator ==, returns true if the operands are equal.
| [op_Explicit](#char--op-explicitchararrayinds-tdim-array)([CharArrayInDS\<TDim\>](/reference/runtime/qsys-runtime/char-array-in-ds-1.html)) | Casting operator to char[]. Returns a copy of the array as a char[].
| [op_Inequality](#bool-op-inequalitychararrayinds-tdim-left-chararrayinds-tdim-right)([CharArrayInDS\<TDim\>](/reference/runtime/qsys-runtime/char-array-in-ds-1.html), [CharArrayInDS\<TDim\>](/reference/runtime/qsys-runtime/char-array-in-ds-1.html)) | Operator !=, returns true if the operands are not equal.
| [Sort](#void-sortbool-ascending-int-start-int-length)([Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Sorts a range of elements in the array in ascending or descending order.
| [To()](#char--to) | Copies the array to a char[]. 

### void Clear()

Sets all array elements to blank.

```cs
void Clear()
```

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

### bool Equals([object obj](https://docs.microsoft.com/en-us/dotnet/api/system.object))

Equality comparer.

```cs
bool Equals(object obj)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) | obj | Object to compare against.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | True in obj is an array of characters and the corresponding elements are equal.

### IEnumerator<char> GetEnumerator()

Returns an enumerator that iterates through the array.

```cs
IEnumerator<char> GetEnumerator()
```

### int GetHashCode()

Computes the hashcode.

```cs
int GetHashCode()
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

### bool op_Equality([CharArrayInDS\<TDim\> left](/reference/runtime/qsys-runtime/char-array-in-ds-1.html), [CharArrayInDS\<TDim\> right](/reference/runtime/qsys-runtime/char-array-in-ds-1.html))

Operator ==, returns true if the operands are equal.

```cs
bool op_Equality(CharArrayInDS<TDim> left, CharArrayInDS<TDim> right)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [CharArrayInDS\<TDim\>](/reference/runtime/qsys-runtime/char-array-in-ds-1.html) | left | Left operand.
| [CharArrayInDS\<TDim\>](/reference/runtime/qsys-runtime/char-array-in-ds-1.html) | right | Right operand.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | True if the operands are equal, false otherwise.

### Char\[\] op_Explicit([CharArrayInDS\<TDim\> array](/reference/runtime/qsys-runtime/char-array-in-ds-1.html))

Casting operator to char[]. Returns a copy of the array as a char[].

```cs
Char[] op_Explicit(CharArrayInDS<TDim> array)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [CharArrayInDS\<TDim\>](/reference/runtime/qsys-runtime/char-array-in-ds-1.html) | array | The array to copy.

#### Returns

| Type | Description
| --- | ---
| [Char\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.char) | 

### bool op_Inequality([CharArrayInDS\<TDim\> left](/reference/runtime/qsys-runtime/char-array-in-ds-1.html), [CharArrayInDS\<TDim\> right](/reference/runtime/qsys-runtime/char-array-in-ds-1.html))

Operator !=, returns true if the operands are not equal.

```cs
bool op_Inequality(CharArrayInDS<TDim> left, CharArrayInDS<TDim> right)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [CharArrayInDS\<TDim\>](/reference/runtime/qsys-runtime/char-array-in-ds-1.html) | left | Left operand.
| [CharArrayInDS\<TDim\>](/reference/runtime/qsys-runtime/char-array-in-ds-1.html) | right | Right operand.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | True if the operands are NOT equal, false otherwise.

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

### Char[] To()

Copies the array to a char[]. 

```cs
Char[] To()
```
