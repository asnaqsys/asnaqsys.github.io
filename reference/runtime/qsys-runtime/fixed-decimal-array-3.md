---
title: "FixedDecimalArray<T1, T2, T3> struct"
description: "Defines the functionality of a fixed-sized unidimensional array of FixedDecimal elements. "
last_modified_at: 2024-08-09T16:18:25Z
---

Defines the functionality of a fixed-sized unidimensional array of FixedDecimal elements.

**Namespace:** ASNA.QSys.Runtime
**Assembly:** ASNA.QSys.Runtime.dll

<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [FixedDecimalArray](#fixeddecimalarraydecimal)([Decimal\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.decimal)) | Initializes a FixedDecimalArray out of an array of decimal elements.

### FixedDecimalArray([Decimal\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.decimal))

Initializes a FixedDecimalArray out of an array of decimal elements.

```cs
FixedDecimalArray(Decimal[])
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Decimal\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | array | The array of decimal elements.

## Properties

| Type | Name | Description
| --- | --- | --- 
| [FixedDecimal`2\[\]](/reference/runtime/qsys-runtime/fixed-decimal-2.html) | Array | Gets the array that holds the values of the FixedDecimalArray. |
| [FixedDecimal\<TDigits, TDecimals\>](/reference/runtime/qsys-runtime/fixed-decimal-2.html) | Item | Indexer over the array, gets or sets the element at that position. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | Length | Gets the number of elements in the FixedDecimalArray. |

## Methods

| Signature | Description |
| --- | --- |
| [Clear()](#void-clear) | Clears all elements of the array to their default value.
| [CopyFrom](#void-copyfromdecimal--sourcearray-int-targetstartat)([Decimal\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Copy elements of a decimal[] into this array, starting at the given position.
| [GetEnumerator()](#ienumerator-fixeddecimal-tdigits-tdecimals--getenumerator) | Get an IEnumerator to iterate over the elements of the array.
| [op_Explicit](#decimal--op-explicitfixeddecimalarray-tdim-tdigits-tdecimals-fixedarray)([FixedDecimalArray\<TDim, TDigits, TDecimals\>](/reference/runtime/qsys-runtime/fixed-decimal-array-3.html)) | Explicit cast from FixedDecimalArray to decimal[]
| [Sort](#void-sortbool-ascending-int-start-int-length)([Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Order elements of the array according to their value.

### void Clear()

Clears all elements of the array to their default value.

```cs
void Clear()
```

### void CopyFrom([Decimal\[\] sourceArray](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [int targetStartAt](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Copy elements of a decimal[] into this array, starting at the given position.

```cs
void CopyFrom(Decimal[] sourceArray, int targetStartAt)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Decimal\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | sourceArray | The array from where to copy.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetStartAt | The starting index in this array. Default is 0.

### IEnumerator<FixedDecimal<TDigits, TDecimals>> GetEnumerator()

Get an IEnumerator to iterate over the elements of the array.

```cs
IEnumerator<FixedDecimal<TDigits, TDecimals>> GetEnumerator()
```

### Decimal\[\] op_Explicit([FixedDecimalArray\<TDim, TDigits, TDecimals\> fixedArray](/reference/runtime/qsys-runtime/fixed-decimal-array-3.html))

Explicit cast from FixedDecimalArray to decimal[]

```cs
Decimal[] op_Explicit(FixedDecimalArray<TDim, TDigits, TDecimals> fixedArray)
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
