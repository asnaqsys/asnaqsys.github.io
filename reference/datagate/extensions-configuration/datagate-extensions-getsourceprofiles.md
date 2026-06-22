---
title: "DataGateExtensions.GetSourceProfiles Method"
description: "Retrieves a read-only dictionary of source profiles from the configuration."
---

## Definition

**Namespace:** ASNA.Extensions.Configuration  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Retrieves a read-only dictionary of source profiles from the configuration.

<a id="ireadonlydictionary-string-sourceprofile-getsourceprofiles-iconfiguration-config"></a>
## IReadOnlyDictionary\<string, SourceProfile\> GetSourceProfiles(IConfiguration config)

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

## See Also
- [DataGateExtensions class](datagate-extensions.html)
