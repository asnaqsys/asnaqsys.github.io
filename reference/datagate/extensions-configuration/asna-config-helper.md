---
title: "AsnaConfigHelper class        | QSYS API Reference Guide"
description: "Provides helper functions and properties for accessing IAsnaConfig properties encoded in JSON configuration texts. "
last_modified_at: 2024-08-08T21:41:32Z
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
| [LoadFromJson](#iasnaconfig-loadfromjsonstream-jsonstream)([Stream](https://learn.microsoft.com/en-us/dotnet/api/system.io.stream?view=net-8.0)) | Returns an instance of IAsnaConfig, given a stream.
| [LoadFromJson](#iasnaconfig-loadfromjsonstring-jsonfilepath)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Returns an instance of IAsnaConfig, given a path to aJSON-encoded file.

### IAsnaConfig LoadFromJson([Stream jsonStream](https://learn.microsoft.com/en-us/dotnet/api/system.io.stream?view=net-8.0))

Returns an instance of IAsnaConfig, given a stream.

```cs
IAsnaConfig LoadFromJson(Stream jsonStream)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Stream](https://learn.microsoft.com/en-us/dotnet/api/system.io.stream?view=net-8.0) | jsonStream | The input Stream.

#### Returns

| Type | Description
| --- | ---
| [IAsnaConfig](/reference/datagate/extensions-configuration/i-asna-config.html) | IAsnaConfig

### IAsnaConfig LoadFromJson([string jsonFilePath](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Returns an instance of IAsnaConfig, given a path to aJSON-encoded file.

```cs
IAsnaConfig LoadFromJson(string jsonFilePath)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | jsonFilePath | 

#### Returns

| Type | Description
| --- | ---
| [IAsnaConfig](/reference/datagate/extensions-configuration/i-asna-config.html) | 
