---
title: "DatabaseLabel.LabelDatabase Method"
description: "Create a label for an existing database"
---

## Definition

**Namespace:** ASNA.DataGate.Client.DatabaseLabel  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Create a label for an existing database

<a id="void-labeldatabase-sourceprofile-serverandcredentials-ilabel-label-boolean-bexists"></a>
## void LabelDatabase(SourceProfile serverAndCredentials, ILabel label, Boolean& bExists)

Create a label for an existing database

```cs
void LabelDatabase(SourceProfile serverAndCredentials, ILabel label, Boolean& bExists)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [SourceProfile](/reference/datagate/datagate-providers/source-profile.html) | serverAndCredentials | Server name and credentials for            DG access.
| [ILabel](/reference/datagate/datagate-client/i-label.html) | label | Label details
| [Boolean&](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | bExists | Modified to reflect whether the database            exists

## See Also
- [DatabaseLabel class](database-label.html)
