---
title: "FileAdapter.DeleteRRN Method"
description: "Deletes the record at the specified relative record number (RRN) from the file that the FileAdapter is working with."
---

## Definition

**Namespace:** ASNA.DataGate.Client  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Deletes the record at the specified relative record number (RRN) from the file that the FileAdapter is working with.

```cs
void DeleteRRN(long RRN)
```

#### Parameters

| Type | Parameter name | Description |
| --- | --- | --- |
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | RRN | The relative record number of the record to delete. |


## Remarks

**DeleteRRN** deletes a record in the open file containing a specified relative record number. First, a search for a record containing the relative record number is performed. If such a record is not found, the method throws dgException. If the record is found, it is set to be the current record of the file, and subsequently deleted.
 
The file should be opened with the `AccessMode` property set to a value including the `AccessMode.Delete`flag, in order to permit delete access to the file.

As SQL Server does not have the concept of a relative record number, this operation is not available on SQL Server.


## See Also
- [FileAdapter class](file-adapter.html)
