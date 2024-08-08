---
title: "IDS interface                 | QSYS API Reference Guide"
description: "Defines the basic set of operations for a data structure. "
last_modified_at: 2024-08-08T21:41:46Z
---

Defines the basic set of operations for a data structure.

**Namespace:** ASNA.QSys.Runtime
**Assembly:** ASNA.QSys.Runtime.dll

**Extends:** doesn't extend any other interfaces.
<br>
<br>

## Properties

| Type | Name | Description
| --- | --- | --- 
| [List\<IDSField\>](https://docs.microsoft.com/en-us/dotnet/api/system.collections.generic.list-1) | BufferDescription | Returns the flat description of the data structure buffer. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | DSName | Gets the name of the data structure. |
| [List\<IDSField\>](https://docs.microsoft.com/en-us/dotnet/api/system.collections.generic.list-1) | Fields | Gets the fields composing the data structure. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | Length | Gets the length of the data structure. |

## Methods

| Signature | Description |
| --- | --- |
| [Clear()](#void-clear) | Clears the data structure.
| [Dump()](#string-dump) | Gats the data structure contents as a string.
| [Load](#void-loadstring-source)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Loads the data structure from a string.
| [ObjectToParm](#void-objecttoparmas400program-program-int32--indices-int-dimensions)([As400Program](/reference/datagate/datagate-client/as400-program.html), [Int32\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Converts the Data Structure field values into parameters for calling the given IBMi program.
| [ParmToObject](#void-parmtoobjectas400program-program-int32--indices-int-dimensions)([As400Program](/reference/datagate/datagate-client/as400-program.html), [Int32\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Gets the data structure field values returned from a call to an IBMi program.

### void Clear()

Clears the data structure.

```cs
void Clear()
```

### string Dump()

Gats the data structure contents as a string.

```cs
string Dump()
```

### void Load([string source](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Loads the data structure from a string.

```cs
void Load(string source)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | source | The string to copy into the data structure.

### void ObjectToParm([As400Program program](/reference/datagate/datagate-client/as400-program.html), [Int32\[\] indices](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [int dimensions](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Converts the Data Structure field values into parameters for calling the given IBMi program.

```cs
void ObjectToParm(As400Program program, Int32[] indices, int dimensions)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [As400Program](/reference/datagate/datagate-client/as400-program.html) | program | As400Program object describing the program call.
| [Int32\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | indices | Array that hold the indices for the current parameter.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | dimensions | The dimension nesting of the parameter.

### void ParmToObject([As400Program program](/reference/datagate/datagate-client/as400-program.html), [Int32\[\] indices](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [int dimensions](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Gets the data structure field values returned from a call to an IBMi program.

```cs
void ParmToObject(As400Program program, Int32[] indices, int dimensions)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [As400Program](/reference/datagate/datagate-client/as400-program.html) | program | As400Program object describing the program call.
| [Int32\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | indices | Array that hold the indices for the current parameter.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | dimensions | The dimension nesting of the parameter.
