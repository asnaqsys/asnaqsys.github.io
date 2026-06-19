---
title: "AdgKeyTable class"
description: "The AdgKeyTable class contains a DataTable object for manipulating key values. "
last_modified_at: 2024-08-09T17:25:07Z
---

The AdgKeyTable class contains a DataTable object for manipulating key values.

**Namespace:** ASNA.DataGate.Client
**Assembly:** ASNA.QSys.DataGate.Client.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [AdgTable](/reference/datagate/datagate-client/adg-table.html)
<br>
<br>
## Thread Safety

Any public static (Shared) members of this type are safe for multithreaded operations. Any instance members are not guaranteed to be thread safe.


## Constructors

| Name | Description |
| --- | --- |
| [AdgKeyTable](adg-key-table-ctor.html#adgkeytable-datatable)([DataTable](https://learn.microsoft.com/en-us/dotnet/api/system.data.datatable)) | Initializes a new instance of the  class with a specified key table template.

## Properties

| Type | Name | Description
| --- | --- | --- 
| [DataRowColumnComparer\<DataRow\>](/reference/datagate/datagate-client/data-row-column-comparer-1.html) | Comparer | Gets the DataRowColumnComparer used for comparing rows in the key table. |
| [DataTable](https://learn.microsoft.com/en-us/dotnet/api/system.data.datatable) | DataTable | Gets the DataTable associated with this instance of the AdgTable. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | KeyPartCount | Gets or sets the number of key parts in the key table. |
| [DataRow](https://learn.microsoft.com/en-us/dotnet/api/system.data.datarow) | Row | Gets the current active DataRow in the AdgTable. |

## Methods

| Signature | Description |
| --- | --- |
| [Equals](adg-key-table-equals.html#bool-equals-datarow-other)([DataRow](https://learn.microsoft.com/en-us/dotnet/api/system.data.datarow)) | Determines whether the specified DataRow is equal to the current DataRow.

## Example 1. Creating a Key Table to read records by Key. Also uses Row property.

```cs 
/* This example will open a file and find the record for
     the customer "Thilmany of Bread Co Resources".
     It omits error trapping for clarity's sake. */

  AdgConnection db = createAdgConnection("MyLocalDB");
  db.Open();
  FileAdapter file = new FileAdapter(db);
  file.FileName = "Examples//CMastNewL2";
  AdgDataSet dataSet;
  file.OpenNewAdgDataSet( out dataSet );

  //This next line creates a key based on record format RCMMastL2
  AdgKeyTable key = dataSet.NewKeyTable("RCMMastL2");

  //We specify KeyPartCount to avoid specifying the second
  //key field.
  //We then set the keyfield "CMName" to our search argument.
  key.KeyPartCount = 1;
  key.Row["CMName"] = "Thilmany Of Bread Co Resources";

  //The following read will find the record associated with the 
  //customer name "Thilmany Of Bread Co Resources" and store it
  //in dataSet.
  file.ReadRandomKey(dataSet, ReadRandomMode.Equal, LockRequest.Default, key);
```

> See [AdgConnection Example](/reference/datagate/datagate-client/adg-connection.html#create-an-adgconnection) for an implementation of `createAdgConnection()`


