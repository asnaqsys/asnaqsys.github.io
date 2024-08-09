---
title: "PrintFile class               | QSYS API Reference Guide"
description: "Represents a Database print file. It contains methods to handle all Output operations on the file. "
last_modified_at: 2024-08-09T16:18:25Z
---

Represents a Database print file. It contains methods to handle all Output operations on the file.

**Namespace:** ASNA.QSys.Runtime
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [PrintFileBase](/reference/runtime/qsys-runtime/print-file-base.html)
<br>
<br>

## Properties

| Type | Name | Description
| --- | --- | --- 
| [Dictionary\<String, String\>](https://learn.microsoft.com/en-us/dotnet/api/system.collections.generic.dictionary-2?view=net-8.0) | formatIDs | Dictionary of format names to format IDs. |

## Methods

| Signature | Description |
| --- | --- |
| [Write](#void-writestring-formatname-indicator--optionindicators)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Indicator\[\]](/reference/runtime/qsys-runtime/indicator.html)) | Write a record.

### void Write([string formatName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [Indicator\[\] optionIndicators](/reference/runtime/qsys-runtime/indicator.html))

Write a record.

```cs
void Write(string formatName, Indicator[] optionIndicators)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatName | Name of the record format to write.
| [Indicator\[\]](/reference/runtime/qsys-runtime/indicator.html) | optionIndicators | Indicator array to use in the write operation.
