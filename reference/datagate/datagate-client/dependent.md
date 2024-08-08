---
title: "Dependent class               | QSYS API Reference Guide"
description: "The `Dependent` class represents a dependency in the ASNA DataGate environment. "
last_modified_at: 2024-08-08T21:41:32Z
---

The `Dependent` class represents a dependency in the ASNA DataGate environment.

**Namespace:** ASNA.DataGate.Client
**Assembly:** ASNA.QSys.DataGate.Client.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>
## Thread Safety

Any public static (Shared) members of this type are safe for multithreaded operations. Any instance members are not guaranteed to be thread safe.

## Remarks
This class implements the `IEquatable<Dependent>` interface, allowing instances of `Dependent` to be compared for equality based on their properties.    /// A `Dependent` instance represents a specific ASNA DataGate object (such as a file or a data area) that a program depends on.
Each `Dependent` has an `AdgObjectType` indicating the type of the ASNA DataGate object it represents, a `DependentType` indicating the type of the dependency, and a `PathName` representing the path name of the ASNA DataGate object.

<br>
<br>

## Properties

| Type | Name | Description
| --- | --- | --- 
| [AdgObjectTypes](/reference/datagate/datagate-common/adg-object-types.html) | AdgObjectType | Gets the type of the ASNA DataGate object that this dependent represents. |
| [DependentTypes](/reference/datagate/datagate-common/dependent-types.html) | DependentType | Gets the type of the dependency that this instance represents. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | PathName | Gets the path name of the ASNA DataGate object that this dependent represents. |

## Methods

| Signature | Description |
| --- | --- |
| [Equals](#bool-equalsdependent-other)([Dependent](/reference/datagate/datagate-client/dependent.html)) | Determines whether the specified  is equal to the current .
| [Equals](#bool-equalsobject-obj)([Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | Determines whether the specified object is equal to the current .
| [GetHashCode()](#int-gethashcode) | Serves as the default hash function.
| [ToString()](#string-tostring) | Returns a string that represents the current object.

### bool Equals([Dependent other](/reference/datagate/datagate-client/dependent.html))

Determines whether the specified  is equal to the current .


#### Remarks
This method checks if the provided  is not null and if its , , and  properties are equal to those of the current instance.The comparison of  is case-insensitive.

```cs
bool Equals(Dependent other)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Dependent](/reference/datagate/datagate-client/dependent.html) | other | The  to compare with the current .

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | true if the specified  is equal to the current ; otherwise, false.

### bool Equals([object obj](https://docs.microsoft.com/en-us/dotnet/api/system.object))

Determines whether the specified object is equal to the current .


#### Remarks
This method overrides the  method.It casts the provided object to a  and calls the  method to perform the comparison.If the cast is unsuccessful (i.e., if the object is not a ), the method returns false.

```cs
bool Equals(object obj)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) | obj | The object to compare with the current .

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | true if the specified object is a  and is equal to the current ; otherwise, false.

### int GetHashCode()

Serves as the default hash function.


#### Remarks
This method overrides the  method.It calculates the hash code for the current instance based on the , , and  properties.The hash code for  is calculated using a case-insensitive method.This hash code will be used when the  instance is used in a hash-based collection, like a hash set or a dictionary.

```cs
int GetHashCode()
```

### string ToString()

Returns a string that represents the current object.


#### Remarks
This method overrides the  method and returns the  property of the current instance.This provides a string representation of the dependent that is the path name of the ASNA DataGate object it represents.

```cs
string ToString()
```
