---
title: "AdgDataSet.AddPreparedRowAndSetActive Method"
description: "Adds a prepared row to the specified format and sets it as the active row."
---

## Definition

**Namespace:** ASNA.DataGate.Client  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Adds a prepared row to the DataTable associated with the specified format index and sets it as the active row.

```cs
bool AddPreparedRowAndSetActive(int iFormat)
```

#### Parameters

| Type | Parameter name | Description |
| --- | --- | --- |
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | iFormat | The format index of the DataTable. |

#### Returns

| Type | Description |
| --- | --- |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | True if the active row was successfully set; otherwise, false. |

## Remarks
This method is used to add a prepared row to a specific DataTable in the AdgDataSet and set it as the active row. The method retrieves the AdgTable instance from the AdgTable dictionary using the provided format index and calls its AddRow method to add a new row. Then, it sets the NewFormatIndex to the provided format index and calls the SetActive method with the index of the last row in the DataTable to set the new row as the active row. The SetActive method returns true if the active row was successfully set; otherwise, it returns false.

## See Also
- [AdgDataSet class](adg-data-set.html)
