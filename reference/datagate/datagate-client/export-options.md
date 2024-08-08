---
title: "ExportOptions class           | QSYS API Reference Guide"
description: "Provides methods for exporting data to XML or CSV formats. This class includes functionality for transforming data using XSLT, logging, and handling c"
last_modified_at: 2024-08-08T21:41:32Z
---

Provides methods for exporting data to XML or CSV formats.
This class includes functionality for transforming data using XSLT, logging, and handling cancellation tokens.

**Namespace:** ASNA.DataGate.Client.CopyData
**Assembly:** ASNA.QSys.DataGate.Client.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>

## Properties

| Type | Name | Description
| --- | --- | --- 
| [ExportAccessMode](/reference/datagate/datagate-client/export-access-mode.html) | AccessPath | Gets or sets the access mode for data export. |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | DetailedFeedback | Gets or sets a value indicating whether detailed feedback is enabled. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | QueryExpression | Gets or sets the query expression to be used for data export. |
| [IDictionary\<String, KeyUsages\>](https://docs.microsoft.com/en-us/dotnet/api/system.collections.generic.idictionary-2) | QueryKeys | Gets the query keys to be used for data export. |
| [IMember](/reference/datagate/datagate-client/i-member.html) | SourceData | Gets or sets the source data to be exported. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | TargetPath | Gets or sets the target path where the data will be exported. |
