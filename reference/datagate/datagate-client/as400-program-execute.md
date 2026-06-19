---
title: "As400Program.Execute Method"
description: "Executes the program with the current parameters."
---

## Definition

**Namespace:** ASNA.DataGate.Client  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Executes the program with the current parameters.

<a id="void-execute"></a>
## void Execute()

Executes the program with the current parameters.

#### Remarks
This method executes the program in the ASNA DataGate client. It first checks if the program path is null or empty, and if so, throws an InvalidOperationException. It then creates a new ParmExchanger with the current parameters and calls the program with the ParmExchanger. The ParmExchanger writes the parameters to the data link before the program is called and reads the parameters from the data link after the program is called.

```cs
void Execute()
```

## See Also
- [As400Program class](as400-program.html)
