---
title: "Delimiter.op_Equality Method"
description: "Determines whether two instances are equal."
---

## Definition

**Namespace:** ASNA.DataGate.Client.CopyData  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Determines whether two instances are equal.

<a id="bool-op-equality-delimiter-lval-delimiter-rval"></a>
## bool op_Equality(Delimiter lval, Delimiter rval)

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

## See Also
- [Delimiter class](delimiter.html)
