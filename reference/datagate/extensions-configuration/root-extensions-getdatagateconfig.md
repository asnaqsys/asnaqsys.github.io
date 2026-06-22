---
title: "RootExtensions.GetDataGateConfig Method"
description: "Retrieves the DataGate configuration section from the ASNA configuration."
---

## Definition

**Namespace:** ASNA.Extensions.Configuration  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Retrieves the DataGate configuration section from the ASNA configuration.

<a id="iconfigurationsection-getdatagateconfig-iconfiguration-this"></a>
## IConfigurationSection GetDataGateConfig(IConfiguration This)

Retrieves the DataGate configuration section from the ASNA configuration.

#### Remarks
This method is used to retrieve the DataGate configuration section from the ASNA configuration. The section is identified by the SECTION_ASNA_DG constant.

```cs
IConfigurationSection GetDataGateConfig(IConfiguration This)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [IConfiguration](https://learn.microsoft.com/en-us/dotnet/api/microsoft.extensions.configuration.iconfiguration?view=net-8.0) | This | The configuration.

#### Returns

| Type | Description
| --- | ---
| [IConfigurationSection](https://learn.microsoft.com/en-us/dotnet/api/microsoft.extensions.configuration.iconfigurationsection?view=net-8.0) | The DataGate configuration section.

## See Also
- [RootExtensions class](root-extensions.html)
