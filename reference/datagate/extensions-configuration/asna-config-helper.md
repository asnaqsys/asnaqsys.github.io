---
title: "AsnaConfigHelper class"
description: "Provides helper functions and properties for accessing IAsnaConfig properties encoded in JSON configuration texts. "
last_modified_at: 2024-08-09T17:25:07Z
---

Provides helper functions and properties for accessing
IAsnaConfig properties encoded in JSON configuration texts.

**Namespace:** ASNA.Extensions.Configuration
**Assembly:** ASNA.QSys.DataGate.Client.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>

## Properties

| Type | Name | Description
| --- | --- | --- 
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | DefaultConfigFilePath | Gets the suggested full path name for a "default" configurationfile. |

## Methods

| Signature | Description |
| --- | --- |
| [LoadFromJson](asna-config-helper-loadfromjson.html#iasnaconfig-loadfromjson-stream-jsonstream)([Stream](https://learn.microsoft.com/en-us/dotnet/api/system.io.stream?view=net-8.0)) | Returns an instance of IAsnaConfig, given a stream.
| [LoadFromJson](asna-config-helper-loadfromjson.html#iasnaconfig-loadfromjson-string-jsonfilepath)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Returns an instance of IAsnaConfig, given a path to aJSON-encoded file.
| [TryLoadFromDefaultFile](asna-config-helper-tryloadfromdefaultfile.html#bool-tryloadfromdefaultfile-iasnaconfig-config)([IAsnaConfig&](/reference/datagate/extensions-configuration/i-asna-config.html)) | Gets a configuration from the default file.

