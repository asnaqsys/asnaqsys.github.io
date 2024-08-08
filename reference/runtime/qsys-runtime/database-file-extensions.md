---
title: "DatabaseFileExtensions class  | QSYS API Reference Guide"
description: "Defines a collection of extension methods to aid in operating with the file&#39;s dataset. "
last_modified_at: 2024-08-08T21:41:46Z
---

Defines a collection of extension methods to aid in operating with the file's dataset.

**Namespace:** ASNA.QSys.Runtime
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>

## Methods

| Signature | Description |
| --- | --- |
| [GetAdgTable](#adgtable-getadgtableadgdataset-dataset-string-formatname)([AdgDataSet](/reference/datagate/datagate-client/adg-data-set.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Finds the data table/record format in the file represented  dataset.
| [SetActive](#adgtable-setactiveadgdataset-dataset-string-formatname)([AdgDataSet](/reference/datagate/datagate-client/adg-data-set.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Sets the active record format in a file and returns it.

### AdgTable GetAdgTable([AdgDataSet dataSet](/reference/datagate/datagate-client/adg-data-set.html), [string formatName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Finds the data table/record format in the file represented  dataset.

```cs
AdgTable GetAdgTable(AdgDataSet dataSet, string formatName)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [AdgDataSet](/reference/datagate/datagate-client/adg-data-set.html) | dataSet | The AdgDataSet that represents the file to query for a table.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatName | The table name, or "*FILE" to return the only table in a single format file.

#### Returns

| Type | Description
| --- | ---
| [AdgTable](/reference/datagate/datagate-client/adg-table.html) | The record format as an AdgTable object of the table that matches the given name in the dataset.

### AdgTable SetActive([AdgDataSet dataSet](/reference/datagate/datagate-client/adg-data-set.html), [string formatName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Sets the active record format in a file and returns it.

```cs
AdgTable SetActive(AdgDataSet dataSet, string formatName)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [AdgDataSet](/reference/datagate/datagate-client/adg-data-set.html) | dataSet | The AdgDataSet that represents the file.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatName | The table name, or "*FILE" to select the only table in a single format file.

#### Returns

| Type | Description
| --- | ---
| [AdgTable](/reference/datagate/datagate-client/adg-table.html) | The active record format AdgTable object.
