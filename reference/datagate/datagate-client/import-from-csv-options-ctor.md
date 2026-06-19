---
title: "ImportFromCsvOptions Constructors"
description: "Initializes a new instance of the class with the specified target member and source path."
---

## Definition

**Namespace:** ASNA.DataGate.Client.CopyData  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Initializes a new instance of the class with the specified target member and source path.

## Overloads

| Name | Description |
| --- | --- |
| [ImportFromCsvOptions](#importfromcsvoptions-imember-string)([IMember](/reference/datagate/datagate-client/i-member.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Initializes a new instance of the class with the specified target member and source path. |
| [ImportFromCsvOptions](#importfromcsvoptions-imember-string-boolean)([IMember](/reference/datagate/datagate-client/i-member.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Initializes a new instance of the class with the specified target member, source path, and clear member flag. |
| [ImportFromCsvOptions](#importfromcsvoptions-imember-string-boolean-boolean)([IMember](/reference/datagate/datagate-client/i-member.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Initializes a new instance of the class with the specified target member, source path, clear member flag, use target connection flag, and detailed feedback flag. |
| [ImportFromCsvOptions](#importfromcsvoptions-imember-string-boolean-boolean-boolean)([IMember](/reference/datagate/datagate-client/i-member.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Initializes a new instance of the class with the specified target member, source path, clear member flag, use target connection flag, and skip first line flag. |

<a id="importfromcsvoptions-imember-string"></a>
### ImportFromCsvOptions([IMember](/reference/datagate/datagate-client/i-member.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Initializes a new instance of the  class with the specified target member and source path.

```cs
ImportFromCsvOptions(IMember, String)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [IMember](/reference/datagate/datagate-client/i-member.html) | target | The target member where the data will be imported.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | source | The source path from where the data will be imported.

<a id="importfromcsvoptions-imember-string-boolean"></a>
### ImportFromCsvOptions([IMember](/reference/datagate/datagate-client/i-member.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Initializes a new instance of the  class with the specified target member, source path, and clear member flag.

```cs
ImportFromCsvOptions(IMember, String, Boolean)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [IMember](/reference/datagate/datagate-client/i-member.html) | target | The target member where the data will be imported.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | source | The source path from where the data will be imported.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | bClearMember | A flag indicating whether the target member should be cleared before the import.

<a id="importfromcsvoptions-imember-string-boolean-boolean"></a>
### ImportFromCsvOptions([IMember](/reference/datagate/datagate-client/i-member.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Initializes a new instance of the  class with the specified target member, source path, clear member flag, use target connection flag, and detailed feedback flag.

```cs
ImportFromCsvOptions(IMember, String, Boolean, Boolean)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [IMember](/reference/datagate/datagate-client/i-member.html) | target | The target member where the data will be imported.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | source | The source path from where the data will be imported.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | bClearMember | A flag indicating whether the target member should be cleared before the import.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | bUseTargetConnection | A flag indicating whether the target connection should be used for the import.

<a id="importfromcsvoptions-imember-string-boolean-boolean-boolean"></a>
### ImportFromCsvOptions([IMember](/reference/datagate/datagate-client/i-member.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Initializes a new instance of the  class with the specified target member, source path, clear member flag, use target connection flag, and skip first line flag.

```cs
ImportFromCsvOptions(IMember, String, Boolean, Boolean, Boolean)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [IMember](/reference/datagate/datagate-client/i-member.html) | target | The target member where the data will be imported.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | source | The source path from where the data will be imported.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | bClearMember | A flag indicating whether the target member should be cleared before the import.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | bUseTargetConnection | A flag indicating whether the target connection should be used for the import.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | bSkipFirstLine | A flag indicating whether the first line of the CSV data should be skipped during the import.

## See Also
- [ImportFromCsvOptions class](import-from-csv-options.html)
