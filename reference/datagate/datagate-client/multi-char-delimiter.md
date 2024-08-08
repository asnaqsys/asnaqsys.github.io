---
title: "MultiCharDelimiter class      | QSYS API Reference Guide"
description: "Represents a delimiter in a data stream. "
last_modified_at: 2024-08-08T21:41:32Z
---

Represents a delimiter in a data stream.

**Namespace:** ASNA.DataGate.Client.CopyData
**Assembly:** ASNA.QSys.DataGate.Client.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [Delimiter](/reference/datagate/datagate-client/delimiter.html)
<br>
<br>

## Remarks
The Delimiter class is used to represent a delimiter in a data stream. It provides a set of static properties that return commonly used delimiters, such as newline, carriage return, and line feed.
It also provides methods and operators for comparing delimiters, converting them to characters and strings, and checking if they represent no delimiter.

<br>
<br>

## Properties

| Type | Name | Description
| --- | --- | --- 
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | Value | Gets or sets the value of this instance. |
| [Char](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/char) | Value | Gets or sets the value of this instance. |

## Methods

| Signature | Description |
| --- | --- |
| [Equals](#bool-equalsobject-obj)([Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | Determines whether the specified object is equal to the current  object.
| [GetHashCode()](#int-gethashcode) | Serves as the default hash function.
| [op_Equality](#bool-op-equalitymultichardelimiter-ldlim-delimiter-rdlim)([MultiCharDelimiter](/reference/datagate/datagate-client/multi-char-delimiter.html), [Delimiter](/reference/datagate/datagate-client/delimiter.html)) | Determines whether a  instance and a  instance are equal.
| [op_Equality](#bool-op-equalitydelimiter-ldlim-multichardelimiter-rdlim)([Delimiter](/reference/datagate/datagate-client/delimiter.html), [MultiCharDelimiter](/reference/datagate/datagate-client/multi-char-delimiter.html)) | Determines whether a  instance and a  instance are equal.
| [op_Inequality](#bool-op-inequalitymultichardelimiter-ldlim-delimiter-rdlim)([MultiCharDelimiter](/reference/datagate/datagate-client/multi-char-delimiter.html), [Delimiter](/reference/datagate/datagate-client/delimiter.html)) | Determines whether a  instance and a  instance are not equal.
| [op_Inequality](#bool-op-inequalitydelimiter-ldlim-multichardelimiter-rdlim)([Delimiter](/reference/datagate/datagate-client/delimiter.html), [MultiCharDelimiter](/reference/datagate/datagate-client/multi-char-delimiter.html)) | Determines whether a  instance and a  instance are not equal.
| [ToString()](#string-tostring) | Returns a string that represents the current  object.

### bool Equals([object obj](https://docs.microsoft.com/en-us/dotnet/api/system.object))

Determines whether the specified object is equal to the current  object.


#### Remarks
This method overrides the base  method and performs a check to determine equality:- If the provided object is a  instance, it compares the string representation of the  instance with the value of the  instance using ordinal string comparison.- If the provided object is not a  instance, it returns false.

```cs
bool Equals(object obj)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) | obj | The object to compare with the current object.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | true if the specified object is equal to the current object; otherwise, false.

### int GetHashCode()

Serves as the default hash function.


#### Remarks
This method overrides the base  method and simply calls the base implementation.The base implementation of  returns a hash code for the current object.

```cs
int GetHashCode()
```

### bool op_Equality([MultiCharDelimiter ldlim](/reference/datagate/datagate-client/multi-char-delimiter.html), [Delimiter rdlim](/reference/datagate/datagate-client/delimiter.html))

Determines whether a  instance and a  instance are equal.


#### Remarks
This operator performs a series of checks to determine equality:- If both instances are null, they are considered equal.- If one instance is null and the other is not, they are considered not equal.- If both instances are not null, it compares the string representation of the  instance with the value of the  instance.

```cs
bool op_Equality(MultiCharDelimiter ldlim, Delimiter rdlim)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [MultiCharDelimiter](/reference/datagate/datagate-client/multi-char-delimiter.html) | ldlim | The  instance to compare.
| [Delimiter](/reference/datagate/datagate-client/delimiter.html) | rdlim | The  instance to compare.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | true if the instances are equal; otherwise, false.

### bool op_Equality([Delimiter ldlim](/reference/datagate/datagate-client/delimiter.html), [MultiCharDelimiter rdlim](/reference/datagate/datagate-client/multi-char-delimiter.html))

Determines whether a  instance and a  instance are equal.


#### Remarks
This operator uses the equality operator (==) of the  class to compare the two instances.The equality comparison is done by comparing the string representation of the  instance with the value of the  instance.

```cs
bool op_Equality(Delimiter ldlim, MultiCharDelimiter rdlim)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Delimiter](/reference/datagate/datagate-client/delimiter.html) | ldlim | The  instance to compare.
| [MultiCharDelimiter](/reference/datagate/datagate-client/multi-char-delimiter.html) | rdlim | The  instance to compare.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | true if the instances are equal; otherwise, false.

### bool op_Inequality([MultiCharDelimiter ldlim](/reference/datagate/datagate-client/multi-char-delimiter.html), [Delimiter rdlim](/reference/datagate/datagate-client/delimiter.html))

Determines whether a  instance and a  instance are not equal.


#### Remarks
This operator is the logical negation of the equality operator (==). It uses the equality operator to compare the two instances and then negates the result.

```cs
bool op_Inequality(MultiCharDelimiter ldlim, Delimiter rdlim)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [MultiCharDelimiter](/reference/datagate/datagate-client/multi-char-delimiter.html) | ldlim | The  instance to compare.
| [Delimiter](/reference/datagate/datagate-client/delimiter.html) | rdlim | The  instance to compare.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | true if the instances are not equal; otherwise, false.

### bool op_Inequality([Delimiter ldlim](/reference/datagate/datagate-client/delimiter.html), [MultiCharDelimiter rdlim](/reference/datagate/datagate-client/multi-char-delimiter.html))

Determines whether a  instance and a  instance are not equal.


#### Remarks
This operator is the logical negation of the equality operator (==). It uses the equality operator to compare the two instances and then negates the result.The equality comparison is done by comparing the string representation of the  instance with the value of the  instance.

```cs
bool op_Inequality(Delimiter ldlim, MultiCharDelimiter rdlim)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Delimiter](/reference/datagate/datagate-client/delimiter.html) | ldlim | The  instance to compare.
| [MultiCharDelimiter](/reference/datagate/datagate-client/multi-char-delimiter.html) | rdlim | The  instance to compare.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | true if the instances are not equal; otherwise, false.

### string ToString()

Returns a string that represents the current  object.


#### Remarks
This method overrides the base  method and returns the value of the  instance.The value is a string that represents the multi-character delimiter.

```cs
string ToString()
```
