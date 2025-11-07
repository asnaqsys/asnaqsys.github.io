---
title: "AdgDataSet.GetFormatIndex Method"
description: "Retrieves the format index associated with the specified format name."
---

## Definition

**Namespace:** ASNA.DataGate.Client  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Retrieves the format index associated with the specified format name.

```cs
int GetFormatIndex(string strFormat)
```

#### Parameters

| Type | Parameter name | Description |
| --- | --- | --- |
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | strFormat | The format name to retrieve the index for. |

#### Returns

| Type | Description |
| --- | --- |
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | The format index associated with the specified format name. |

## Remarks

In **AdgDataSet,** DataTables corresponding to DataGate file formats are identified in two ways:
 - By Format Name or
 - By Integer Index

**GetFormatIndex** provides a way to obtain the integer index, given a format name. **GetFormatIndex** does not validate the _strFormat_ parameter.  If _strFormat_ names a format that does not exist in the **AdgDataSet**, the method returns an invalid format index value equal to the current value of the `Formats` property.


## See Also
- [AdgDataSet class](adg-data-set.html)
