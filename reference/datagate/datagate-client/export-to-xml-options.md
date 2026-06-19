---
title: "ExportToXmlOptions class"
description: "Provides options for exporting data to XML format. This class includes properties for specifying whether fields should be exported as elements and whe"
last_modified_at: 2024-08-09T17:25:07Z
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
| [ExportToXmlOptions](export-to-xml-options-ctor.html#exporttoxmloptions-imember-string-exportaccessmode)([IMember](/reference/datagate/datagate-client/i-member.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [ExportAccessMode](/reference/datagate/datagate-client/export-access-mode.html)) | Initializes a new instance of the  class.
| [ExportToXmlOptions](export-to-xml-options-ctor.html#exporttoxmloptions-imember-string-exportaccessmode-boolean)([IMember](/reference/datagate/datagate-client/i-member.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [ExportAccessMode](/reference/datagate/datagate-client/export-access-mode.html), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Initializes a new instance of the  class.
| [ExportToXmlOptions](export-to-xml-options-ctor.html#exporttoxmloptions-imember-string-exportaccessmode-boolean-boolean)([IMember](/reference/datagate/datagate-client/i-member.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [ExportAccessMode](/reference/datagate/datagate-client/export-access-mode.html), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Initializes a new instance of the  class.

## Properties

| Type | Name | Description
| --- | --- | --- 
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | FieldsAsElements | Gets or sets a value indicating whether fields should be exported as elements. |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | IncludeSchema | Gets or sets a value indicating whether the schema should be included in the exported data. |

