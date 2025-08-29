---
title: "AdgConnection.GetDeviceCodePageID Method"
description: "Gets the device code page ID."
---

## Definition

**Namespace:** ASNA.DataGate.Client<br/>
**Assembly:** ASNA.QSys.DataGate.Client.dll

### int GetDeviceCodePageID()

Gets the device code page ID.

#### Remarks
This method retrieves the device code page ID from the DataLinkSource if the connection is open. The device code page ID is used to determine the character encoding for the connection. 

```cs
int GetDeviceCodePageID()
```

#### Returns

| Type | Description
| --- | ---
| [int](https://learn.microsoft.com/en-us/dotnet/api/system.int32) | The device code page ID.


## See Also

[AdgConnection Class](adg-connection.html)