---
title: "AdgDataSet.DeleteRow Method"
description: "Deletes the row at the specified RRN in the DataTable for the given format name."
---

## Definition

**Namespace:** ASNA.DataGate.Client  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Deletes the row at the specified relative record number (rrn) in the DataTable associated with the specified format name.

```cs
void DeleteRow(string strFormat, int rrn)
```

#### Parameters

| Type | Parameter name | Description |
| --- | --- | --- |
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | strFormat | The format name of the DataTable. |
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | rrn | The relative record number of the row to delete. |

## Remarks
Sets the active row using SetActive; if not found, throws ArgumentException. Otherwise, deletes the active row via the corresponding AdgTable.

## See Also
- [AdgDataSet class](adg-data-set.html)
