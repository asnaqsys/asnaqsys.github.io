---
title: "AdgTable.SetRowDefaultValues Method"
description: "Sets the default values for each column in the provided DataRow."
---

## Definition

**Namespace:** ASNA.DataGate.Client  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Sets the default values for each column in the provided DataRow.

<a id="void-setrowdefaultvalues-datarow-row"></a>
## void SetRowDefaultValues(DataRow row)

Sets the default values for each column in the provided DataRow.

#### Remarks
This method iterates over each DataColumn in the DataRow's table, and sets the value of the DataRow's column to its default value.The default value is determined by the FieldType.GetColumnDefaultValue method, which is not shown in the provided code.An ArgumentNullException is thrown if the provided DataRow is null.

```cs
void SetRowDefaultValues(DataRow row)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DataRow](https://learn.microsoft.com/en-us/dotnet/api/system.data.datarow) | row | The DataRow for which to set default values.

## See Also
- [AdgTable class](adg-table.html)
