---
title: "PrintFileOpenAttr class       | QSYS API Reference Guide"
description: "Represents the attributes for opening a print file. "
last_modified_at: 2024-08-09T16:18:40Z
---

Represents the attributes for opening a print file.

**Namespace:** ASNA.DataGate.Providers
**Assembly:** ASNA.QSys.DataGate.Client.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [Hashtable](https://learn.microsoft.com/en-us/dotnet/api/system.collections.hashtable?view=net-8.0) --> [FileOpenAttr](/reference/datagate/datagate-providers/file-open-attr.html)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [PrintFileOpenAttr()](#printfileopenattr) | Initializes a new instance of the PrintFileOpenAttr class.

### PrintFileOpenAttr()

Initializes a new instance of the PrintFileOpenAttr class.

```cs
PrintFileOpenAttr()
```

## Properties

| Type | Name | Description
| --- | --- | --- 
| [PrintDevAttr](/reference/datagate/datagate-providers/print-dev-attr.html) | DevAttr | Gets or sets the device attributes for the print file to be opened. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | DocumentName | Gets or sets the name of the document for the print file to be opened. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | FormType | Gets or sets the form type for the print file to be opened. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | PrintToFileName | Gets or sets the name of the file to which the print file will be printed. |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | ProcessMacros | Gets or sets a value indicating whether macros should be processed when the print file is opened. |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | Prompt | Gets or sets a value indicating whether a prompt should be displayed when the print file is opened. |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | SaveAfter | Gets or sets a value indicating whether the print file should be saved after being opened. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | UserData | Gets or sets the user data for the print file to be opened. |
