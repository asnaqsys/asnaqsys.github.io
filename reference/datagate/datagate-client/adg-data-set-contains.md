---
title: "AdgDataSet.Contains Method"
description: "Determines whether the AdgDataSet contains a specific key-value pair."
---

## Definition

**Namespace:** ASNA.DataGate.Client  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Determines whether the AdgDataSet contains a specific key-value pair.

```cs
bool Contains(KeyValuePair<int, AdgTable> item)
```

#### Parameters

| Type | Parameter name | Description |
| --- | --- | --- |
| [KeyValuePair\<Int32, AdgTable\>](https://learn.microsoft.com/en-us/dotnet/api/system.collections.generic.keyvaluepair-2?view=net-8.0) | item | The key-value pair to locate in the AdgDataSet. |

#### Returns

| Type | Description |
| --- | --- |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | True if the key-value pair exists; otherwise, false. |

## Remarks
Calls the Contains method of the internal dictionary with the provided key-value pair.

## See Also
- [AdgDataSet class](adg-data-set.html)
