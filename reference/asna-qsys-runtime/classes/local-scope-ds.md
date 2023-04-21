---
title: LocalScopeDS Class
---

Base class that contains functionality to support locally scoped data structures.

**Namespace:** ASNA.QSys.Runtime <br/>
**Assembly:** ASNA.QSys.Runtime

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> LocalScopeDS

<br>
<br>

## Remarks

Locally scoped data structures are defined as a class extending LocalScopeDS. The encapsulated DataStructure object provides the buffer functionality, while properties declared in the derived class access the encapsulated DataStructure.

[//]: # ($$TODO: Complete the Remarks section.)

<br>
<br>

## Constructors

| Name |  Description 
| --- | --- 
| [LocalScopeDS](#localscopedsint32)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Constructs a LocalScopeDS object with a buffer of the given size. 
| [LocalScopeDS](#localscopedsdatastructure)([DataStructure](/reference/asna-qsys-runtime/classes/data-structure.html)) | Constructs a LocalScopeDS object given a DataStructure to use. 

<br>

### LocalScopeDS( [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) )

Constructs a LocalScopeDS object with a buffer of the given size.

```cs
LocalScopeDS( Int32 size );
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | size | Size of the Data Structure buffer. 

<br>

### LocalScopeDS( [DataStructure](/reference/asna-qsys-runtime/classes/data-structure.html) )

Constructs a LocalScopeDS object given a DataStructure to use.

```cs
LocalScopeDS( ASNA.QSys.Runtime.DataStructure ds );
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DataStructure](/reference/asna-qsys-runtime/classes/data-structure.html) | ds | The DataStructure object to use to hold the field values. 

<br>


<br>
<br>

## Properties

| Type | Name | Description | Indexer
| --- | --- | --- | --- 
| [List](https://docs.microsoft.com/en-us/dotnet/api/system.collections.generic.list-1) | BufferDescription | Returns the flat description of the data structure buffer. | 
| [DataStructure](/reference/asna-qsys-runtime/classes/data-structure.html) | DS | Gets or sets the DataStructure object to support the buffer where data is stored. | 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | DSName | Gets the name of this Data Structure object. | 
| [List](https://docs.microsoft.com/en-us/dotnet/api/system.collections.generic.list-1) | Fields | Gets the Layout of this Data Structure. A null return means the DataStructure was defined via buffer length. | 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | Length | Length of the Data Structure buffer. | 

<br>
<br>

## Methods

| Type | Name | Description | Return Description 
| --- | --- | --- | --- 
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [Clear](#clear)() | Clears the Data Structure. If the layout is defined, each field is cleared to its default value. Otherwise it is cleared to blanks. | 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [Dump](#dump)() | Gets the contents of the Data Structure buffer as a string value. | The contents of the Data Structure buffer as a string.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | [Equals](https://docs.microsoft.com/en-us/dotnet/api/system.object.equals)([Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | Determines whether the specified object is equal to the current object.<br>(Inherited from [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | true if the specified object is equal to the current object; otherwise, false.
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [Finalize](https://docs.microsoft.com/en-us/dotnet/api/system.object.finalize)() | Allows an object to try to free resources and perform other cleanup operations before it is reclaimed by garbage collection.<br>(Inherited from [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | [GetHashCode](https://docs.microsoft.com/en-us/dotnet/api/system.object.gethashcode)() | Serves as the default hash function.<br>(Inherited from [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | A hash code for the current object.
| [Type](https://docs.microsoft.com/en-us/dotnet/api/system.type) | [GetType](https://docs.microsoft.com/en-us/dotnet/api/system.object.gettype)() | Gets the Type of the current instance.<br>(Inherited from [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | The exact runtime type of the current instance.
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [Load](#loadstring)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Sets the Data Structure buffer to the given string value, padding with blanks if necessary. | 
| [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) | [MemberwiseClone](https://docs.microsoft.com/en-us/dotnet/api/system.object.memberwiseclone)() | Creates a shallow copy of the current Object.<br>(Inherited from [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | A shallow copy of the current Object.
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [ObjectToParm](#objecttoparmas400program-int32[]-int32)([As400Program]($$TODO-ASNA.DataGate.Client.As400Program.html), [Int32[]](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | IDS.ObjectToParm implementation. Converts the Data Structure field values into parameters for calling the given IBMi program. | 
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [ParmToObject](#parmtoobjectas400program-int32[]-int32)([As400Program]($$TODO-ASNA.DataGate.Client.As400Program.html), [Int32[]](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | IDS.ParmToObject implementation. Gets the Data Structure field values returned from a call to an IBMi program. | 
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | [ReferenceEquals](https://docs.microsoft.com/en-us/dotnet/api/system.object.referenceequals)([Object](https://docs.microsoft.com/en-us/dotnet/api/system.object), [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | Determines whether the specified Object instances are the same instance.<br>(Inherited from [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | true if objA is the same instance as objB or if both are null; otherwise, false.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [ToString](#tostring)() | Gets the contents of the data structure as a string. | A copy of the contents of the data structure as a string.

<br>
<br>

### Clear()

Clears the Data Structure. If the layout is defined, each field is cleared to its default value. Otherwise it is cleared to blanks.

```cs
Clear();
```


<br>
<br>

### Dump()

Gets the contents of the Data Structure buffer as a string value.

```cs
Dump();
```

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

The contents of the Data Structure buffer as a string.


<br>
<br>

### Load([String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Sets the Data Structure buffer to the given string value, padding with blanks if necessary.

```cs
Load(String source);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | source | The string to load into the buffer. 


<br>
<br>

### ObjectToParm([As400Program]($$TODO-ASNA.DataGate.Client.As400Program.html), [Int32[]](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

IDS.ObjectToParm implementation. Converts the Data Structure field values into parameters for calling the given IBMi program.

```cs
ObjectToParm(ASNA.DataGate.Client.As400Program program, Int32[] indices, Int32 dim);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [As400Program]($$TODO-ASNA.DataGate.Client.As400Program.html) | program | As400Program object describing the program call. 
| [Int32[]](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | indices | Array that hold the indices for the current parameter. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | dim | The dimension nesting of the parameter. 


<br>
<br>

### ParmToObject([As400Program]($$TODO-ASNA.DataGate.Client.As400Program.html), [Int32[]](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

IDS.ParmToObject implementation. Gets the Data Structure field values returned from a call to an IBMi program.

```cs
ParmToObject(ASNA.DataGate.Client.As400Program program, Int32[] indices, Int32 dim);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [As400Program]($$TODO-ASNA.DataGate.Client.As400Program.html) | program | As400Program object describing the program call. 
| [Int32[]](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | indices | Array that hold the indices for the current parameter. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | dim | The dimension nesting of the parameter. 


<br>
<br>

### ToString()

Gets the contents of the data structure as a string.

```cs
ToString();
```

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

A copy of the contents of the data structure as a string.


<br>
<br>

