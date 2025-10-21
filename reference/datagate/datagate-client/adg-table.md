---
title: "AdgTable class                | QSYS API Reference Guide"
description: "The AdgTable class supports DG infrastructure and is not intended to be used directly from your code. "
last_modified_at: 2024-08-09T17:25:07Z
---

The AdgTable class supports DG infrastructure and is not intended to be used directly from your code.

**Namespace:** ASNA.DataGate.Client
**Assembly:** ASNA.QSys.DataGate.Client.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [AdgTable](#adgtabledatatable-adgdataset)([DataTable](https://learn.microsoft.com/en-us/dotnet/api/system.data.datatable), [AdgDataSet](/reference/datagate/datagate-client/adg-data-set.html)) | Initializes a new instance of the  class with a specified DataTable and parent AdgDataSet.

### AdgTable([DataTable](https://learn.microsoft.com/en-us/dotnet/api/system.data.datatable), [AdgDataSet](/reference/datagate/datagate-client/adg-data-set.html))

Initializes a new instance of the  class with a specified DataTable and parent AdgDataSet.

```cs
AdgTable(DataTable, AdgDataSet)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DataTable](https://learn.microsoft.com/en-us/dotnet/api/system.data.datatable) | table | The DataTable to be associated with this instance.
| [AdgDataSet](/reference/datagate/datagate-client/adg-data-set.html) | parent | The parent AdgDataSet to which this AdgTable belongs.

## Properties

| Type | Name | Description
| --- | --- | --- 
| [DataTable](https://learn.microsoft.com/en-us/dotnet/api/system.data.datatable) | DataTable | Gets the DataTable associated with this instance of the AdgTable. |
| [DataRow](https://learn.microsoft.com/en-us/dotnet/api/system.data.datarow) | Row | Gets the current active DataRow in the AdgTable. |

## Methods

| Signature | Description |
| --- | --- |
| [SetRowDefaultValues](#void-setrowdefaultvaluesdatarow-row)([DataRow](https://learn.microsoft.com/en-us/dotnet/api/system.data.datarow)) | Sets the default values for each column in the provided DataRow.

### void SetRowDefaultValues([DataRow row](https://learn.microsoft.com/en-us/dotnet/api/system.data.datarow))

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
