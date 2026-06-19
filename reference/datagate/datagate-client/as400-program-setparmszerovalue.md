---
title: "As400Program.SetParmsZeroValue Method"
description: "Sets all parameters of the program to their zero value."
---

## Definition

**Namespace:** ASNA.DataGate.Client  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Sets all parameters of the program to their zero value.

<a id="void-setparmszerovalue"></a>
## void SetParmsZeroValue()

Sets all parameters of the program to their zero value.

#### Remarks
This method sets all parameters of the program in the ASNA DataGate client to their zero value. It iterates over the list of parameters and calls the SetZeroValue method of each parameter.

```cs
void SetParmsZeroValue()
```

## See Also
- [As400Program class](as400-program.html)
