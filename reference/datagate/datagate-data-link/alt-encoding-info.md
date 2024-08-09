---
title: "AltEncodingInfo class         | QSYS API Reference Guide"
description: "Represents information about an alternative encoding. "
last_modified_at: 2024-08-09T16:18:40Z
---

Represents information about an alternative encoding.

**Namespace:** ASNA.DataGate.DataLink.Text
**Assembly:** ASNA.QSys.DataGate.Client.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [AltEncodingInfo](#altencodinginfoaltencoding)([AltEncoding](/reference/datagate/datagate-data-link/alt-encoding.html)) | Initializes a new instance of the AltEncodingInfo class with the specified AltEncoding.

### AltEncodingInfo([AltEncoding](/reference/datagate/datagate-data-link/alt-encoding.html))

Initializes a new instance of the AltEncodingInfo class with the specified AltEncoding.

```cs
AltEncodingInfo(AltEncoding)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [AltEncoding](/reference/datagate/datagate-data-link/alt-encoding.html) | enc | The AltEncoding to use.

## Properties

| Type | Name | Description
| --- | --- | --- 
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | CodePage | Gets the code page identifier of the AltEncoding for this instance of AltEncodingInfo. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | DisplayName | Gets the display name of the AltEncoding for this instance of AltEncodingInfo. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | Name | Gets the web name of the AltEncoding for this instance of AltEncodingInfo. |

## Methods

| Signature | Description |
| --- | --- |
| [GetEncoding()](#altencoding-getencoding) | Returns the AltEncoding for this instance of AltEncodingInfo.

### AltEncoding GetEncoding()

Returns the AltEncoding for this instance of AltEncodingInfo.

```cs
AltEncoding GetEncoding()
```
