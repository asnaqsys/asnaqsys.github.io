---
title: "FileAdapter.ChangeRRN Method"
description: "Changes the contents of the record at the specified relative record number (RRN)."
---

## Definition

**Namespace:** ASNA.DataGate.Client  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Changes the contents of the record at the specified relative record number (RRN). This operation is not valid for SQL Server.


```cs
public void ChangeRRN(AdgDataSet ds, long RRN)
```

#### Parameters

| Type | Parameter name | Description |
| --- | --- | --- |
| [AdgDataSet](/reference/datagate/datagate-client/adg-data-set.html) | ds | The AdgDataSet containing the data for the new record. |
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | RRN | The relative record number of the record to change to. |

## Remarks

 **ChangeRRN** is similar to [ChangeCurrent](file-adapter-changecurrent.html), which updates database file records.  Whereas **ChangeCurrent** allows the current record to be updated, **ChangeRRN** permits update to a record with the specified relative record number.


## See Also
- [FileAdapter class](file-adapter.html)
- [FileAdapter.ChangeCurrent](file-adapter-changecurrent.html)
