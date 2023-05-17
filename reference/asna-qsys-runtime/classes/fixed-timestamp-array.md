---
title: FixedTimestampArray`2 Class
---

Defines the functionality of a fixed-sized unidimensional array of FixedTimestamp elements.

**Namespace:** ASNA.QSys.Runtime <br/>
**Assembly:** ASNA.QSys.Runtime

<br>
<br>

## Remarks

Defines the functionality of a fixed-sized unidimensional array of FixedTimestamp elements.

[//]: # ($$TODO: Complete the Remarks section.)

<br>
<br>

## Constructors

| Name |  Description 
| --- | --- 
| [FixedTimestampArray](#fixedtimestamparrayfixedtimestamp{`1}[])([FixedTimestamp{\\`1}[]](/reference/asna-qsys-runtime/fixed-timestamp{`1}.html)) | Initializes a FixedTimestampArray out of an array of FixedTimestamp elements. 
| [FixedTimestampArray](#fixedtimestamparraydatetime[])([DateTime[]](https://docs.microsoft.com/en-us/dotnet/api/system.datetime)) | Initializes a FixedTimestampArray out of an array of System.DateTime elements. 

<br>

### FixedTimestampArray( [FixedTimestamp{\\`1}[]](/reference/asna-qsys-runtime/fixed-timestamp{`1}.html) )

Initializes a FixedTimestampArray out of an array of FixedTimestamp elements.

```cs
FixedTimestampArray( ASNA.QSys.Runtime.FixedTimestamp{`1}[] array );
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [FixedTimestamp{\\`1}[]](/reference/asna-qsys-runtime/fixed-timestamp{`1}.html) | array | The array of FixedTimestamp elements. 

<br>

### FixedTimestampArray( [DateTime[]](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) )

Initializes a FixedTimestampArray out of an array of System.DateTime elements.

```cs
FixedTimestampArray( DateTime[] array );
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DateTime[]](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | array | The array of System.DateTime elements. 

<br>


<br>
<br>

## Properties

| Type | Name | Description | Indexer
| --- | --- | --- | --- 
| [FixedTimestamp\\`1[]]($$TODO-FixedTimestamp`1[].html) | Array | Gets the array that holds the values of the FixedTimestampArray. | 
| [FixedTimestamp\\`1]($$TODO-FixedTimestamp`1.html) | Item([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Indexer over the array, gets or sets the element at that position. | index /* Index of the desired element. */
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | Length | Gets the number of elements in the FixedTimestampArray. | 

<br>
<br>

## Methods

| Type | Name | Description | Return Description 
| --- | --- | --- | --- 
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [Clear](#clear)() | Clears all elements of the array to their default value. | 
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [CopyFrom](#copyfromfixedtimestamp{`1}[]-int32)([FixedTimestamp{\\`1}[]](/reference/asna-qsys-runtime/fixed-timestamp{`1}.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Copy elements of a FixedTimestamp[] into this array, starting at the given position. | 
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [CopyFrom](#copyfromdatetime[]-int32)([DateTime[]](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Copy elements of a DateTime[] into this array, starting at the given position. | 
| [IEnumerator\\`1]($$TODO-IEnumerator`1.html) | [GetEnumerator](#getenumerator)() | Get an IEnumerator to iterate over the elements of the array. | The IEnumerator object.
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [Sort](#sortboolean-int32-int32)([Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Order elements of the array according to their value. | 

<br>
<br>

### Clear()

Clears all elements of the array to their default value.

```cs
Clear();
```


<br>
<br>

### CopyFrom([FixedTimestamp{\\`1}[]](/reference/asna-qsys-runtime/fixed-timestamp{`1}.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

Copy elements of a FixedTimestamp[] into this array, starting at the given position.

```cs
CopyFrom(ASNA.QSys.Runtime.FixedTimestamp{`1}[] sourceArray, Int32 targetStartAt);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [FixedTimestamp{\\`1}[]](/reference/asna-qsys-runtime/fixed-timestamp{`1}.html) | sourceArray | The array from where to copy. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetStartAt | The starting index in this array. Default is 0. 


<br>
<br>

### CopyFrom([DateTime[]](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

Copy elements of a DateTime[] into this array, starting at the given position.

```cs
CopyFrom(DateTime[] sourceArray, Int32 targetStartAt);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DateTime[]](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | sourceArray | The array from where to copy. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetStartAt | The starting index in this array. Default is 0. 


<br>
<br>

### GetEnumerator()

Get an IEnumerator to iterate over the elements of the array.

```cs
GetEnumerator();
```

#### Returns

[IEnumerator\\`1]($$TODO-IEnumerator`1.html)

The IEnumerator object.


<br>
<br>

### Sort([Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

Order elements of the array according to their value.

```cs
Sort(Boolean ascending, Int32 start, Int32 length);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | ascending | True for ascending order. Default is true. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | start | Index of the element where the sort starts. Default is 0. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | length | How many elements to sort. Default is -1, sort the whole array. 


<br>
<br>
