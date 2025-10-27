---
title: "AdgDataSet.GetFormatName Method"
description: "Retrieves the format name associated with the specified format index."
---

## Definition

**Namespace:** ASNA.DataGate.Client  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Retrieves the format name associated with the specified format index.

```cs
string GetFormatName(int iFormat)
```

#### Parameters

| Type | Parameter name | Description |
| --- | --- | --- |
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | iFormat | The format index. |

#### Returns

| Type | Description |
| --- | --- |
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The format name associated with the specified format index. |

## Remarks

In **AdgDataSet,** DataTables corresponding to DataGate file formats are identified in two ways:
 - By Format Name or
 - By Integer Index

**GetFormatName** provides a way to obtain the format name, given an integer index. The number of formats defined in the **AdgDataSet** is given by the **Formats** property. Valid values for _iFormat_ are in the range `0 ≤ _iFormat_ < AdgDataSet.Formats`.  If _iFormat_ is an invalid index, **GetFormatName** throws dgException with the Error property set to dgEINVARG.


## See Also
- [AdgDataSet class](adg-data-set.html)
