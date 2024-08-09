---
title: "DatabaseFileExtensions class  | QSYS API Reference Guide"
description: "Defines a collection of extension methods to aid in operating with the file&#39;s dataset. "
last_modified_at: 2024-08-09T17:25:29Z
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
| [GetUpdatedDataSet](#adgdataset-getupdateddatasetfileadapter-fileadapter-dictionary-string-string-formatids)([FileAdapter](/reference/datagate/datagate-client/file-adapter.html), [Dictionary\<String, String\>](https://learn.microsoft.com/en-us/dotnet/api/system.collections.generic.dictionary-2?view=net-8.0)) | Allocates a file's dataset, to hold the data communicated between the program and the database.
| [SetActive](#adgtable-setactiveadgdataset-dataset-string-formatname)([AdgDataSet](/reference/datagate/datagate-client/adg-data-set.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Sets the active record format in a file and returns it.
| [ToDataSetValues](#ienumerable-object-todatasetvaluesienumerable-object-stronglytypedvalues)([IEnumerable\<Object\>](https://learn.microsoft.com/en-us/dotnet/api/system.collections.generic.ienumerable-1?view=net-8.0)) | Converts a collection of fixed-sized values into a collection of basic .Net scalar types.

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

### AdgDataSet GetUpdatedDataSet([FileAdapter fileAdapter](/reference/datagate/datagate-client/file-adapter.html), [Dictionary\<string, string\> formatIDs](https://learn.microsoft.com/en-us/dotnet/api/system.collections.generic.dictionary-2?view=net-8.0))

Allocates a file's dataset, to hold the data communicated between the program and the database.

```cs
AdgDataSet GetUpdatedDataSet(FileAdapter fileAdapter, Dictionary<string, string> formatIDs)
```

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

### IEnumerable\<object\> ToDataSetValues([IEnumerable\<object\> stronglyTypedValues](https://learn.microsoft.com/en-us/dotnet/api/system.collections.generic.ienumerable-1?view=net-8.0))

Converts a collection of fixed-sized values into a collection of basic .Net scalar types.

```cs
IEnumerable<object> ToDataSetValues(IEnumerable<object> stronglyTypedValues)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [IEnumerable\<Object\>](https://learn.microsoft.com/en-us/dotnet/api/system.collections.generic.ienumerable-1?view=net-8.0) | stronglyTypedValues | Collection of fixed-sized values.

#### Returns

| Type | Description
| --- | ---
| [IEnumerable`1](https://learn.microsoft.com/en-us/dotnet/api/system.collections.generic.ienumerable-1?view=net-8.0) | The converted collection of .Net scalar values.
