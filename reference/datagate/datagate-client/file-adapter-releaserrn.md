---
title: "FileAdapter.ReleaseRRN Method"
description: "Releases the lock on the record at the specified relative record number (RRN)."
---

## Definition

**Namespace:** ASNA.DataGate.Client  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Releases the lock on the record at the specified relative record number (RRN) in the file that the FileAdapter is working with.

```cs
void ReleaseRRN(LockRequest lr, long RRN)
```

#### Parameters

| Type | Parameter name | Description |
| --- | --- | --- |
| [LockRequest](/reference/datagate/datagate-common/lock-request.html) | lr | The LockRequest to use when releasing the lock. |
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | RRN | The relative record number of the record to release the lock on. |

## Remarks
 
**FileAdapter** methods which read, update, and add records may also optionally lock the current record associated with those operations, in compliance with the rules of the database provider.   **ReleaseRRN** allows programs to release a locked record if by providing the relative record number of the record.

When a **FileAdapter** is using manual locks, multiple records of a file may be locked, **ReleaseRRN** enable the program to selectively release individual records.

The _lr_ parameter specifies the record locks to release. DG supports the **LockRequest.Write** and **LockRequest.Read** flags as valid components of the _lr_ parameter value.

## See Also
- [FileAdapter class](file-adapter.html)
