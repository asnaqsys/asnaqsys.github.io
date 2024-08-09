---
title: "RootExtensions class          | QSYS API Reference Guide"
description: "Provides extension methods for the root configuration. "
last_modified_at: 2024-08-09T16:18:40Z
---

Provides extension methods for the root configuration.

**Namespace:** ASNA.Extensions.Configuration
**Assembly:** ASNA.QSys.DataGate.Client.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>

## Properties

| Type | Name | Description
| --- | --- | --- 
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | SECTION_ASNA | Represents the section name in the configuration that contains the ASNA configuration. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | SECTION_ASNA_DG | Represents the section name in the ASNA configuration that contains the DataGate configuration. |

## Methods

| Signature | Description |
| --- | --- |
| [GetAsnaConfig](#iconfigurationsection-getasnaconfigiconfiguration-this)([IConfiguration](https://learn.microsoft.com/en-us/dotnet/api/microsoft.extensions.configuration.iconfiguration?view=net-8.0)) | Retrieves the ASNA configuration section from the configuration.
| [GetDataGateConfig](#iconfigurationsection-getdatagateconfigiconfiguration-this)([IConfiguration](https://learn.microsoft.com/en-us/dotnet/api/microsoft.extensions.configuration.iconfiguration?view=net-8.0)) | Retrieves the DataGate configuration section from the ASNA configuration.

### IConfigurationSection GetAsnaConfig([IConfiguration This](https://learn.microsoft.com/en-us/dotnet/api/microsoft.extensions.configuration.iconfiguration?view=net-8.0))

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

### IConfigurationSection GetDataGateConfig([IConfiguration This](https://learn.microsoft.com/en-us/dotnet/api/microsoft.extensions.configuration.iconfiguration?view=net-8.0))

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
