---
title: "IDataGateConfig interface     | QSYS API Reference Guide"
description: "Provides an interface for accessing DataGate configuration. "
last_modified_at: 2024-08-09T16:18:40Z
---

Provides an interface for accessing DataGate configuration.

**Namespace:** ASNA.Extensions.Configuration
**Assembly:** ASNA.QSys.DataGate.Client.dll

**Extends:** doesn't extend any other interfaces.
<br>
<br>

## Properties

| Type | Name | Description
| --- | --- | --- 
| [IReadOnlyDictionary\<String, SourceProfile\>](https://learn.microsoft.com/en-us/dotnet/api/system.collections.generic.ireadonlydictionary-2?view=net-8.0) | Sources | Gets the table of all configured database sources. |

## Methods

| Signature | Description |
| --- | --- |
| [ResolveSourceName](#sourceprofile-resolvesourcenamestring-name)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Resolves a configured SourceProfile with behavior similar to the DatabaseName.ToSourceProfile methods for traditional database names.

### SourceProfile ResolveSourceName([string name](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Resolves a configured SourceProfile with behavior similar to the DatabaseName.ToSourceProfile methods for traditional database names.


#### Remarks
This method is used to resolve a SourceProfile from its name. If the name is not found, it throws a NoDbNameException.

```cs
SourceProfile ResolveSourceName(string name)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | name | The name of the source to resolve.

#### Returns

| Type | Description
| --- | ---
| [SourceProfile](/reference/datagate/datagate-providers/source-profile.html) | The resolved SourceProfile.
