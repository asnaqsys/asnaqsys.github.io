---
title: "ExportToXmlOptions Constructors"
description: "Initializes a new instance of the class."
---

## Definition

**Namespace:** ASNA.DataGate.Client.CopyData  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Initializes a new instance of the class.

## Overloads

| Name | Description |
| --- | --- |
| [ExportToXmlOptions](#exporttoxmloptions-imember-string-exportaccessmode)([IMember](/reference/datagate/datagate-client/i-member.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [ExportAccessMode](/reference/datagate/datagate-client/export-access-mode.html)) | Initializes a new instance of the class. |
| [ExportToXmlOptions](#exporttoxmloptions-imember-string-exportaccessmode-boolean)([IMember](/reference/datagate/datagate-client/i-member.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [ExportAccessMode](/reference/datagate/datagate-client/export-access-mode.html), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Initializes a new instance of the class. |
| [ExportToXmlOptions](#exporttoxmloptions-imember-string-exportaccessmode-boolean-boolean)([IMember](/reference/datagate/datagate-client/i-member.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [ExportAccessMode](/reference/datagate/datagate-client/export-access-mode.html), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Initializes a new instance of the class. |

<a id="exporttoxmloptions-imember-string-exportaccessmode"></a>
### ExportToXmlOptions([IMember](/reference/datagate/datagate-client/i-member.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [ExportAccessMode](/reference/datagate/datagate-client/export-access-mode.html))

Initializes a new instance of the  class.

```cs
ExportToXmlOptions(IMember, String, ExportAccessMode)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [IMember](/reference/datagate/datagate-client/i-member.html) | src | The source data to be exported.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | target | The target path where the data will be exported.
| [ExportAccessMode](/reference/datagate/datagate-client/export-access-mode.html) | seq | The access mode for data export.

<a id="exporttoxmloptions-imember-string-exportaccessmode-boolean"></a>
### ExportToXmlOptions([IMember](/reference/datagate/datagate-client/i-member.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [ExportAccessMode](/reference/datagate/datagate-client/export-access-mode.html), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Initializes a new instance of the  class.

```cs
ExportToXmlOptions(IMember, String, ExportAccessMode, Boolean)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [IMember](/reference/datagate/datagate-client/i-member.html) | src | The source data to be exported.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | target | The target path where the data will be exported.
| [ExportAccessMode](/reference/datagate/datagate-client/export-access-mode.html) | seq | The access mode for data export.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | bFieldsAsElements | A boolean value indicating whether fields should be exported as elements.

<a id="exporttoxmloptions-imember-string-exportaccessmode-boolean-boolean"></a>
### ExportToXmlOptions([IMember](/reference/datagate/datagate-client/i-member.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [ExportAccessMode](/reference/datagate/datagate-client/export-access-mode.html), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Initializes a new instance of the  class.

```cs
ExportToXmlOptions(IMember, String, ExportAccessMode, Boolean, Boolean)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [IMember](/reference/datagate/datagate-client/i-member.html) | src | The source data to be exported.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | target | The target path where the data will be exported.
| [ExportAccessMode](/reference/datagate/datagate-client/export-access-mode.html) | seq | The access mode for data export.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | bFieldsAsElements | A boolean value indicating whether fields should be exported as elements.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | bSaveSchema | A boolean value indicating whether the schema should be saved.

## See Also
- [ExportToXmlOptions class](export-to-xml-options.html)
