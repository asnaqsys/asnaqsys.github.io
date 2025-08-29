---
title: "AdgConnection.GetPeerAltCodePageID Method"
description: "Gets the peer alternative code page ID."
---

## Definition

**Namespace:** ASNA.DataGate.Client<br/>
**Assembly:** ASNA.QSys.DataGate.Client.dll

### int GetPeerAltCodePageID()

Gets the peer alternative code page ID.


#### Remarks
This method retrieves the peer alternative code page ID from the DataLinkSource if the connection is open.

The peer alternative code page ID is used to determine the character encoding for the connection.If the connection is not open, it throws an ApplicationException.

```cs
int GetPeerAltCodePageID()
```

#### Returns

| Type | Description
| --- | ---
| [int](https://learn.microsoft.com/en-us/dotnet/api/system.int32) | The code page ID.

## See Also

[AdgConnection Class](adg-connection.html)