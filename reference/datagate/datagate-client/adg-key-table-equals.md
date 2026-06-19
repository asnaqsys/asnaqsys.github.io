---
title: "AdgKeyTable.Equals Method"
description: "Determines whether the specified DataRow is equal to the current DataRow."
---

## Definition

**Namespace:** ASNA.DataGate.Client  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Determines whether the specified DataRow is equal to the current DataRow.

<a id="bool-equals-datarow-other"></a>
## bool Equals(DataRow other)

Determines whether the specified DataRow is equal to the current DataRow.

#### Remarks
This method uses the DataRowColumnComparer associated with this AdgKeyTable instance to compare the specified DataRow with the current DataRow.The DataRowColumnComparer compares the rows based on the first m_cParts columns of the DataTable associated with this AdgKeyTable instance.

```cs
bool Equals(DataRow other)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DataRow](https://learn.microsoft.com/en-us/dotnet/api/system.data.datarow) | other | The DataRow to compare with the current DataRow.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | true if the specified DataRow is equal to the current DataRow; otherwise, false.

## See Also
- [AdgKeyTable class](adg-key-table.html)
