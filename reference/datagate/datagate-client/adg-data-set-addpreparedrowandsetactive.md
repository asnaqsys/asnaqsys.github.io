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
 
**AddPreparedRowAndSetActive** combines the operations performed by the `AddRow`and `SetActive` methods into a single method call.  First, a prepared row is added to the specified format table, just as if **AddRow**(_iFormat_) had been called.  Then the row just added to the table is set to be the `ActiveRow` for the **AdgDataSet**, like using **SetActive**.  This is useful when adding a record format that is to be immediately used in a `FileAdapter` method which operates upon the **ActiveRow**, such as `AddRecord`.
 
The usual pattern of use involves first staging the prepared DataRow object via `PrepareRow`setting the field values in the DataRow as necessary, then calling **AddRow** or **AddPreparedRowAndSetActive** to append the row to the table.
 
 Note that prior to calling this method, you must call **PrepareRow** to stage a prepared row for insertion to the table.  Also, upon return from this method, the prepared row of the table remains the row added to the table.  Calling **AddRow** or **AddPreparedRowAndSetActive** again before calling **PrepareRow** will cause an exception.


## See Also
- [AdgDataSet class](adg-data-set.html)
