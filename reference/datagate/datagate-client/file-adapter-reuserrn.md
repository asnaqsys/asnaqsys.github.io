---
title: "FileAdapter.ReuseRRN Method"
description: "Reuses the record at the specified relative record number (RRN) in the file that the FileAdapter is working with."
---

## Definition

**Namespace:** ASNA.DataGate.Client  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Reuses the record at the specified relative record number (RRN) in the file that the FileAdapter is working with, by updating the contents of the specified record and marking it as undeleted.

```cs
void ReuseRRN(AdgDataSet ds, long RRN)
```

#### Parameters

| Type | Parameter name | Description |
| --- | --- | --- |
| [AdgDataSet](/reference/datagate/datagate-client/adg-data-set.html) | ds | The AdgDataSet to fill with the data from the record. |
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | RRN | The relative record number of the record to reuse. |


## See Also
- [FileAdapter class](file-adapter.html)
