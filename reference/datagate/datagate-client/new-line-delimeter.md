---
title: "NewLineDelimeter class"
description: "Represents a newline delimiter in a data stream. "
last_modified_at: 2024-08-09T17:25:07Z
---

Represents a newline delimiter in a data stream.

**Namespace:** ASNA.DataGate.Client.CopyData
**Assembly:** ASNA.QSys.DataGate.Client.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [Delimiter](/reference/datagate/datagate-client/delimiter.html)
<br>
<br>

## Remarks
The NewLineDelimeter class is a specialized type of Delimiter that represents a newline delimiter. 
It overrides certain methods and properties of the Delimiter class to provide behavior specific to newline delimiters.
For example, it overrides the Value property to throw an exception when accessed, because a newline delimiter is a string and not a single character.

<br>
<br>

## Properties

| Type | Name | Description
| --- | --- | --- 
| [Char](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/char) | Value | Gets or sets the value of this instance. |

## Methods

| Signature | Description |
| --- | --- |
| [Equals](new-line-delimeter-equals.html#bool-equals-object-obj)([Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | Determines whether the specified object is equal to the current  object.
| [GetHashCode()](new-line-delimeter-gethashcode.html#int-gethashcode) | Serves as the default hash function.
| [op_Equality](new-line-delimeter-op-equality.html#bool-op-equality-newlinedelimeter-ldlim-delimiter-rdlim)([NewLineDelimeter](/reference/datagate/datagate-client/new-line-delimeter.html), [Delimiter](/reference/datagate/datagate-client/delimiter.html)) | Determines whether a  instance and a  instance are equal.
| [op_Equality](new-line-delimeter-op-equality.html#bool-op-equality-delimiter-ldlim-newlinedelimeter-rdlim)([Delimiter](/reference/datagate/datagate-client/delimiter.html), [NewLineDelimeter](/reference/datagate/datagate-client/new-line-delimeter.html)) | Determines whether a  instance and a  instance are equal.
| [op_Inequality](new-line-delimeter-op-inequality.html#bool-op-inequality-newlinedelimeter-ldlim-delimiter-rdlim)([NewLineDelimeter](/reference/datagate/datagate-client/new-line-delimeter.html), [Delimiter](/reference/datagate/datagate-client/delimiter.html)) | Determines whether a  instance and a  instance are not equal.
| [op_Inequality](new-line-delimeter-op-inequality.html#bool-op-inequality-delimiter-ldlim-newlinedelimeter-rdlim)([Delimiter](/reference/datagate/datagate-client/delimiter.html), [NewLineDelimeter](/reference/datagate/datagate-client/new-line-delimeter.html)) | Determines whether a  instance and a  instance are not equal.
| [ToString()](new-line-delimeter-tostring.html#string-tostring) | Returns a string that represents the current  object.

