---
title: "FileAdapter.ReadRandomRRN Method"
description: "Reads a record from the file that the FileAdapter is working with using the specified relative record number (RRN)."
---

## Definition

**Namespace:** ASNA.DataGate.Client  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Reads a record from the file that the FileAdapter is working with using the specified relative record number (RRN).

```cs
void ReadRandomRRN([AdgDataSet ds, ReadRandomMode mode, LockRequest lr, long RRN)
```

#### Parameters

| Type | Parameter name | Description |
| --- | --- | --- |
| [AdgDataSet](/reference/datagate/datagate-client/adg-data-set.html) | ds | The AdgDataSet to fill with the data from the record. |
| [ReadRandomMode](/reference/datagate/datagate-common/read-random-mode.html) | mode | The ReadRandomMode to use when reading the record. |
| [LockRequest](/reference/datagate/datagate-common/lock-request.html) | lr | The LockRequest to use when reading the record. |
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | RRN | The relative record number of the record to read. |


## Remarks

This method reads a file record specified by relative-record number (_RRN_), or an arrival-oriented location in the file.  If no such _RRN_ exists in the file the method throws dgException, with the Error property set to dgEaNOTFND.
 
If the operation is successful, the record read is placed in the specified **AdgDataSet** object. The record is appended to a DataTable in the **AdgDataSet** corresponding to the record format.  The record is appended as a DataRow object in the DataTable, and the `AdgDataSet.ActiveRow`property will reference this DataRow on return.  
 
A successful read operation optionally locks the record read as directed by the _lr_ parameter and the locking properties of the file.
 
The _mode_ parameter is currently ignored.  To maintain your code’s compatibility with future enhancements, please use the value **ReadRandomMode.Equal** for this parameter.
 
Calling this method cancels "range mode".  A prior successful call to `ReadRange`or `SeekRange` places the **FileAdapter** in range mode, in which only records with keys in a specified range are accessed.  This method cancels the restriction.


## See Also
- [FileAdapter class](file-adapter.html)
