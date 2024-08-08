---
title: "ExportToXmlOptions class      | QSYS API Reference Guide"
description: "Provides options for exporting data to XML format. This class includes properties for specifying whether fields should be exported as elements and whe"
last_modified_at: 2024-08-08T21:41:32Z
---

Provides options for exporting data to XML format.
This class includes properties for specifying whether fields should be exported as elements and whether the schema should be included in the exported data.

**Namespace:** ASNA.DataGate.Client.CopyData
**Assembly:** ASNA.QSys.DataGate.Client.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [ExportOptions](/reference/datagate/datagate-client/export-options.html)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [ExportToXmlOptions](#exporttoxmloptionsimember-string-exportaccessmode)([IMember](/reference/datagate/datagate-client/i-member.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [ExportAccessMode](/reference/datagate/datagate-client/export-access-mode.html)) | Initializes a new instance of the  class.
| [ExportToXmlOptions](#exporttoxmloptionsimember-string-exportaccessmode-boolean)([IMember](/reference/datagate/datagate-client/i-member.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [ExportAccessMode](/reference/datagate/datagate-client/export-access-mode.html), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Initializes a new instance of the  class.
| [ExportToXmlOptions](#exporttoxmloptionsimember-string-exportaccessmode-boolean-boolean)([IMember](/reference/datagate/datagate-client/i-member.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [ExportAccessMode](/reference/datagate/datagate-client/export-access-mode.html), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Initializes a new instance of the  class.

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

## Properties

| Type | Name | Description
| --- | --- | --- 
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | FieldsAsElements | Gets or sets a value indicating whether fields should be exported as elements. |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | IncludeSchema | Gets or sets a value indicating whether the schema should be included in the exported data. |
