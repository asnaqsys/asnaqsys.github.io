---
title: "DatabaseLabel.CreateDatabase Method"
description: "Creates a database"
---

## Definition

**Namespace:** ASNA.DataGate.Client.DatabaseLabel  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Creates a database

## Overloads

| Signature | Description |
| --- | --- |
| [CreateDatabase](#void-createdatabase-sourceprofile-serverandcredentials-bool-bissecured-ilabel-label)(void CreateDatabase(SourceProfile serverAndCredentials, bool bIsSecured, ILabel label)) | Creates a database |
| [CreateDatabase](#void-createdatabase-sourceprofile-serverandcredentials-bool-bissecured-ilabel-plabel-int-tcpport)(void CreateDatabase(SourceProfile serverAndCredentials, bool bIsSecured, ILabel pLabel, int tcpPort)) | Creates a database |

<a id="void-createdatabase-sourceprofile-serverandcredentials-bool-bissecured-ilabel-label"></a>
## void CreateDatabase(SourceProfile serverAndCredentials, bool bIsSecured, ILabel label)

Creates a database

```cs
void CreateDatabase(SourceProfile serverAndCredentials, bool bIsSecured, ILabel label)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [SourceProfile](/reference/datagate/datagate-providers/source-profile.html) | serverAndCredentials | Object identifying the server            and client credentials.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | bIsSecured | Whether the database is secure
| [ILabel](/reference/datagate/datagate-client/i-label.html) | label | Label details for the database

<a id="void-createdatabase-sourceprofile-serverandcredentials-bool-bissecured-ilabel-plabel-int-tcpport"></a>
## void CreateDatabase(SourceProfile serverAndCredentials, bool bIsSecured, ILabel pLabel, int tcpPort)

Creates a database

```cs
void CreateDatabase(SourceProfile serverAndCredentials, bool bIsSecured, ILabel pLabel, int tcpPort)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [SourceProfile](/reference/datagate/datagate-providers/source-profile.html) | serverAndCredentials | Object identifying the server            and client credentials.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | bIsSecured | Whether the database is secure
| [ILabel](/reference/datagate/datagate-client/i-label.html) | pLabel | Label details for the database
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | tcpPort | The TCP port number the server listens to.

## See Also
- [DatabaseLabel class](database-label.html)
