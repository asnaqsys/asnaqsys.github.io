---
title: "IFileAdapter interface.ReadSequentialEqual Method"
description: "Reads the file sequentially with the specified dataset, read mode, and lock request."
---

## Definition

**Namespace:** ASNA.DataGate.Providers  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Reads the file sequentially with the specified dataset, read mode, and lock request.

<a id="void-readsequentialequal-adgdataset-ds-readsequentialmode-rm-lockrequest-lr"></a>
## void ReadSequentialEqual(AdgDataSet ds, ReadSequentialMode rm, LockRequest lr)

Reads the file sequentially with the specified dataset, read mode, and lock request.

```cs
void ReadSequentialEqual(AdgDataSet ds, ReadSequentialMode rm, LockRequest lr)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [AdgDataSet](/reference/datagate/datagate-client/adg-data-set.html) | ds | The dataset to use when reading the file.
| [ReadSequentialMode](/reference/datagate/datagate-common/read-sequential-mode.html) | rm | The read mode to use when reading the file.
| [LockRequest](/reference/datagate/datagate-common/lock-request.html) | lr | The lock request to use when reading the file.

## See Also
- [IFileAdapter interface class](i-file-adapter.html)
