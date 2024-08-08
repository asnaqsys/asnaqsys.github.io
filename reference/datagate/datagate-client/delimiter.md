---
title: "Delimiter class               | QSYS API Reference Guide"
description: "Represents a delimiter in a data stream. "
last_modified_at: 2024-08-08T21:41:32Z
---

Represents a delimiter in a data stream.

**Namespace:** ASNA.DataGate.Client.CopyData
**Assembly:** ASNA.QSys.DataGate.Client.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>

## Remarks
The Delimiter class is used to represent a delimiter in a data stream. It provides a set of static properties that return commonly used delimiters, such as newline, carriage return, and line feed.
It also provides methods and operators for comparing delimiters, converting them to characters and strings, and checking if they represent no delimiter.

<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [Delimiter()](#delimiter) | Initializes a new instance of the  class.
| [Delimiter](#delimiterchar)([Char](https://docs.microsoft.com/en-us/dotnet/api/system.char)) | Initializes a new instance of the  class with a specified value.

### Delimiter()

Initializes a new instance of the  class.

```cs
Delimiter()
```

### Delimiter([Char](https://docs.microsoft.com/en-us/dotnet/api/system.char))

Initializes a new instance of the  class with a specified value.

```cs
Delimiter(Char)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Char](https://docs.microsoft.com/en-us/dotnet/api/system.char) | value | The character value to initialize the  instance with.

## Properties

| Type | Name | Description
| --- | --- | --- 
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | IsStarNone | Gets a value indicating whether this instance represents no delimiter. |
| [Delimiter](/reference/datagate/datagate-client/delimiter.html) | NewLine | Constant new line delimiter |
| [Delimiter](/reference/datagate/datagate-client/delimiter.html) | None | Get new Delimiter instance that represents no delimiter |
| [Delimiter](/reference/datagate/datagate-client/delimiter.html) | StarAll | Gets a new instance of the  class that represents a newline delimiter. |
| [Delimiter](/reference/datagate/datagate-client/delimiter.html) | StarCR | Gets a new instance of the  class that represents a carriage return delimiter. |
| [Delimiter](/reference/datagate/datagate-client/delimiter.html) | StarCRLF | Gets a new instance of the  class that represents a carriage return and line feed delimiter. |
| [Delimiter](/reference/datagate/datagate-client/delimiter.html) | StarLFCR | Gets a new instance of the  class that represents a line feed followed by a carriage return delimiter. |
| [Delimiter](/reference/datagate/datagate-client/delimiter.html) | StartLF | Gets a new instance of the  class that represents a line feed delimiter. |
| [Char](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/char) | Value | Gets or sets the value of this instance. |

## Methods

| Signature | Description |
| --- | --- |
| [ClearValue()](#void-clearvalue) | Clears the value of this instance, making it represent no delimiter.
| [Equals](#bool-equalsobject-obj)([Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | Determines whether the specified object is equal to the current object.
| [FromChar](#delimiter-fromcharchar-ch)([Char](https://docs.microsoft.com/en-us/dotnet/api/system.char)) | Creates a new  instance from a given character.
| [GetHashCode()](#int-gethashcode) | Serves as the default hash function.
| [op_Equality](#bool-op-equalitydelimiter-lval-delimiter-rval)([Delimiter](/reference/datagate/datagate-client/delimiter.html), [Delimiter](/reference/datagate/datagate-client/delimiter.html)) | Determines whether two  instances are equal.
| [op_Inequality](#bool-op-inequalitydelimiter-lval-delimiter-rval)([Delimiter](/reference/datagate/datagate-client/delimiter.html), [Delimiter](/reference/datagate/datagate-client/delimiter.html)) | Determines whether two  instances are not equal.
| [ToChar()](#char-tochar) | Converts the value of this instance to a .
| [ToString()](#string-tostring) | Returns a string that represents the current object.

### void ClearValue()

Clears the value of this instance, making it represent no delimiter.


#### Remarks
This method sets the  field to false, indicating that the  property has not been set.As a result, this instance will represent no delimiter (IsStarNone will be true).

```cs
void ClearValue()
```

### bool Equals([object obj](https://docs.microsoft.com/en-us/dotnet/api/system.object))

Determines whether the specified object is equal to the current object.


#### Remarks
This method overrides the base  method and performs a series of checks to determine equality:- If the provided object is a  instance, it uses the equality operator (==) to compare the two instances.- If the provided object is a , it creates a new  instance from the character and uses the equality operator to compare the two instances.- If the provided object is neither a  nor a , it returns false.

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

### Delimiter FromChar([char ch](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/char))

Creates a new  instance from a given character.


#### Remarks
This method creates a new  instance and sets its  property to the given character.If the given character is '\0', the created  instance will represent no delimiter (IsStarNone will be true).

```cs
Delimiter FromChar(char ch)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Char](https://docs.microsoft.com/en-us/dotnet/api/system.char) | ch | The character to create a  from.

#### Returns

| Type | Description
| --- | ---
| [Delimiter](/reference/datagate/datagate-client/delimiter.html) | A new  instance with its value set to the given character.

### int GetHashCode()

Serves as the default hash function.


#### Remarks
This method overrides the base  method and simply calls the base implementation.The base implementation of  returns a hash code for the current object.

```cs
int GetHashCode()
```

### bool op_Equality([Delimiter lval](/reference/datagate/datagate-client/delimiter.html), [Delimiter rval](/reference/datagate/datagate-client/delimiter.html))

Determines whether two  instances are equal.


#### Remarks
This operator performs a series of checks to determine equality:- If both instances are null, they are considered equal.- If one instance is null and the other is not, they are considered not equal.- If both instances represent no delimiter (IsStarNone is true), they are considered equal.- If one instance represents no delimiter and the other does not, they are considered not equal.- Otherwise, the values of the instances are compared.

```cs
bool op_Equality(Delimiter lval, Delimiter rval)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Delimiter](/reference/datagate/datagate-client/delimiter.html) | lval | The first  to compare.
| [Delimiter](/reference/datagate/datagate-client/delimiter.html) | rval | The second  to compare.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | true if the  instances are equal; otherwise, false.

### bool op_Inequality([Delimiter lval](/reference/datagate/datagate-client/delimiter.html), [Delimiter rval](/reference/datagate/datagate-client/delimiter.html))

Determines whether two  instances are not equal.


#### Remarks
This operator is the logical negation of the equality operator (==).

```cs
bool op_Inequality(Delimiter lval, Delimiter rval)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Delimiter](/reference/datagate/datagate-client/delimiter.html) | lval | The first  to compare.
| [Delimiter](/reference/datagate/datagate-client/delimiter.html) | rval | The second  to compare.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | true if the  instances are not equal; otherwise, false.

### char ToChar()

Converts the value of this instance to a .


#### Remarks
This method returns the  property of this instance, which is a .If the  property has not been set (IsStarNone is true), this method will throw an .

```cs
char ToChar()
```

### string ToString()

Returns a string that represents the current object.


#### Remarks
This method overrides the base  method and performs a check to determine the string representation:- If this instance represents no delimiter (None == this is true), it returns an empty string.- Otherwise, it creates a new string from the  property of this instance.

```cs
string ToString()
```
