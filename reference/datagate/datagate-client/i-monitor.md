---
title: "IMonitor interface            | QSYS API Reference Guide"
description: "Defines the contract for monitoring resources in the ASNA DataGate client. "
last_modified_at: 2024-08-09T16:18:40Z
---

Defines the contract for monitoring resources in the ASNA DataGate client.

**Namespace:** ASNA.DataGate.Client
**Assembly:** ASNA.QSys.DataGate.Client.dll

**Extends:** [IDisposable](https://learn.microsoft.com/en-us/dotnet/api/system.idisposable?view=net-8.0)
<br>
<br>

## Remarks
This interface provides properties and methods to monitor resources in the ASNA DataGate client. 
It includes properties to get the locks held by the monitor, the active clients monitored by the monitor, 
the open members monitored by the monitor, the connection associated with the monitor, 
and a value indicating whether the monitor should cache data.

<br>
<br>

## Properties

| Type | Name | Description
| --- | --- | --- 
| [IEnumerable\<IClientMonitor\>](https://learn.microsoft.com/en-us/dotnet/api/system.collections.generic.ienumerable-1?view=net-8.0) | ActiveClients | Gets the active clients monitored by the monitor. |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | CacheData | Gets or sets a value indicating whether the monitor should cache data. |
| [AdgConnection](/reference/datagate/datagate-client/adg-connection.html) | Connection | Gets the connection associated with the monitor. |
| [IEnumerable\<ILock\>](https://learn.microsoft.com/en-us/dotnet/api/system.collections.generic.ienumerable-1?view=net-8.0) | LocksHeld | Gets the locks held by the monitor. |
| [IEnumerable\<IPhysicalMember\>](https://learn.microsoft.com/en-us/dotnet/api/system.collections.generic.ienumerable-1?view=net-8.0) | OpenMembers | Gets the open members monitored by the monitor. |
