---
title: "MultiDataStructure class      | QSYS API Reference Guide"
description: "Contains functionality to support multiple occurrence data structures. "
last_modified_at: 2024-08-09T17:25:29Z
---

Contains functionality to support multiple occurrence data structures.

**Namespace:** ASNA.QSys.Runtime
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>

## Remarks
Multiple occurrence data structures encapsulate a collection of data structure objects that provide the buffer functionality. Access to the buffer
is via the class field properties operating on the current occurrence object.

<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [MultiDataStructure](#multidatastructureint32-int32)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Constructs a unidimensional MultiDataStructure object.
| [MultiDataStructure](#multidatastructureint32-ilayout)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [ILayout\[\]](/reference/runtime/qsys-runtime/i-layout.html)) | Constructs a unidimensional MultiDataStructure object.
| [MultiDataStructure](#multidatastructureint32--int32)([Int32\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Constructs a MultiDataStructure object.
| [MultiDataStructure](#multidatastructureint32--ilayout)([Int32\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [ILayout\[\]](/reference/runtime/qsys-runtime/i-layout.html)) | Constructs a MultiDataStructure object.

### MultiDataStructure([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

Constructs a unidimensional MultiDataStructure object.

```cs
MultiDataStructure(Int32, Int32)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | arrayLength | Number of elements in the multi data structure.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | size | Size of the individual data structures.

### MultiDataStructure([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [ILayout\[\]](/reference/runtime/qsys-runtime/i-layout.html))

Constructs a unidimensional MultiDataStructure object.

```cs
MultiDataStructure(Int32, ILayout[])
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | arrayLength | Number of elements in the multi data structure.
| [ILayout\[\]](/reference/runtime/qsys-runtime/i-layout.html) | fields | An ILayout array of field descriptions.

### MultiDataStructure([Int32\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

Constructs a MultiDataStructure object.

```cs
MultiDataStructure(Int32[], Int32)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | arrayLength | Number of elements in all dimensions of the multi data structure.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | size | Size of the individual data structures.

### MultiDataStructure([Int32\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [ILayout\[\]](/reference/runtime/qsys-runtime/i-layout.html))

Constructs a MultiDataStructure object.

```cs
MultiDataStructure(Int32[], ILayout[])
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | arrayLength | Number of elements in all dimensions of the multi data structure.
| [ILayout\[\]](/reference/runtime/qsys-runtime/i-layout.html) | fields | An ILayout array of field descriptions.

## Properties

| Type | Name | Description
| --- | --- | --- 
| [Int32\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | ArrayLength | Length of the multi data structure in all dimensions. |
| [List\<IDSField\>](https://docs.microsoft.com/en-us/dotnet/api/system.collections.generic.list-1) | BufferDescription | Returns the flat description of the data structure buffer. |
| [DataStructure](/reference/runtime/qsys-runtime/data-structure.html) | Current | Gets the current occurrence of this multiple occurrence data structure. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | DSName | Gets the name of this multi data structure. |
| [List\<IDSField\>](https://docs.microsoft.com/en-us/dotnet/api/system.collections.generic.list-1) | Fields | Layout of the individual data structures, if it exists. |
| [DataStructure](/reference/runtime/qsys-runtime/data-structure.html) | Item | Gets the DataStructure object at the given index. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | ItemLength | Gets the length of the individual data structures in this MODS. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | Length | Gets the length of the multi occurrence data structure. |
| [Int32\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | Occurrence | Gets the indices of the current occurrence of the multi data structure. |

## Methods

| Signature | Description |
| --- | --- |
| [Clear()](#void-clear) | Clears the current occurrence.
| [ClearAll()](#void-clearall) | Clears all occurrences of the data structure.
| [Dump()](#string-dump) | Gats the contents of the current occurrence as a string.
| [DumpAll()](#string-dumpall) | Gets the contents of all occurrences of the multi data structure as a string.
| [Load](#void-loadstring-source)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Loads the current occurrence from a string.
| [LoadAll](#void-loadallstring-source)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Copies the given string into the multi-occurrence data structure. 
| [ObjectToParm](#void-objecttoparmas400program-program-int32--indices-int-dim)([As400Program](/reference/datagate/datagate-client/as400-program.html), [Int32\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | IDS.ObjectToParm implementation. Converts the current occurrence field values into parameters for calling the given IBMi program.
| [op_Explicit](#string-op-explicitmultidatastructure-multidatastructure)([MultiDataStructure](/reference/runtime/qsys-runtime/multi-data-structure.html)) | Casting operator to string. Returns the multi-occurrence data structure as a string.
| [op_Implicit](#datastructure-op-implicitmultidatastructure-mods)([MultiDataStructure](/reference/runtime/qsys-runtime/multi-data-structure.html)) | Cast operator to DataStructure. Returns the current occurrence.
| [ParmToObject](#void-parmtoobjectas400program-program-int32--indices-int-dim)([As400Program](/reference/datagate/datagate-client/as400-program.html), [Int32\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | IDS.ParmToObject implementation. Gets the current occurrence field values returned from a call to an IBMi program.
| [ToString()](#string-tostring) | Gets the contents of all occurrences of the multi data structure as a string.

### void Clear()

Clears the current occurrence.

```cs
void Clear()
```

### void ClearAll()

Clears all occurrences of the data structure.

```cs
void ClearAll()
```

### string Dump()

Gats the contents of the current occurrence as a string.

```cs
string Dump()
```

### string DumpAll()

Gets the contents of all occurrences of the multi data structure as a string.

```cs
string DumpAll()
```

### void Load([string source](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Loads the current occurrence from a string.

```cs
void Load(string source)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | source | The string to copy into the current occurrence.

### void LoadAll([string source](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Copies the given string into the multi-occurrence data structure. 

```cs
void LoadAll(string source)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | source | The string to copy.

### void ObjectToParm([As400Program program](/reference/datagate/datagate-client/as400-program.html), [Int32\[\] indices](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [int dim](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

IDS.ObjectToParm implementation. Converts the current occurrence field values into parameters for calling the given IBMi program.

```cs
void ObjectToParm(As400Program program, Int32[] indices, int dim)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [As400Program](/reference/datagate/datagate-client/as400-program.html) | program | As400Program object describing the program call.
| [Int32\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | indices | Array that hold the indices for the current parameter.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | dim | The dimension nesting of the parameter.

### string op_Explicit([MultiDataStructure multiDataStructure](/reference/runtime/qsys-runtime/multi-data-structure.html))

Casting operator to string. Returns the multi-occurrence data structure as a string.

```cs
string op_Explicit(MultiDataStructure multiDataStructure)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [MultiDataStructure](/reference/runtime/qsys-runtime/multi-data-structure.html) | multiDataStructure | Multi-occurrence data structure to cast to string.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | 

### DataStructure op_Implicit([MultiDataStructure mods](/reference/runtime/qsys-runtime/multi-data-structure.html))

Cast operator to DataStructure. Returns the current occurrence.

```cs
DataStructure op_Implicit(MultiDataStructure mods)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [MultiDataStructure](/reference/runtime/qsys-runtime/multi-data-structure.html) | mods | The multi data structure.

#### Returns

| Type | Description
| --- | ---
| [DataStructure](/reference/runtime/qsys-runtime/data-structure.html) | 

### void ParmToObject([As400Program program](/reference/datagate/datagate-client/as400-program.html), [Int32\[\] indices](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [int dim](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

IDS.ParmToObject implementation. Gets the current occurrence field values returned from a call to an IBMi program.

```cs
void ParmToObject(As400Program program, Int32[] indices, int dim)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [As400Program](/reference/datagate/datagate-client/as400-program.html) | program | As400Program object describing the program call.
| [Int32\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | indices | Array that hold the indices for the current parameter.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | dim | The dimension nesting of the parameter.

### string ToString()

Gets the contents of all occurrences of the multi data structure as a string.

```cs
string ToString()
```
