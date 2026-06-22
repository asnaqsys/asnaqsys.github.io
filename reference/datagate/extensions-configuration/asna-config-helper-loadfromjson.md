---
title: "AsnaConfigHelper.LoadFromJson Method"
description: "Returns an instance of IAsnaConfig, given a stream."
---

## Definition

**Namespace:** ASNA.Extensions.Configuration  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Returns an instance of IAsnaConfig, given a stream.

## Overloads

| Signature | Description |
| --- | --- |
| [LoadFromJson](#iasnaconfig-loadfromjson-stream-jsonstream)(IAsnaConfig LoadFromJson(Stream jsonStream)) | Returns an instance of IAsnaConfig, given a stream. |
| [LoadFromJson](#iasnaconfig-loadfromjson-string-jsonfilepath)(IAsnaConfig LoadFromJson(string jsonFilePath)) | Returns an instance of IAsnaConfig, given a path to aJSON-encoded file. |

<a id="iasnaconfig-loadfromjson-stream-jsonstream"></a>
## IAsnaConfig LoadFromJson(Stream jsonStream)

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

<a id="iasnaconfig-loadfromjson-string-jsonfilepath"></a>
## IAsnaConfig LoadFromJson(string jsonFilePath)

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

## See Also
- [AsnaConfigHelper class](asna-config-helper.html)
