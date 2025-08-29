---
title: "AdgConnection.GetSupportsMultiMember Method"
description: "Gets a value indicating whether the connection supports multi-member files."
---

## Definition

**Namespace:** ASNA.DataGate.Client<br/>
**Assembly:** ASNA.QSys.DataGate.Client.dll

### bool GetSupportsMultiMember()

Gets a value indicating whether the connection is associates with a server that supports multi-member files. 

#### Remarks

The only server that may not have multimember support is SQL Server when configured to not support multiple members per file.


```cs
bool GetSupportsMultiMember()
```

#### Returns

| Type | Description
| --- | ---
| [bool](https://learn.microsoft.com/en-us/dotnet/api/system.boolean) | `true` when the server supports files with multiple members.


## See Also

[AdgConnection Class](adg-connection.html)