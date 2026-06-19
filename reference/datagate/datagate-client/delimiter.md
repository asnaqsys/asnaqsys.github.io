---
title: "Delimiter class"
description: "Represents a delimiter in a data stream. "
last_modified_at: 2024-08-09T17:25:07Z
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
| [Delimiter()](delimiter-ctor.html#delimiter) | Initializes a new instance of the  class.
| [Delimiter](delimiter-ctor.html#delimiter-char)([Char](https://docs.microsoft.com/en-us/dotnet/api/system.char)) | Initializes a new instance of the  class with a specified value.

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
| [ClearValue()](delimiter-clearvalue.html#void-clearvalue) | Clears the value of this instance, making it represent no delimiter.
| [Equals](delimiter-equals.html#bool-equals-object-obj)([Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | Determines whether the specified object is equal to the current object.
| [FromChar](delimiter-fromchar.html#delimiter-fromchar-char-ch)([Char](https://docs.microsoft.com/en-us/dotnet/api/system.char)) | Creates a new  instance from a given character.
| [GetHashCode()](delimiter-gethashcode.html#int-gethashcode) | Serves as the default hash function.
| [op_Equality](delimiter-op-equality.html#bool-op-equality-delimiter-lval-delimiter-rval)([Delimiter](/reference/datagate/datagate-client/delimiter.html), [Delimiter](/reference/datagate/datagate-client/delimiter.html)) | Determines whether two  instances are equal.
| [op_Inequality](delimiter-op-inequality.html#bool-op-inequality-delimiter-lval-delimiter-rval)([Delimiter](/reference/datagate/datagate-client/delimiter.html), [Delimiter](/reference/datagate/datagate-client/delimiter.html)) | Determines whether two  instances are not equal.
| [ToChar()](delimiter-tochar.html#char-tochar) | Converts the value of this instance to a .
| [ToString()](delimiter-tostring.html#string-tostring) | Returns a string that represents the current object.

