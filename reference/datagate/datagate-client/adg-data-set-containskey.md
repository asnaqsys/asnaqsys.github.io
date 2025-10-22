---
title: "AdgDataSet.ContainsKey Method"
description: "Determines whether the AdgDataSet contains an AdgTable with the specified format index."
---

## Definition

**Namespace:** ASNA.DataGate.Client  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Determines whether the AdgDataSet contains an AdgTable with the specified format index.

```cs
bool ContainsKey(int key)
```

#### Parameters

| Type | Parameter name | Description |
| --- | --- | --- |
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | key | The format index to locate in the AdgDataSet. |

#### Returns

| Type | Description |
| --- | --- |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | True if an AdgTable with the specified format index exists; otherwise, false. |

## Remarks
Calls the ContainsKey method of the internal dictionary with the provided format index.

## See Also
- [AdgDataSet class](adg-data-set.html)
