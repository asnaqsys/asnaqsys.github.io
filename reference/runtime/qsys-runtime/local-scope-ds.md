---
title: "LocalScopeDS class            | QSYS API Reference Guide"
description: "Base class that contains functionality to support locally scoped data structures. "
last_modified_at: 2024-08-09T17:25:29Z
---

Base class that contains functionality to support locally scoped data structures.

**Namespace:** ASNA.QSys.Runtime
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>

## Remarks
Locally scoped data structures are defined as a class extending LocalScopeDS. The encapsulated DataStructure object provides the buffer functionality,
while properties declared in the derived class access the encapsulated DataStructure.

<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [LocalScopeDS](#localscopedsint32)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Constructs a LocalScopeDS object with a buffer of the given size.
| [LocalScopeDS](#localscopedsdatastructure)([DataStructure](/reference/runtime/qsys-runtime/data-structure.html)) | Constructs a LocalScopeDS object given a DataStructure to use.

### LocalScopeDS([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

Constructs a LocalScopeDS object with a buffer of the given size.

```cs
LocalScopeDS(Int32)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | size | Size of the Data Structure buffer.

### LocalScopeDS([DataStructure](/reference/runtime/qsys-runtime/data-structure.html))

Constructs a LocalScopeDS object given a DataStructure to use.

```cs
LocalScopeDS(DataStructure)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DataStructure](/reference/runtime/qsys-runtime/data-structure.html) | ds | The DataStructure object to use to hold the field values.

## Properties

| Type | Name | Description
| --- | --- | --- 
| [List\<IDSField\>](https://docs.microsoft.com/en-us/dotnet/api/system.collections.generic.list-1) | BufferDescription | Returns the flat description of the data structure buffer. |
| [DataStructure](/reference/runtime/qsys-runtime/data-structure.html) | DS | Gets or sets the DataStructure object to support the buffer where data is stored. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | DSName | Gets the name of this Data Structure object. |
| [List\<IDSField\>](https://docs.microsoft.com/en-us/dotnet/api/system.collections.generic.list-1) | Fields | Gets the Layout of this Data Structure. A null return means the DataStructure was defined via buffer length. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | Length | Length of the Data Structure buffer. |

## Methods

| Signature | Description |
| --- | --- |
| [Clear()](#void-clear) | Clears the Data Structure. If the layout is defined, each field is cleared to its default value. Otherwise it is cleared to blanks.
| [Dump()](#string-dump) | Gets the contents of the Data Structure buffer as a string value.
| [Load](#void-loadstring-source)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Sets the Data Structure buffer to the given string value, padding with blanks if necessary.
| [ObjectToParm](#void-objecttoparmas400program-program-int32--indices-int-dim)([As400Program](/reference/datagate/datagate-client/as400-program.html), [Int32\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | IDS.ObjectToParm implementation. Converts the Data Structure field values into parameters for calling the given IBMi program.
| [op_Explicit](#string-op-explicitlocalscopeds-datastructure)([LocalScopeDS](/reference/runtime/qsys-runtime/local-scope-ds.html)) | Casting operator to string. Returns the data structure as a string.
| [ParmToObject](#void-parmtoobjectas400program-program-int32--indices-int-dim)([As400Program](/reference/datagate/datagate-client/as400-program.html), [Int32\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | IDS.ParmToObject implementation. Gets the Data Structure field values returned from a call to an IBMi program.
| [ToString()](#string-tostring) | Gets the contents of the data structure as a string.

### void Clear()

Clears the Data Structure. If the layout is defined, each field is cleared to its default value. Otherwise it is cleared to blanks.

```cs
void Clear()
```

### string Dump()

Gets the contents of the Data Structure buffer as a string value.

```cs
string Dump()
```

### void Load([string source](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Sets the Data Structure buffer to the given string value, padding with blanks if necessary.

```cs
void Load(string source)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | source | The string to load into the buffer.

### void ObjectToParm([As400Program program](/reference/datagate/datagate-client/as400-program.html), [Int32\[\] indices](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [int dim](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

IDS.ObjectToParm implementation. Converts the Data Structure field values into parameters for calling the given IBMi program.

```cs
void ObjectToParm(As400Program program, Int32[] indices, int dim)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [As400Program](/reference/datagate/datagate-client/as400-program.html) | program | As400Program object describing the program call.
| [Int32\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | indices | Array that hold the indices for the current parameter.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | dim | The dimension nesting of the parameter.

### string op_Explicit([LocalScopeDS dataStructure](/reference/runtime/qsys-runtime/local-scope-ds.html))

Casting operator to string. Returns the data structure as a string.

```cs
string op_Explicit(LocalScopeDS dataStructure)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [LocalScopeDS](/reference/runtime/qsys-runtime/local-scope-ds.html) | dataStructure | Data structure to cast to string.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | 

### void ParmToObject([As400Program program](/reference/datagate/datagate-client/as400-program.html), [Int32\[\] indices](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [int dim](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

IDS.ParmToObject implementation. Gets the Data Structure field values returned from a call to an IBMi program.

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

Gets the contents of the data structure as a string.

```cs
string ToString()
```
