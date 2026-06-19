---
title: "IConnectionHandler interface.EnsureConnectionOpened Method"
description: "Ensures that the connection is open."
---

## Definition

**Namespace:** ASNA.DataGate.Client  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Ensures that the connection is open.

<a id="bool-ensureconnectionopened"></a>
## bool EnsureConnectionOpened()

Ensures that the connection is open.

#### Remarks
This method checks if the connection is already open. If it is not, it attempts to open the connection. It returns true if the connection had to be opened, and false if the connection was already open. This can be useful to ensure that a connection is open before performing operations that require it.

```cs
bool EnsureConnectionOpened()
```

## See Also
- [IConnectionHandler interface class](i-connection-handler.html)
