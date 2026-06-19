---
title: "IClientMonitor interface.Kill Method"
description: "Forcibly terminates the current client."
---

## Definition

**Namespace:** ASNA.DataGate.Client  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Forcibly terminates the current client.

<a id="void-kill-int-delay"></a>
## void Kill(int delay)

Forcibly terminates the current client.

#### Remarks
This method will forcibly terminate the client after the specified delay. Use this method with caution as it can lead to data loss if the client is in the middle of a transaction.

```cs
void Kill(int delay)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | delay | Wait time in milliseconds before terminating the client.

## See Also
- [IClientMonitor interface class](i-client-monitor.html)
