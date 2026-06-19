---
title: "MultiCharDelimiter class"
description: "Represents a delimiter in a data stream. "
last_modified_at: 2024-08-09T17:25:07Z
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
| [Equals](multi-char-delimiter-equals.html#bool-equals-object-obj)([Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | Determines whether the specified object is equal to the current  object.
| [GetHashCode()](multi-char-delimiter-gethashcode.html#int-gethashcode) | Serves as the default hash function.
| [op_Equality](multi-char-delimiter-op-equality.html#bool-op-equality-multichardelimiter-ldlim-delimiter-rdlim)([MultiCharDelimiter](/reference/datagate/datagate-client/multi-char-delimiter.html), [Delimiter](/reference/datagate/datagate-client/delimiter.html)) | Determines whether a  instance and a  instance are equal.
| [op_Equality](multi-char-delimiter-op-equality.html#bool-op-equality-delimiter-ldlim-multichardelimiter-rdlim)([Delimiter](/reference/datagate/datagate-client/delimiter.html), [MultiCharDelimiter](/reference/datagate/datagate-client/multi-char-delimiter.html)) | Determines whether a  instance and a  instance are equal.
| [op_Inequality](multi-char-delimiter-op-inequality.html#bool-op-inequality-multichardelimiter-ldlim-delimiter-rdlim)([MultiCharDelimiter](/reference/datagate/datagate-client/multi-char-delimiter.html), [Delimiter](/reference/datagate/datagate-client/delimiter.html)) | Determines whether a  instance and a  instance are not equal.
| [op_Inequality](multi-char-delimiter-op-inequality.html#bool-op-inequality-delimiter-ldlim-multichardelimiter-rdlim)([Delimiter](/reference/datagate/datagate-client/delimiter.html), [MultiCharDelimiter](/reference/datagate/datagate-client/multi-char-delimiter.html)) | Determines whether a  instance and a  instance are not equal.
| [ToString()](multi-char-delimiter-tostring.html#string-tostring) | Returns a string that represents the current  object.

