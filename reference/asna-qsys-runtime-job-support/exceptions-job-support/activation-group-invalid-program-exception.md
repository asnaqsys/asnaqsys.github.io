---
title: ActivationGroupInvalidProgramException Class
---

The exception that is thrown when an activation could not be created because the program is invalid.

**Namespace:** ASNA.QSys.Runtime.JobSupport <br/>
**Assembly:** ASNA.QSys.Runtime

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception) --> [JobFrameworkException](/reference/asna-qsys-runtime-job-support/exceptions-job-support/job-framework-exception.html) --> ActivationGroupInvalidProgramException

<br>
<br>

## Remarks

The exception that is thrown when an activation could not be created because the program is invalid.

[//]: # ($$TODO: Complete the Remarks section.)

<br>
<br>

## Constructor

| Name |  Description 
| --- | --- 
| **ActivationGroupInvalidProgramException**( [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) ) | Initializes a new instance of the ActivationGroupInvalidProgram exception class.

<br>

### ActivationGroupInvalidProgramException( [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) )

Initializes a new instance of the ActivationGroupInvalidProgram exception class.

```cs
ActivationGroupInvalidProgramException( String program, String cause );
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | program | The class name of the program being called. 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | cause | The reason the program is invalid. 

<br>


<br>
<br>

## Properties

| Type | Name | Description | Indexer
| --- | --- | --- | --- 
| [IDictionary](https://docs.microsoft.com/en-us/dotnet/api/system.collections.generic.idictionary-2) | Data | Gets a collection of key/value pairs that provide additional user-defined information about the exception.<br>(Inherited from [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception)) | 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | HelpLink | Gets or sets a link to the help file associated with this exception.<br>(Inherited from [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception)) | 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | HResult | Gets or sets HRESULT, a coded numerical value that is assigned to a specific exception.<br>(Inherited from [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception)) | 
| [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception) | InnerException | Gets the Exception instance that caused the current exception.<br>(Inherited from [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception)) | 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | Message | Gets a message that describes the current exception.<br>(Inherited from [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception)) | 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | Source | Gets or sets the name of the application or the object that causes the error.<br>(Inherited from [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception)) | 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | StackTrace | Gets a string representation of the immediate frames on the call stack.<br>(Inherited from [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception)) | 
| [MethodBase]($$TODO-MethodBase.html) | TargetSite | Gets the method that throws the current exception.<br>(Inherited from [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception)) | 

<br>
<br>

## Methods

| Type | Name | Description | Return Description 
| --- | --- | --- | --- 
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | [Equals](https://docs.microsoft.com/en-us/dotnet/api/system.object.equals)([Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | Determines whether the specified object is equal to the current object.<br>(Inherited from [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | true if the specified object is equal to the current object; otherwise, false.
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [Finalize](https://docs.microsoft.com/en-us/dotnet/api/system.object.finalize)() | Allows an object to try to free resources and perform other cleanup operations before it is reclaimed by garbage collection.<br>(Inherited from [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | 
| [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception) | [GetBaseException]($$TODO-System.Exception.html#getbaseexception)() | When overridden in a derived class, returns the Exception that is the root cause of one or more subsequent exceptions.<br>(Inherited from [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception)) | 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | [GetHashCode](https://docs.microsoft.com/en-us/dotnet/api/system.object.gethashcode)() | Serves as the default hash function.<br>(Inherited from [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | A hash code for the current object.
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [GetObjectData]($$TODO-System.Exception.html#getobjectdata)([SerializationInfo]($$TODO-SerializationInfo.html), [StreamingContext]($$TODO-StreamingContext.html)) | When overridden in a derived class, sets the SerializationInfo with information about the exception.<br>(Inherited from [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception)) | 
| [Type](https://docs.microsoft.com/en-us/dotnet/api/system.type) | [GetType](https://docs.microsoft.com/en-us/dotnet/api/system.object.gettype)() | Gets the Type of the current instance.<br>(Inherited from [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | The exact runtime type of the current instance.
| [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) | [MemberwiseClone](https://docs.microsoft.com/en-us/dotnet/api/system.object.memberwiseclone)() | Creates a shallow copy of the current Object.<br>(Inherited from [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | A shallow copy of the current Object.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | [ReferenceEquals](https://docs.microsoft.com/en-us/dotnet/api/system.object.referenceequals)([Object](https://docs.microsoft.com/en-us/dotnet/api/system.object), [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | Determines whether the specified Object instances are the same instance.<br>(Inherited from [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | true if objA is the same instance as objB or if both are null; otherwise, false.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | [ToString](https://docs.microsoft.com/en-us/dotnet/api/system.object.tostring)() | Returns a string that represents the current object.<br>(Inherited from [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | A string that represents the current object.

<br>
<br>

