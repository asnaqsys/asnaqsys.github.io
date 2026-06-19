---
title: "As400Program.GetParameters Method"
description: "Gets the parameters of the program."
---

## Definition

**Namespace:** ASNA.DataGate.Client  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Gets the parameters of the program.

<a id="ienumerable-progparm-getparameters"></a>
## IEnumerable<ProgParm> GetParameters()

Gets the parameters of the program.

#### Remarks
This method returns a read-only collection of the parameters of the program in the ASNA DataGate client. The parameters are stored in a list, which is converted to a read-only collection before being returned.

```cs
IEnumerable<ProgParm> GetParameters()
```

## See Also
- [As400Program class](as400-program.html)
