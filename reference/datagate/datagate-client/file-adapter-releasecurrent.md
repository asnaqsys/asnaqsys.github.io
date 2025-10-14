---
title: "FileAdapter.ReleaseCurrent Method"
description: "Releases the lock on the current record in the file that the FileAdapter is working with."
---

## Definition

**Namespace:** ASNA.DataGate.Client  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Releases the lock on the current record in the file that the FileAdapter is working with.

```cs
void ReleaseCurrent()
```

## Remarks
 
**FileAdapter** methods which read, update, and add records may also optionally lock the current record associated with those operations, in compliance with the rules of the database provider. **ReleaseCurrent** allows programs to release the current lock, if any, on the current record.

Other ways of releasing the current record, when the FileAdapter is using automatic locks, is to to read a different record than the current one; On non SQL Server databases, updating the current record will also release it.

## See Also
- [FileAdapter class](file-adapter.html)
