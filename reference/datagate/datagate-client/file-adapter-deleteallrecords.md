---
title: "FileAdapter.DeleteAllRecords Method"
description: "Deletes all records from the file that the FileAdapter is working with."
---

## Definition


**Namespace:** ASNA.DataGate.Client  
**Assembly:** ASNA.QSys.DataGate.Client.dll


Deletes all records from the file that the FileAdapter is working with.

```cs
public void DeleteAllRecords()
```

## Remarks

**DeleteAllRecords** clears the file of all records. 

The file should be opened with the `AccessMode` property set to a value including the `AccessMode.Delete` flag in order to permit delete access to the file.


## See Also
- [FileAdapter class](file-adapter.html)
