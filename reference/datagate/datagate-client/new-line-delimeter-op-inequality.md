---
title: "NewLineDelimeter.op_Inequality Method"
description: "Determines whether a instance and a instance are not equal."
---

## Definition

**Namespace:** ASNA.DataGate.Client.CopyData  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Determines whether a instance and a instance are not equal.

## Overloads

| Signature | Description |
| --- | --- |
| [op_Inequality](#bool-op-inequality-newlinedelimeter-ldlim-delimiter-rdlim)(bool op_Inequality(NewLineDelimeter ldlim, Delimiter rdlim)) | Determines whether a instance and a instance are not equal. |
| [op_Inequality](#bool-op-inequality-delimiter-ldlim-newlinedelimeter-rdlim)(bool op_Inequality(Delimiter ldlim, NewLineDelimeter rdlim)) | Determines whether a instance and a instance are not equal. |

<a id="bool-op-inequality-newlinedelimeter-ldlim-delimiter-rdlim"></a>
## bool op_Inequality(NewLineDelimeter ldlim, Delimiter rdlim)

Determines whether a  instance and a  instance are not equal.

#### Remarks
This operator is the logical negation of the equality operator (==). It uses the equality operator to compare the two instances and then negates the result.

```cs
bool op_Inequality(NewLineDelimeter ldlim, Delimiter rdlim)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [NewLineDelimeter](/reference/datagate/datagate-client/new-line-delimeter.html) | ldlim | The  instance to compare.
| [Delimiter](/reference/datagate/datagate-client/delimiter.html) | rdlim | The  instance to compare.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | true if the instances are not equal; otherwise, false.

<a id="bool-op-inequality-delimiter-ldlim-newlinedelimeter-rdlim"></a>
## bool op_Inequality(Delimiter ldlim, NewLineDelimeter rdlim)

Determines whether a  instance and a  instance are not equal.

#### Remarks
This operator is the logical negation of the equality operator (==). It uses the equality operator to compare the two instances and then negates the result.

```cs
bool op_Inequality(Delimiter ldlim, NewLineDelimeter rdlim)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Delimiter](/reference/datagate/datagate-client/delimiter.html) | ldlim | The  instance to compare.
| [NewLineDelimeter](/reference/datagate/datagate-client/new-line-delimeter.html) | rdlim | The  instance to compare.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | true if the instances are not equal; otherwise, false.

## See Also
- [NewLineDelimeter class](new-line-delimeter.html)
