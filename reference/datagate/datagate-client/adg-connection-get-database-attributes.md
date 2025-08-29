---
title: "AdgConnection.GetDatabaseAttributes Method"
description: "Gets the attributes of the database."
---

## Definition

**Namespace:** ASNA.DataGate.Client<br/>
**Assembly:** ASNA.QSys.DataGate.Client.dll


### DatabaseAttributes GetDatabaseAttributes()

Gets the attributes of the database.


#### Remarks
This method retrieves the attributes of the database from the SourceProvider if the connection is open.The attributes include information about the database such as its name, version, and other metadata.If the connection is not open, it throws an ApplicationException.

```cs
DatabaseAttributes GetDatabaseAttributes()
```

#### Returns

| Type | Description
| --- | ---
| [DatabaseAttributes](/reference/datagate/datagate-providers/database-attributes.html) | The database attributes.



## See Also

[AdgConnection Class](adg-connection.html)