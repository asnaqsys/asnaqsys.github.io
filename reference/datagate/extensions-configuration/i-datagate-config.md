---
title: "IDataGateConfig interface"
description: "Provides an interface for accessing DataGate configuration. "
last_modified_at: 2024-08-09T17:25:07Z
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
| [ResolveSourceName](i-datagate-config-resolvesourcename.html#sourceprofile-resolvesourcename-string-name)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Resolves a configured SourceProfile with behavior similar to the DatabaseName.ToSourceProfile methods for traditional database names.

