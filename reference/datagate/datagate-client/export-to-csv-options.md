---
title: "ExportToCsvOptions class      | QSYS API Reference Guide"
description: "Provides options for exporting data to CSV format. This class includes properties for specifying whether field names should be included, whether trail"
last_modified_at: 2024-08-08T21:41:32Z
---

Provides options for exporting data to CSV format.
This class includes properties for specifying whether field names should be included, whether trailing delimiters should be omitted, and what characters should be used for text delimiters, field delimiters, and decimal points in the exported data.

**Namespace:** ASNA.DataGate.Client.CopyData
**Assembly:** ASNA.QSys.DataGate.Client.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [ExportOptions](/reference/datagate/datagate-client/export-options.html)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [ExportToCsvOptions](#exporttocsvoptionsimember-string-exportaccessmode)([IMember](/reference/datagate/datagate-client/i-member.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [ExportAccessMode](/reference/datagate/datagate-client/export-access-mode.html)) | Initializes a new instance of the  class.

### ExportToCsvOptions([IMember](/reference/datagate/datagate-client/i-member.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [ExportAccessMode](/reference/datagate/datagate-client/export-access-mode.html))

Initializes a new instance of the  class.

```cs
ExportToCsvOptions(IMember, String, ExportAccessMode)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [IMember](/reference/datagate/datagate-client/i-member.html) | src | The source data to be exported.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | target | The target path where the data will be exported.
| [ExportAccessMode](/reference/datagate/datagate-client/export-access-mode.html) | seq | The access mode for data export.

## Properties

| Type | Name | Description
| --- | --- | --- 
| [Char](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/char) | DecimalPoint | Gets or sets the decimal point character to be used in the exported CSV data. |
| [Nullable\<Char\>](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/nullable-value-types) | FieldDelimiter | Gets or sets the field delimiter to be used in the exported CSV data. |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | IncludeNames | Gets or sets a value indicating whether field names should be included in the exported CSV data. |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | OmitTrailingDelimiter | Gets or sets a value indicating whether trailing delimiters should be omitted in the exported CSV data. |
| [Nullable\<Char\>](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/nullable-value-types) | TextDelimiter | Gets or sets the text delimiter to be used in the exported CSV data. |
