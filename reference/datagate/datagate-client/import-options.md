---
title: "ImportOptions class           | QSYS API Reference Guide"
description: "Provides options for importing data from XML or CSV format. This class includes properties for specifying the target member where the data will be imp"
last_modified_at: 2024-08-09T17:25:07Z
---

Provides options for importing data from XML or CSV format.
This class includes properties for specifying the target member where the data will be imported, the source path from where the data will be imported, whether the target member should be cleared before the import, whether the target connection should be used for the import, and whether detailed feedback should be provided during the import operation.

**Namespace:** ASNA.DataGate.Client.CopyData
**Assembly:** ASNA.QSys.DataGate.Client.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [ImportOptions](#importoptionsimember-string-boolean-boolean)([IMember](/reference/datagate/datagate-client/i-member.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Initializes a new instance of the  class with the specified target member, source path, clear member flag, and use target connection flag.

### ImportOptions([IMember](/reference/datagate/datagate-client/i-member.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Initializes a new instance of the  class with the specified target member, source path, clear member flag, and use target connection flag.

```cs
ImportOptions(IMember, String, Boolean, Boolean)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [IMember](/reference/datagate/datagate-client/i-member.html) | target | The target member where the data will be imported.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | source | The source path from where the data will be imported.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | bClearMember | A flag indicating whether the target member should be cleared before the import.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | bUseTargetConnection | A flag indicating whether the target connection should be used for the import.

## Properties

| Type | Name | Description
| --- | --- | --- 
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | ClearTargetBeforeImport | Gets or sets a value indicating whether the target member should be cleared before the import. |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | DetailedFeedback | Gets or sets a value indicating whether detailed feedback should be provided during the import operation. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | SourcePath | Gets or sets the source path from where the data will be imported. |
| [IMember](/reference/datagate/datagate-client/i-member.html) | TargetMember | Gets or sets the target member where the data will be imported. |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | UseTargetConnection | Gets or sets a value indicating whether the target connection should be used for the import. |
