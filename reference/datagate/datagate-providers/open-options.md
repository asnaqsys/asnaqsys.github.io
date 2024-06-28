---
title: OpenOptions enum
description: "Defines options for opening a connection. "
last_modified_at: 2024-06-28T18:18:27Z
---

Defines options for opening a connection.

**Namespace:** ASNA.DataGate.Providers
**Assembly:** ASNA.QSys.DataGate.Client.dll
<br>
<br>

## Enum Values

| Name | Description | Value
| --- | --- | --- 
| Default | Represents the default opening option. | 0 |
| DoNotStartServer | Prevents the server from starting when opening a connection. | 1 |
| ForceAllSessions | Forces all sessions to initiate at AdgConnection.Open(). | 4 |
| StartServerIfUnlimited | Starts the server if User is not limited when opening a connection. | 2 |
