---
title: "IConnectionHandler interface  | QSYS API Reference Guide"
description: "Defines the methods for handling connections. "
last_modified_at: 2024-08-09T16:18:40Z
---

Defines the methods for handling connections.

**Namespace:** ASNA.DataGate.Client
**Assembly:** ASNA.QSys.DataGate.Client.dll

**Extends:** [IDisposable](https://learn.microsoft.com/en-us/dotnet/api/system.idisposable?view=net-8.0)
<br>
<br>

## Remarks
This interface provides methods for opening, closing, and managing connections. 
It can be implemented by any class that needs to manage connections, such as a database connection handler or a network connection handler.

<br>
<br>

## Methods

| Signature | Description |
| --- | --- |
| [EnsureConnectionOpened()](#bool-ensureconnectionopened) | Ensures that the connection is open.

### bool EnsureConnectionOpened()

Ensures that the connection is open.


#### Remarks
This method checks if the connection is already open. If it is not, it attempts to open the connection. It returns true if the connection had to be opened, and false if the connection was already open. This can be useful to ensure that a connection is open before performing operations that require it.

```cs
bool EnsureConnectionOpened()
```
