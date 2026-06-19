---
title: "MultiCharDelimiter.op_Inequality Method"
description: "Determines whether a instance and a instance are not equal."
---

## Definition

**Namespace:** ASNA.DataGate.Client.CopyData  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Determines whether a instance and a instance are not equal.

## Overloads

| Signature | Description |
| --- | --- |
| [op_Inequality](#bool-op-inequality-multichardelimiter-ldlim-delimiter-rdlim)(bool op_Inequality(MultiCharDelimiter ldlim, Delimiter rdlim)) | Determines whether a instance and a instance are not equal. |
| [op_Inequality](#bool-op-inequality-delimiter-ldlim-multichardelimiter-rdlim)(bool op_Inequality(Delimiter ldlim, MultiCharDelimiter rdlim)) | Determines whether a instance and a instance are not equal. |

<a id="bool-op-inequality-multichardelimiter-ldlim-delimiter-rdlim"></a>
## bool op_Inequality(MultiCharDelimiter ldlim, Delimiter rdlim)

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

<a id="bool-op-inequality-delimiter-ldlim-multichardelimiter-rdlim"></a>
## bool op_Inequality(Delimiter ldlim, MultiCharDelimiter rdlim)

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

## See Also
- [MultiCharDelimiter class](multi-char-delimiter.html)
