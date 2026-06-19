---
title: "MultiCharDelimiter.op_Equality Method"
description: "Determines whether a instance and a instance are equal."
---

## Definition

**Namespace:** ASNA.DataGate.Client.CopyData  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Determines whether a instance and a instance are equal.

## Overloads

| Signature | Description |
| --- | --- |
| [op_Equality](#bool-op-equality-multichardelimiter-ldlim-delimiter-rdlim)(bool op_Equality(MultiCharDelimiter ldlim, Delimiter rdlim)) | Determines whether a instance and a instance are equal. |
| [op_Equality](#bool-op-equality-delimiter-ldlim-multichardelimiter-rdlim)(bool op_Equality(Delimiter ldlim, MultiCharDelimiter rdlim)) | Determines whether a instance and a instance are equal. |

<a id="bool-op-equality-multichardelimiter-ldlim-delimiter-rdlim"></a>
## bool op_Equality(MultiCharDelimiter ldlim, Delimiter rdlim)

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

<a id="bool-op-equality-delimiter-ldlim-multichardelimiter-rdlim"></a>
## bool op_Equality(Delimiter ldlim, MultiCharDelimiter rdlim)

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

## See Also
- [MultiCharDelimiter class](multi-char-delimiter.html)
