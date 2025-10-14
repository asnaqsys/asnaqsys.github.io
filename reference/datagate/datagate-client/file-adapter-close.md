---
title: "FileAdapter.Close Method"
description: "Closes the FileAdapter and releases all resources used by it."
---

## Definition

**Namespace:** ASNA.DataGate.Client  
**Assembly:** ASNA.QSys.DataGate.Client.dll


Closes the FileAdapter and releases all resources used by it.

```cs
public void Close()
```

## Remarks
Use the **Close** or **Dispose** methods to close a file opened by a previous call to one of the open methods (`Open`,`OpenNewAdgDataSet`). After a successful **Close** or **Dispose** call, the file may be subsequently reopened using the same **FileAdapter** object’s open methods.
 
**Close** releases unmanaged resources associated with the **FileAdapter**, via the **Dispose** method.


## See Also
- [FileAdapter class](file-adapter.html)
