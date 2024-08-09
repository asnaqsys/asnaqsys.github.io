---
title: "ImportFromCsvOptions class    | QSYS API Reference Guide"
description: "Represents options for importing data from a CSV file. "
last_modified_at: 2024-08-09T16:18:40Z
---

Represents options for importing data from a CSV file.

**Namespace:** ASNA.DataGate.Client.CopyData
**Assembly:** ASNA.QSys.DataGate.Client.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [ImportOptions](/reference/datagate/datagate-client/import-options.html)
<br>
<br>

## Remarks
The ImportFromCsvOptions class inherits from the ImportOptions class and adds additional properties specific to CSV data import.
These properties include SkipFirstLine, TextDelimiter, FieldDelimiter, and DecimalPoint.
The SkipFirstLine property indicates whether the first line of the CSV data should be skipped during the import.
The TextDelimiter property specifies the text delimiter for the CSV data.
The FieldDelimiter property specifies the field delimiter for the CSV data.
The DecimalPoint property specifies the decimal point for the CSV data.

<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [ImportFromCsvOptions](#importfromcsvoptionsimember-string)([IMember](/reference/datagate/datagate-client/i-member.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Initializes a new instance of the  class with the specified target member and source path.
| [ImportFromCsvOptions](#importfromcsvoptionsimember-string-boolean)([IMember](/reference/datagate/datagate-client/i-member.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Initializes a new instance of the  class with the specified target member, source path, and clear member flag.
| [ImportFromCsvOptions](#importfromcsvoptionsimember-string-boolean-boolean)([IMember](/reference/datagate/datagate-client/i-member.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Initializes a new instance of the  class with the specified target member, source path, clear member flag, use target connection flag, and detailed feedback flag.
| [ImportFromCsvOptions](#importfromcsvoptionsimember-string-boolean-boolean-boolean)([IMember](/reference/datagate/datagate-client/i-member.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Initializes a new instance of the  class with the specified target member, source path, clear member flag, use target connection flag, and skip first line flag.

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

## Properties

| Type | Name | Description
| --- | --- | --- 
| [Char](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/char) | DecimalPoint | Gets or sets the decimal point for the CSV data. |
| [Nullable\<Char\>](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/nullable-value-types) | FieldDelimiter | Gets or sets the field delimiter for the CSV data. |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | SkipFirstLine | Gets or sets a value indicating whether the first line of the CSV data should be skipped during the import. |
| [Nullable\<Char\>](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/nullable-value-types) | TextDelimiter | Gets or sets the text delimiter for the CSV data. |
