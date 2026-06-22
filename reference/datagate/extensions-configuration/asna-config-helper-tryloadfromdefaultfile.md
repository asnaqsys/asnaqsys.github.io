---
title: "AsnaConfigHelper.TryLoadFromDefaultFile Method"
description: "Gets a configuration from the default file."
---

## Definition

**Namespace:** ASNA.Extensions.Configuration  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Gets a configuration from the default file.

<a id="bool-tryloadfromdefaultfile-iasnaconfig-config"></a>
## bool TryLoadFromDefaultFile(IAsnaConfig& config)

Gets a configuration from the default file.

```cs
bool TryLoadFromDefaultFile(IAsnaConfig& config)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [IAsnaConfig&](/reference/datagate/extensions-configuration/i-asna-config.html) | config | An IAsnaConfig instance, if the default            configuration file named by DefaultConfigFilePath is            found, loaded, and parsed. Otherwise, null.            

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | true if a configuration is loaded from thedefault config file; otherwise false.

## See Also
- [AsnaConfigHelper class](asna-config-helper.html)
