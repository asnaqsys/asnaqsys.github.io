---
title: "RootExtensions class"
description: "Provides extension methods for the root configuration. "
last_modified_at: 2024-08-09T17:25:07Z
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
| [GetAsnaConfig](root-extensions-getasnaconfig.html#iconfigurationsection-getasnaconfig-iconfiguration-this)([IConfiguration](https://learn.microsoft.com/en-us/dotnet/api/microsoft.extensions.configuration.iconfiguration?view=net-8.0)) | Retrieves the ASNA configuration section from the configuration.
| [GetDataGateConfig](root-extensions-getdatagateconfig.html#iconfigurationsection-getdatagateconfig-iconfiguration-this)([IConfiguration](https://learn.microsoft.com/en-us/dotnet/api/microsoft.extensions.configuration.iconfiguration?view=net-8.0)) | Retrieves the DataGate configuration section from the ASNA configuration.

