---
title: CallHostSpecs Class
---

Packages the specification of a remote program call command and its parameters.

**Namespace:** ASNA.QSys.Runtime.JobSupport <br/>
**Assembly:** ASNA.QSys.Runtime

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> CallHostSpecs

<br>
<br>

## Remarks

Packages the specification of a remote program call command and its parameters.

[//]: # ($$TODO: Complete the Remarks section.)

<br>
<br>

## Constructor

| Name |  Description 
| --- | --- 
| **CallHostSpecs**( [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) ) | Initializes a new instance of the CallHostSpecs class.

<br>

### CallHostSpecs( [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) )

Initializes a new instance of the CallHostSpecs class.

```cs
CallHostSpecs( String agentContainer, String programName, String parmsConstants, Int32 parmsControlsCount, String formatName, String parmsFormatFields, Int32 maxOutputLength );
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | agentContainer | The library or assembly name containing the program. 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | programName | The name of the program to be called. 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | parmsConstants | The comma separated list of constants to be passed as parameters. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | parmsControlsCount | The number of control values to be passed as parameters. 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatName | The name of a record format whose field values are to be passed as parameters. 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | parmsFormatFields | The comma separated list of fields whose values are to be passed as parameters. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | maxOutputLength | The maximum length expected as a return value from the called program. 

<br>


<br>
<br>

## Properties

| Type | Name | Description | Indexer
| --- | --- | --- | --- 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | FormatName | Gets the name of the record format to use to find the parameters. | 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | LibraryName | Gets the IBM i Library Name or .NET Assembly name where program resides. | 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | MaxOutputLength | Gets the Maximum length of result from program call. | 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | ParmsConstants | Gets the comma separated list of constant parameters to be passed to the program. | 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | ParmsControlsCount | Gets the number of controls used as parameters to be passed to the program. | 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | ParmsFormatFields | Gets the comma separated list of field names whose values in a record format, are used as parameters to be passed to the program. | 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | ProgramName | Gets the Program Name to call. | 

<br>
<br>

## Methods

| Type | Name | Description | Return Description 
| --- | --- | --- | --- 
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | [Equals](https://docs.microsoft.com/en-us/dotnet/api/system.object.equals)([Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | Determines whether the specified object is equal to the current object.<br>(Inherited from [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | true if the specified object is equal to the current object; otherwise, false.
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [Finalize](https://docs.microsoft.com/en-us/dotnet/api/system.object.finalize)() | Allows an object to try to free resources and perform other cleanup operations before it is reclaimed by garbage collection.<br>(Inherited from [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | [GetHashCode](https://docs.microsoft.com/en-us/dotnet/api/system.object.gethashcode)() | Serves as the default hash function.<br>(Inherited from [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | A hash code for the current object.
| [Type](https://docs.microsoft.com/en-us/dotnet/api/system.type) | [GetType](https://docs.microsoft.com/en-us/dotnet/api/system.object.gettype)() | Gets the Type of the current instance.<br>(Inherited from [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | The exact runtime type of the current instance.
| [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) | [MemberwiseClone](https://docs.microsoft.com/en-us/dotnet/api/system.object.memberwiseclone)() | Creates a shallow copy of the current Object.<br>(Inherited from [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | A shallow copy of the current Object.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | [ReferenceEquals](https://docs.microsoft.com/en-us/dotnet/api/system.object.referenceequals)([Object](https://docs.microsoft.com/en-us/dotnet/api/system.object), [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | Determines whether the specified Object instances are the same instance.<br>(Inherited from [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | true if objA is the same instance as objB or if both are null; otherwise, false.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | [ToString](https://docs.microsoft.com/en-us/dotnet/api/system.object.tostring)() | Returns a string that represents the current object.<br>(Inherited from [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | A string that represents the current object.

<br>
<br>

