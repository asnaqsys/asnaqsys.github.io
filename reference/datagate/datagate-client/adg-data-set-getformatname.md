---
title: "AdgDataSet.GetFormatName Method"
description: "Retrieves the format name associated with the specified format index."
---

## Definition

**Namespace:** ASNA.DataGate.Client  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Retrieves the format name associated with the specified format index.

```cs
string GetFormatName(int iFormat)
```

#### Parameters

| Type | Parameter name | Description |
| --- | --- | --- |
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | iFormat | The format index. |

#### Returns

| Type | Description |
| --- | --- |
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The format name associated with the specified format index. |

## Remarks
Validates array bounds and returns the name; throws a dgException if invalid.

## See Also
- [AdgDataSet class](adg-data-set.html)
