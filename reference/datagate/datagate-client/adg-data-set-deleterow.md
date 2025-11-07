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
 
**DeleteRow** marks the DataRow object specified by _rrn_ as deleted in the format table specified by _strFormat_. Upon return, the `ActiveRow Property` of the **AdgDataSet** is set to null and the RowState of the DataRow is RowDeleted.
 
The _rrn_ parameter is a zero-relative index referring to a DataRow object contained in the Rows collection of the DataTable corresponding to the _strFormat_ parameter.  The Rows collection and its containing DataTable object is accessible via the [GetFormatTable](adg-data-set-getformattable.html) method.

## See Also
- [AdgDataSet class](adg-data-set.html)
