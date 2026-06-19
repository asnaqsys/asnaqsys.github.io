---
title: "As400Program.SetConnection Method"
description: "Sets the connection to be used by the program."
---

## Definition

**Namespace:** ASNA.DataGate.Client  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Sets the connection to be used by the program.

<a id="void-setconnection-adgconnection-value"></a>
## void SetConnection(AdgConnection value)

Sets the connection to be used by the program.

#### Remarks
This method sets the connection for the ASNA DataGate client. The provided connection is checked for null before being set.

```cs
void SetConnection(AdgConnection value)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [AdgConnection](/reference/datagate/datagate-client/adg-connection.html) | value | The connection to be used.

## See Also
- [As400Program class](as400-program.html)
