---
title: "NewLineDelimeter.op_Equality Method"
description: "Determines whether a instance and a instance are equal."
---

## Definition

**Namespace:** ASNA.DataGate.Client.CopyData  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Determines whether a instance and a instance are equal.

## Overloads

| Signature | Description |
| --- | --- |
| [op_Equality](#bool-op-equality-newlinedelimeter-ldlim-delimiter-rdlim)(bool op_Equality(NewLineDelimeter ldlim, Delimiter rdlim)) | Determines whether a instance and a instance are equal. |
| [op_Equality](#bool-op-equality-delimiter-ldlim-newlinedelimeter-rdlim)(bool op_Equality(Delimiter ldlim, NewLineDelimeter rdlim)) | Determines whether a instance and a instance are equal. |

<a id="bool-op-equality-newlinedelimeter-ldlim-delimiter-rdlim"></a>
## bool op_Equality(NewLineDelimeter ldlim, Delimiter rdlim)

Determines whether a  instance and a  instance are equal.

#### Remarks
This operator checks if the provided  instance is a . If it is, the operator returns true. Otherwise, it returns false.

```cs
bool op_Equality(NewLineDelimeter _, Delimiter rdlim)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [NewLineDelimeter](/reference/datagate/datagate-client/new-line-delimeter.html) | ldlim | The  instance to compare.
| [Delimiter](/reference/datagate/datagate-client/delimiter.html) | rdlim | The  instance to compare.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | true if the  instance is a ; otherwise, false.

<a id="bool-op-equality-delimiter-ldlim-newlinedelimeter-rdlim"></a>
## bool op_Equality(Delimiter ldlim, NewLineDelimeter rdlim)

Determines whether a  instance and a  instance are equal.

#### Remarks
This operator checks if the provided  instance is a . If it is, the operator returns true. Otherwise, it returns false.

```cs
bool op_Equality(Delimiter ldlim, NewLineDelimeter _)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Delimiter](/reference/datagate/datagate-client/delimiter.html) | ldlim | The  instance to compare.
| [NewLineDelimeter](/reference/datagate/datagate-client/new-line-delimeter.html) | rdlim | The  instance to compare.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | true if the  instance is a ; otherwise, false.

## See Also
- [NewLineDelimeter class](new-line-delimeter.html)
