---
title: DataGateException Class
---

DataGate operation on file -filename- caused -datagate exception- exception.

**Namespace:** ASNA.QSys.Runtime <br/>
**Assembly:** ASNA.QSys.Runtime

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception) --> [RuntimeException](/reference/asna-qsys-runtime/exceptions/runtime-exception.html) --> DataGateException

<br>
<br>

## Remarks

DataGate operation on file -filename- caused -datagate exception- exception.

[//]: # ($$TODO: Complete the Remarks section.)

<br>
<br>

## Constructor

| Name |  Description 
| --- | --- 
| **DataGateException**( [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [dgException]($$TODO-ASNA.DataGate.Common.dgException.html) ) | Constructor that takes the -filename- and the Datagate -exception instance- that caused the Exception.

<br>

### DataGateException( [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [dgException]($$TODO-ASNA.DataGate.Common.dgException.html) )

Constructor that takes the -filename- and the Datagate -exception instance- that caused the Exception.

```cs
DataGateException( String FileName, ASNA.DataGate.Common.dgException e );
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | FileName | Filename. 
| [dgException]($$TODO-ASNA.DataGate.Common.dgException.html) | e | Datagate exception. 

<br>


<br>
<br>

## Properties

| Type | Name | Description | Indexer
| --- | --- | --- | --- 
| [IDictionary](https://docs.microsoft.com/en-us/dotnet/api/system.collections.generic.idictionary-2) | Data | Gets a collection of key/value pairs that provide additional user-defined information about the exception.<br>(Inherited from [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception)) | 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | DclFileName | Gets the name of the declared filename that caused the exception. | 
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
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [ToString](#tostring)() | Formats exception using DataGate exception error formatting. | The exception error message indicating the filename and the database operation cause.

<br>
<br>

### ToString()

Formats exception using DataGate exception error formatting.

```cs
ToString();
```

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

The exception error message indicating the filename and the database operation cause.


<br>
<br>

