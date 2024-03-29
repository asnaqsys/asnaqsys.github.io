---
title: RpgTypeExtensions Class
---

RpgTypeExtensions class.

**Namespace:** ASNA.QSys.Runtime <br/>
**Assembly:** ASNA.QSys.Runtime

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> RpgTypeExtensions

<br>
<br>

## Remarks

RpgTypeExtensions class.

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
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [MoveL&lt;T,U,V&gt;](#movel&lt;t,u,v&gt;fixedstring<t-u>-fixeddecimal(<t>-<t>)-boolean)([FixedString&lt;T,U&gt;](/reference/asna-qsys-runtime/fixed-string.html), [FixedDecimal](/reference/asna-qsys-runtime/classes/fixed-decimal.html)([&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics),[&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics)), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | MoveL extension. | Decimal result.
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [MoveR&lt;T,U,V&gt;](#mover&lt;t,u,v&gt;fixedstring<t-u>-fixeddecimal(<t>-<t>)-boolean)([FixedString&lt;T,U&gt;](/reference/asna-qsys-runtime/fixed-string.html), [FixedDecimal](/reference/asna-qsys-runtime/classes/fixed-decimal.html)([&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics),[&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics)), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | MoveR extension. | Decimal result.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | [ReferenceEquals](https://docs.microsoft.com/en-us/dotnet/api/system.object.referenceequals)([Object](https://docs.microsoft.com/en-us/dotnet/api/system.object), [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | Determines whether the specified Object instances are the same instance.<br>(Inherited from [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | true if objA is the same instance as objB or if both are null; otherwise, false.
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | [RemoveDate](#removedatedatetime)([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime)) | RemoveDate extension. | DateTime result.
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | [RemoveTime](#removetimedatetime)([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime)) | RemoveTime extension. | DateTime result.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | [ToString](https://docs.microsoft.com/en-us/dotnet/api/system.object.tostring)() | Returns a string that represents the current object.<br>(Inherited from [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | A string that represents the current object.

<br>
<br>

### MoveL&lt;T,U,V&gt;([FixedString&lt;T,U&gt;](/reference/asna-qsys-runtime/fixed-string.html), [FixedDecimal](/reference/asna-qsys-runtime/classes/fixed-decimal.html)([&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics),[&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics)), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

MoveL extension.

```cs
MoveL<T,U,V>(Runtime.FixedString<T,U> s, Runtime.FixedDecimal(<T>, <T>) decNum, Boolean pad);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [FixedString&lt;T,U&gt;](/reference/asna-qsys-runtime/fixed-string.html) | s | MoveL s param. 
| [FixedDecimal(&lt;T&gt;, &lt;T&gt;)](/reference/asna-qsys-runtime/fixed-decimal.html) | decNum | MoveL decNum param. 
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | pad | MoveL pad param. 


<br>
<br>

### MoveR&lt;T,U,V&gt;([FixedString&lt;T,U&gt;](/reference/asna-qsys-runtime/fixed-string.html), [FixedDecimal](/reference/asna-qsys-runtime/classes/fixed-decimal.html)([&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics),[&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics)), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

MoveR extension.

```cs
MoveR<T,U,V>(Runtime.FixedString<T,U> s, Runtime.FixedDecimal(<T>, <T>) decNum, Boolean pad);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [FixedString&lt;T,U&gt;](/reference/asna-qsys-runtime/fixed-string.html) | s | MoveR s param. 
| [FixedDecimal(&lt;T&gt;, &lt;T&gt;)](/reference/asna-qsys-runtime/fixed-decimal.html) | decNum | MoveR decNum param. 
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | pad | MoveR pad param. 


<br>
<br>

### RemoveDate([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime))

RemoveDate extension.

```cs
RemoveDate(DateTime from);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | from | RemoveDate from param. 

#### Returns

[DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime)

DateTime result.


<br>
<br>

### RemoveTime([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime))

RemoveTime extension.

```cs
RemoveTime(DateTime from);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | from | RemoveTime from param. 

#### Returns

[DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime)

DateTime result.


<br>
<br>

