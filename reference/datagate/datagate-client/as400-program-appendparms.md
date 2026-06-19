---
title: "As400Program.AppendParms Method"
description: "Appends an array of parameters to the program."
---

## Definition

**Namespace:** ASNA.DataGate.Client  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Appends an array of parameters to the program.

<a id="void-appendparms-progparm-parameters-reference-datagate-datagate-data-link-prog-parm-html"></a>
## void AppendParms([ProgParm\[\] parameters](/reference/datagate/datagate-data-link/prog-parm.html))

Appends an array of parameters to the program.

#### Remarks
This method appends an array of parameters to the program in the ASNA DataGate client. It checks if the provided array is null, and if so, throws an ArgumentNullException. It then iterates over the array and appends each parameter to the program using the AppendParm method.

```cs
void AppendParms(ProgParm[] parameters)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [ProgParm\[\]](/reference/datagate/datagate-data-link/prog-parm.html) | parameters | The array of parameters to append.

## See Also
- [As400Program class](as400-program.html)
