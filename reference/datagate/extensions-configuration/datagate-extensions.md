---
title: "DataGateExtensions class      | QSYS API Reference Guide"
description: "Provides extension methods for the DataGate configuration. "
last_modified_at: 2024-08-09T16:18:40Z
---

Provides extension methods for the DataGate configuration.

**Namespace:** ASNA.Extensions.Configuration
**Assembly:** ASNA.QSys.DataGate.Client.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>

## Properties

| Type | Name | Description
| --- | --- | --- 
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | SECTION_SOURCES | Represents the section name in the configuration that contains the source profiles. |

## Methods

| Signature | Description |
| --- | --- |
| [GetSourceProfiles](#ireadonlydictionary-string-sourceprofile-getsourceprofilesiconfiguration-config)([IConfiguration](https://learn.microsoft.com/en-us/dotnet/api/microsoft.extensions.configuration.iconfiguration?view=net-8.0)) | Retrieves a read-only dictionary of source profiles from the configuration.

### IReadOnlyDictionary\<string, SourceProfile\> GetSourceProfiles([IConfiguration config](https://learn.microsoft.com/en-us/dotnet/api/microsoft.extensions.configuration.iconfiguration?view=net-8.0))

Retrieves a read-only dictionary of source profiles from the configuration.


#### Remarks
This method is used to retrieve all source profiles from the configuration. The source profiles are loaded lazily, which means they are only loaded when they are accessed.

```cs
IReadOnlyDictionary<string, SourceProfile> GetSourceProfiles(IConfiguration config)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [IConfiguration](https://learn.microsoft.com/en-us/dotnet/api/microsoft.extensions.configuration.iconfiguration?view=net-8.0) | config | The configuration.

#### Returns

| Type | Description
| --- | ---
| [IReadOnlyDictionary`2](https://learn.microsoft.com/en-us/dotnet/api/system.collections.generic.ireadonlydictionary-2?view=net-8.0) | A read-only dictionary of source profiles. The key is the name of the source profile, and the value is the source profile itself.
