---
title: "Delimiter.op_Inequality Method"
description: "Determines whether two instances are not equal."
---

## Definition

**Namespace:** ASNA.DataGate.Client.CopyData  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Determines whether two instances are not equal.

<a id="bool-op-inequality-delimiter-lval-delimiter-rval"></a>
## bool op_Inequality(Delimiter lval, Delimiter rval)

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

## See Also
- [Delimiter class](delimiter.html)
