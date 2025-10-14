---
title: "FileAdapter.GetPrintProperties Method"
description: "Gets the print properties for the specified format in the file that the FileAdapter is working with."
---

## Definition

**Namespace:** ASNA.DataGate.Client  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Gets the print properties for the specified format in the file that the FileAdapter is working with.

```cs
IPrintProperties? GetPrintProperties(string format)
```

#### Parameters

| Type | Parameter name | Description |
| --- | --- | --- |
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | format | The name of the format to get the print properties for. |

#### Returns

| Type | Description |
| --- | --- |
| [IPrintProperties](/reference/datagate/datagate-providers/i-print-properties.html) | The print properties for the specified format. |

## Remarks
 
The **IPrintProperties** object returned by this method can be used to get and set print file control property values of an open file.  These control properties include fonts, images, and other display characteristics.

If the file is not a print file, the method throws an dgException with the error number dgEcINVFILETYPE.

## See Also
- [FileAdapter class](file-adapter.html)
