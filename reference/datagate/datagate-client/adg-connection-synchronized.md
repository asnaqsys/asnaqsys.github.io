---
title: "AdgConnection.Synchronized Method"
description: "Returns a synchronized (thread-safe) wrapper for the AdgConnection."
---

## Definition

**Namespace:** ASNA.DataGate.Client<br/>
**Assembly:** ASNA.QSys.DataGate.Client.dll


### AdgConnection Synchronized([AdgConnection cn](/reference/datagate/datagate-client/adg-connection.html))

Returns a synchronized (thread-safe) wrapper for the AdgConnection.


#### Remarks
This method checks if the provided AdgConnection is already a SyncConnection. If it is, it returns the connection as is, if it's not, it creates a new SyncConnection with the provided connection and returns it.

The SyncConnection is a thread-safe wrapper for the AdgConnection. It ensures that only one thread can access the AdgConnection at a time, which is necessary when multiple threads are working with the same connection.

```cs
AdgConnection Synchronized(AdgConnection cn)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [AdgConnection](/reference/datagate/datagate-client/adg-connection.html) | cn | The AdgConnection to synchronize.

#### Returns

| Type | Description
| --- | ---
| [AdgConnection](/reference/datagate/datagate-client/adg-connection.html) | A thread-safe wrapper for the AdgConnection.


## See Also

[AdgConnection Class](adg-connection.html)