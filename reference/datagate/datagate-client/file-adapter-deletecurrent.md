---
title: "FileAdapter.DeleteCurrent Method"
description: "Deletes the current record from the file that the FileAdapter is working with."
---

## Definition

**Namespace:** ASNA.DataGate.Client  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Deletes the current record from the file that the FileAdapter is working with.

```cs
void DeleteCurrent()
```

## Remarks

The current record of an open file is marked as deleted by **DeleteCurrent**. After the delete, any lock on the record is released. The file should be opened with the `AccessMode` property set to a value including the `AccessMode.Delete` flag in order to permit delete access to the file.

Once the record is deleted it cannot be read anymore. 

## See Also
- [FileAdapter class](file-adapter.html)
