---
title: "AdgConnection.GetPeerVersion Method"
description: "Gets the protocol level of the peer"
---

## Definition

**Namespace:** ASNA.DataGate.Client<br/>
**Assembly:** ASNA.QSys.DataGate.Client.dll

### ProtoLevel GetPeerVersion()

Gets the protocol level of the DataGate server.

#### Remarks
This method retrieves the protocol level of the peer from the DataLinkSource if the connection is open. The protocol level is used to determine the version of the protocol used for communication.

If the connection is not open, it throws an ApplicationException. If the SourceProvider is not a DataLinkSource, it returns the current protocol version.

```cs
ProtoLevel GetPeerVersion()
```

#### Returns

| Type | Description
| --- | ---
| [ProtoLevel](https://learn.microsoft.com/en-us/dotnet/api/system.int32) | The server protocol level. Higher levels typically mean newer versions.

## See Also

[AdgConnection Class](adg-connection.html)