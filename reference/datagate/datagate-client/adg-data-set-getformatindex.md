---
title: "AdgDataSet.GetFormatIndex Method"
description: "Retrieves the format index associated with the specified format name."
---

## Definition

**Namespace:** ASNA.DataGate.Client  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Retrieves the format index associated with the specified format name.

```cs
int GetFormatIndex(string strFormat)
```

#### Parameters

| Type | Parameter name | Description |
| --- | --- | --- |
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | strFormat | The format name to retrieve the index for. |

#### Returns

| Type | Description |
| --- | --- |
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | The format index associated with the specified format name. |

## Remarks
Iterates over the format strings to find the format name; throws a dgException if not found. Used by methods like GetFormatTable, SetActive, and AddRow.

## See Also
- [AdgDataSet class](adg-data-set.html)
