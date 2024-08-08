---
title: "ISystemValue interface        | QSYS API Reference Guide"
description: "Defines the contract for managing system values in the ASNA DataGate client. "
last_modified_at: 2024-08-08T21:41:32Z
---

Defines the contract for managing system values in the ASNA DataGate client.

**Namespace:** ASNA.DataGate.Client
**Assembly:** ASNA.QSys.DataGate.Client.dll

**Extends:** [IDisposable](https://learn.microsoft.com/en-us/dotnet/api/system.idisposable?view=net-8.0)
<br>
<br>

## Remarks
This interface provides properties to manage system values in the ASNA DataGate client. 
It includes properties to get and set the system and user library lists, 
whether multi-member files are enabled, the QTemp library, the new column collation, 
whether to update the legacy DSS library list, the hashtag prefix substitute, 
the connection associated with the system value, whether to cache data, and the transaction associated with the system value.

<br>
<br>

## Properties

| Type | Name | Description
| --- | --- | --- 
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | CacheData | Gets or sets a value indicating whether to cache data. |
| [AdgConnection](/reference/datagate/datagate-client/adg-connection.html) | Connection | Gets the connection associated with the system value. |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | EnableMultimemberFiles | Gets or sets a value indicating whether multi-member files are enabled. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | HashtagPrefixSubstitute | Gets or sets the hashtag prefix substitute. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | NewColumnCollation | Gets or sets the new column collation. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | QTempLibrary | Gets or sets the QTemp library. |
| [IEnumerable\<String\>](https://learn.microsoft.com/en-us/dotnet/api/system.collections.generic.ienumerable-1?view=net-8.0) | SystemLibraryList | Gets or sets the system library list. |
| [IDbTransaction](https://learn.microsoft.com/en-us/dotnet/api/system.data.idbtransaction?view=net-8.0) | Transaction | Gets the transaction associated with the system value. |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | UpdateLegacyDssLibraryList | Gets or sets a value indicating whether to update the legacy DSS library list. |
| [IEnumerable\<String\>](https://learn.microsoft.com/en-us/dotnet/api/system.collections.generic.ienumerable-1?view=net-8.0) | UserLibraryList | Gets or sets the user library list. |
