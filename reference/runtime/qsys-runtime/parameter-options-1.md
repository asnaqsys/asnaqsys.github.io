---
title: "ParameterOptions&lt;T&gt; class"
description: "Represents the base functionality of the special RPG parameters *OMIT and *NOPASS "
last_modified_at: 2024-08-09T17:25:29Z
---

Represents the base functionality of the special RPG parameters *OMIT and *NOPASS

**Namespace:** ASNA.QSys.Runtime
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [ParameterOptions()](#parameteroptions) | Initializes a ParameterOptions object without a value.

### ParameterOptions()

Initializes a ParameterOptions object without a value.

```cs
ParameterOptions()
```

## Properties

| Type | Name | Description
| --- | --- | --- 
| [T](https://learn.microsoft.com/en-us/dotnet/api/system.type?view=net-8.0) | _value | The internal value of the parameter. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | IOPMessage | When overridden in a derived class, gets the message for the exception thrown when this object is being used but hasn't been initialized. |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | IsValid | Returns true if the parameter has a value. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | ToStringMessage | When overridden in a derived class, gets the default value returned by the ToString method when this object is being used but hasn't been initialized. |
| [T](https://learn.microsoft.com/en-us/dotnet/api/system.type?view=net-8.0) | Value | THe value of the parameter. Trying to get the value before the value is set will throw an InvalidOperationException. |

## Methods

| Signature | Description |
| --- | --- |
| [ToString()](#string-tostring) | Get the value as a string.

### string ToString()

Get the value as a string.

```cs
string ToString()
```
