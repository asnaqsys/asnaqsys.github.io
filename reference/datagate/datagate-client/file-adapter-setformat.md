---
title: "FileAdapter.SetFormat Method"
description: "Sets the format of the file that the FileAdapter is working with to the specified format."
---

## Definition

**Namespace:** ASNA.DataGate.Client  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Sets the format of the file that the FileAdapter is working with to the specified format.

```cs
void SetFormat(string Format)
```

#### Parameters

| Type | Parameter name | Description |
| --- | --- | --- |
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | Format | The name of the format to set. |

## Remarks
 
The default behavior of **FileAdapter** is to read all formats.  Use this method to change an open file to read only records of the given format.  To switch back to "read all records" mode, use the `ResetFormat` method.  This method has no effect if the file is not a multiformat file.


## See Also
- [FileAdapter class](file-adapter.html)
