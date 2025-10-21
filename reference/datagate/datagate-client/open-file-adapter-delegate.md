---
title: "OpenFileAdapterDelegate Delegate"
description: "Represents the method that will handle the opening of a file adapter."
---

## Definition

**Namespace:** ASNA.DataGate.Client  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Handles the opening of a file adapter and returns an AdgDataSet.

```csharp
public delegate AdgDataSet OpenFileAdapterDelegate(FileAdapter adapter)
```

#### Parameters

| Type | Parameter name | Description |
| --- | --- | --- |
| [FileAdapter](/reference/datagate/datagate-client/file-adapter.html) | adapter | The file adapter to open. |

## Remarks
Use this delegate to supply a method that opens a FileAdapter and returns a corresponding AdgDataSet suitable for operations on the file.

## See Also
- [FileAdapter](/reference/datagate/datagate-client/file-adapter.html)
- [AdgDataSet](/reference/datagate/datagate-client/adg-data-set.html)
