---
title: "LocalScopeMultiDS&lt;T&gt; class"
description: "Contains functionality to support locally scoped multiple occurrence data structures. A LocalScopeMultiDS object contains an array of LocalScopeDS obj"
last_modified_at: 2024-08-08T21:41:46Z
---

Contains functionality to support locally scoped multiple occurrence data structures. A LocalScopeMultiDS object contains an array of LocalScopeDS objects.

**Namespace:** ASNA.QSys.Runtime
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>

## Remarks
Locally scoped multiple occurrence data structures encapsulate a collection of LocalScopeDS objects that provide the buffer functionality. Access to the buffer
is via the field properties of the current occurrence object.

<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [LocalScopeMultiDS](#localscopemultidsint32)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Constructs a one-dimensional LocalScopeMultiDS of the given array length.

### LocalScopeMultiDS([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

Constructs a one-dimensional LocalScopeMultiDS of the given array length.

```cs
LocalScopeMultiDS(Int32)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | arrayLength | Length of the LocalScopeMultiDS.

## Properties

| Type | Name | Description
| --- | --- | --- 
| [List\<IDSField\>](https://docs.microsoft.com/en-us/dotnet/api/system.collections.generic.list-1) | BufferDescription | Returns the flat description of the data structure buffer. |
| [T](https://learn.microsoft.com/en-us/dotnet/api/system.type?view=net-8.0) | Current | Gets the current occurrence of this multiple occurrence data structure. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | DSName | Gets the name of the current occurrence. |
| [List\<IDSField\>](https://docs.microsoft.com/en-us/dotnet/api/system.collections.generic.list-1) | Fields | Gets the layout of the current occurrence. |
| [T](https://learn.microsoft.com/en-us/dotnet/api/system.type?view=net-8.0) | Item | Gets the LocalScopeDS object at the given index. |
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
| [ParmToObject](#void-parmtoobjectas400program-program-int32--indices-int-dim)([As400Program](/reference/datagate/datagate-client/as400-program.html), [Int32\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | IDS.ParmToObject implementation. Gets the current occurrence field values returned from a call to an IBMi program.
| [ToString()](#string-tostring) | Gets the contents of all occurrences of the multi data structure as a string.
| [ToT()](#t-tot) | Get the current occurrence.

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

### T ToT()

Get the current occurrence.

```cs
T ToT()
```
