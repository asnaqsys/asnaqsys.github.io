---
title: "RootExtensions.GetAsnaConfig Method"
description: "Retrieves the ASNA configuration section from the configuration."
---

## Definition

**Namespace:** ASNA.Extensions.Configuration  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Retrieves the ASNA configuration section from the configuration.

<a id="iconfigurationsection-getasnaconfig-iconfiguration-this"></a>
## IConfigurationSection GetAsnaConfig(IConfiguration This)

Retrieves the ASNA configuration section from the configuration.

#### Remarks
This method is used to retrieve the ASNA configuration section from the configuration. The section is identified by the SECTION_ASNA constant.

```cs
IConfigurationSection GetAsnaConfig(IConfiguration This)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [IConfiguration](https://learn.microsoft.com/en-us/dotnet/api/microsoft.extensions.configuration.iconfiguration?view=net-8.0) | This | The configuration.

#### Returns

| Type | Description
| --- | ---
| [IConfigurationSection](https://learn.microsoft.com/en-us/dotnet/api/microsoft.extensions.configuration.iconfigurationsection?view=net-8.0) | The ASNA configuration section.

## See Also
- [RootExtensions class](root-extensions.html)
