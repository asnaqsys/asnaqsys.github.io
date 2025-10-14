---
title: "FileAdapter.Finalize Method"
description: "Finalizes an instance of the FileAdapter class."
---

## Definition

**Namespace:** ASNA.DataGate.Client  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Finalizes an instance of the FileAdapter class.

```cs
void Finalize()
```

## Remarks

The garbage collector calls `codeFinalize` when the current object is ready to be finalized. Note that **Finalize** does not "close" the ** FileAdapter**.  If the **FileAdapter** represents an open database file, its `Close`or `Dispose` method should be called prior to finalization, or database provider resources may not be properly released.


## See Also
- [FileAdapter class](file-adapter.html)
