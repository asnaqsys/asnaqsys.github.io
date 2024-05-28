---
title: AdgTable class
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
| [AdgTable](#adgtabledatatable-adgdataset)([DataTable](https://learn.microsoft.com/en-us/dotnet/api/system.data.datatable.select?view=net-8.0), [AdgDataSet](/reference/datagate/datagate-client/adg-data-set.html)) | Initializes a new instance of the  class with a specified DataTable and parent AdgDataSet.

### AdgTable([DataTable](https://learn.microsoft.com/en-us/dotnet/api/system.data.datatable.select?view=net-8.0), [AdgDataSet](/reference/datagate/datagate-client/adg-data-set.html))

Initializes a new instance of the  class with a specified DataTable and parent AdgDataSet.

```cs
AdgTable(DataTable, AdgDataSet)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DataTable](https://learn.microsoft.com/en-us/dotnet/api/system.data.datatable.select?view=net-8.0) | table | 
| [AdgDataSet](/reference/datagate/datagate-client/adg-data-set.html) | parent | 

## Properties

| Type | Name | Description
| --- | --- | --- 
| [DataTable](https://learn.microsoft.com/en-us/dotnet/api/system.data.datatable.select?view=net-8.0) | DataTable | Gets the DataTable associated with this instance of the AdgTable. |
| [DataRow](https://learn.microsoft.com/en-us/dotnet/api/system.data.datarow?view=net-8.0) | Row | Gets the current active DataRow in the AdgTable. |

## Methods

| Signature | Description |
| --- | --- |
| [SetRowDefaultValues](#void-setrowdefaultvaluesdatarow-row)([DataRow](https://learn.microsoft.com/en-us/dotnet/api/system.data.datarow?view=net-8.0)) | Sets the default values for each column in the provided DataRow.

### void SetRowDefaultValues([DataRow row](https://learn.microsoft.com/en-us/dotnet/api/system.data.datarow?view=net-8.0))

Sets the default values for each column in the provided DataRow.

```cs
void SetRowDefaultValues(DataRow row)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DataRow](https://learn.microsoft.com/en-us/dotnet/api/system.data.datarow?view=net-8.0) | row | 
