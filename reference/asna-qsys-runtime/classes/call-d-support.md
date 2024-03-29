---
title: CallDSupport Class
---

Provides methods to construct Omissible and Optional parameters for CALLD

**Namespace:** ASNA.QSys.Runtime <br/>
**Assembly:** ASNA.QSys.Runtime

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> CallDSupport

<br>
<br>

## Remarks

Provides methods to construct Omissible and Optional parameters for CALLD

[//]: # ($$TODO: Complete the Remarks section.)

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
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [NewEmptyNoPassOmit&lt;T&gt;](#newemptynopassomit&lt;t&gt;)() | Creates a new NoPassOmit parameter without value. | An empty NoPassOmit object that has no value stored.
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [NewEmptyOmissible&lt;T&gt;](#newemptyomissible&lt;t&gt;)() | Creates a new Omissible parameter without value. | An empty Omissible object that has no value stored.
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [NewEmptyOptional&lt;T&gt;](#newemptyoptional&lt;t&gt;)() | Creates a new Optional parameter without value. | An empty Optional object that has no value stored.
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [NewNoPassOmit&lt;T&gt;](#newnopassomit&lt;t&gt;<t>)([&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics)) | Creates a new NoPassOmit parameter. | A NoPassOmit object with a value.
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [NewOmissible&lt;T&gt;](#newomissible&lt;t&gt;<t>)([&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics)) | Creates a new Omissible parameter. | An Omissible object with a value.
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [NewOptional&lt;T&gt;](#newoptional&lt;t&gt;<t>)([&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics)) | Creates a new Optional parameter. | An Optional object with a value.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | [ReferenceEquals](https://docs.microsoft.com/en-us/dotnet/api/system.object.referenceequals)([Object](https://docs.microsoft.com/en-us/dotnet/api/system.object), [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | Determines whether the specified Object instances are the same instance.<br>(Inherited from [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | true if objA is the same instance as objB or if both are null; otherwise, false.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | [ToString](https://docs.microsoft.com/en-us/dotnet/api/system.object.tostring)() | Returns a string that represents the current object.<br>(Inherited from [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | A string that represents the current object.

<br>
<br>

### NewEmptyNoPassOmit&lt;T&gt;()

Creates a new NoPassOmit parameter without value.

```cs
NewEmptyNoPassOmit<T>();
```


<br>
<br>

### NewEmptyOmissible&lt;T&gt;()

Creates a new Omissible parameter without value.

```cs
NewEmptyOmissible<T>();
```


<br>
<br>

### NewEmptyOptional&lt;T&gt;()

Creates a new Optional parameter without value.

```cs
NewEmptyOptional<T>();
```


<br>
<br>

### NewNoPassOmit&lt;T&gt;([&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics))

Creates a new NoPassOmit parameter.

```cs
NewNoPassOmit<T>(<T> value);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics) | value | The value to store in the NoPassOmit object. 


<br>
<br>

### NewOmissible&lt;T&gt;([&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics))

Creates a new Omissible parameter.

```cs
NewOmissible<T>(<T> value);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics) | value | The value to store in the Omissible object. 


<br>
<br>

### NewOptional&lt;T&gt;([&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics))

Creates a new Optional parameter.

```cs
NewOptional<T>(<T> value);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics) | value | The value to store in the Optional object. 


<br>
<br>

