---
title: "AsnaConfig class              | QSYS API Reference Guide"
description: "Represents the ASNA configuration. "
last_modified_at: 2024-08-08T21:41:32Z
---

Represents the ASNA configuration.

**Namespace:** ASNA.Extensions.Configuration
**Assembly:** ASNA.QSys.DataGate.Client.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>

## Remarks
This class is used to encapsulate the configuration settings for ASNA. It provides access to the DataGate configuration through the DataGate property.

<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [AsnaConfig](#asnaconfigiconfiguration)([IConfiguration](https://learn.microsoft.com/en-us/dotnet/api/microsoft.extensions.configuration.iconfiguration?view=net-8.0)) | Initializes a new instance of the  class with the specified configuration.

### AsnaConfig([IConfiguration](https://learn.microsoft.com/en-us/dotnet/api/microsoft.extensions.configuration.iconfiguration?view=net-8.0))

Initializes a new instance of the  class with the specified configuration.

```cs
AsnaConfig(IConfiguration)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [IConfiguration](https://learn.microsoft.com/en-us/dotnet/api/microsoft.extensions.configuration.iconfiguration?view=net-8.0) | config | The configuration.

## Properties

| Type | Name | Description
| --- | --- | --- 
| [IDataGateConfig](/reference/datagate/extensions-configuration/i-datagate-config.html) | DataGate | Gets the DataGate configuration. |
