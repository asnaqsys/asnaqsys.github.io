---
title: "AdgTable class"
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
| [AdgTable](adg-table-ctor.html#adgtable-datatable-adgdataset)([DataTable](https://learn.microsoft.com/en-us/dotnet/api/system.data.datatable), [AdgDataSet](/reference/datagate/datagate-client/adg-data-set.html)) | Initializes a new instance of the  class with a specified DataTable and parent AdgDataSet.

## Properties

| Type | Name | Description
| --- | --- | --- 
| [DataTable](https://learn.microsoft.com/en-us/dotnet/api/system.data.datatable) | DataTable | Gets the DataTable associated with this instance of the AdgTable. |
| [DataRow](https://learn.microsoft.com/en-us/dotnet/api/system.data.datarow) | Row | Gets the current active DataRow in the AdgTable. |

## Methods

| Signature | Description |
| --- | --- |
| [SetRowDefaultValues](adg-table-setrowdefaultvalues.html#void-setrowdefaultvalues-datarow-row)([DataRow](https://learn.microsoft.com/en-us/dotnet/api/system.data.datarow)) | Sets the default values for each column in the provided DataRow.

