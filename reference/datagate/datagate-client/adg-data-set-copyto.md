---
title: "AdgDataSet.CopyTo Method"
description: "Copies the elements of the AdgDataSet to an array, starting at a particular array index."
---

## Definition

**Namespace:** ASNA.DataGate.Client  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Copies the elements of the AdgDataSet to an array, starting at a particular array index.

```cs
void CopyTo(KeyValuePair`2[] array, int arrayIndex)
```

#### Parameters

| Type | Parameter name | Description |
| --- | --- | --- |
| [KeyValuePair`2\[\]](https://learn.microsoft.com/en-us/dotnet/api/system.collections.generic.keyvaluepair-2?view=net-8.0) | array | The destination array. |
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | arrayIndex | The zero-based index in the array at which copying begins. |

## Remarks
Calls the CopyTo method of the underlying dictionary with the provided array and array index.

## See Also
- [AdgDataSet class](adg-data-set.html)
