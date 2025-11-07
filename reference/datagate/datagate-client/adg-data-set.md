---
title: "AdgDataSet class              | QSYS API Reference Guide"
description: "A DataGate-compatible DataSet class for record-oriented database access. "
last_modified_at: 2024-08-09T17:25:07Z
---

A DataGate-compatible DataSet class for record-oriented database access.

**Namespace:** ASNA.DataGate.Client
**Assembly:** ASNA.QSys.DataGate.Client.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [MarshalByValueComponent](https://learn.microsoft.com/en-us/dotnet/api/system.componentmodel.marshalbyvaluecomponent?view=net-8.0) --> [DataSet](https://docs.microsoft.com/en-us/dotnet/api/system.data.dataset)
<br>
<br>
## Thread Safety

Any public static (Shared) members of this type are safe for multithreaded operations. 

Any instance members are not guaranteed to be thread safe.



## Constructors

| Name | Description |
| --- | --- |
| [AdgDataSet](adg-data-set-ctor.html#adgdatasetstring)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Initializes a new instance of the  class with the specified name.

For detailed constructor documentation, see [AdgDataSet Constructors](adg-data-set-ctor.html).

## Properties

| Type | Name | Description
| --- | --- | --- 
| [DataRow](https://learn.microsoft.com/en-us/dotnet/api/system.data.datarow?view=net-8.0) | ActiveRow | Gets the active row in the DataTable associated with the current format index. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | Count | Gets the number of AdgTable instances in the AdgDataSet. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | CurrentFormatIndex | Gets the current format index used in the dataset. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | CurrentFormatName | Gets the name of the current format used in the dataset. |
| [IEnumerable\<Byte\[\]\>](https://learn.microsoft.com/en-us/dotnet/api/system.collections.generic.ienumerable-1?view=net-8.0) | FormatIdentifiers | Gets the format identifiers used in the dataset. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | Formats | Gets the number of formats used in the dataset. |
| [ICollection\<Int32\>](https://docs.microsoft.com/en-us/dotnet/api/system.collections.icollection) | IntKeys | Gets the collection of format indices in the AdgDataSet. |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | IsReadOnly | Gets a value indicating whether the AdgDataSet is read-only. |
| [AdgTable](/reference/datagate/datagate-client/adg-table.html) | Item | Gets the AdgTable instance associated with the specified format index. |
| [AdgTable](/reference/datagate/datagate-client/adg-table.html) | Item | Gets the AdgTable instance associated with the specified format index. |
| [AdgTable](/reference/datagate/datagate-client/adg-table.html) | Item | Gets the AdgTable instance associated with the specified format name. |
| [AdgTable](/reference/datagate/datagate-client/adg-table.html) | Item | Gets the AdgTable instance associated with the specified format name. |
| [Dictionary\<Int32, AdgTable\>](https://learn.microsoft.com/en-us/dotnet/api/system.collections.generic.dictionary-2?view=net-8.0) | m_adgTables | A dictionary of AdgTable instances used in the dataset. |
| [String\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.string) | m_aFormatStrings | An array of format strings used in the dataset. |
| [DataTable\[\]](https://learn.microsoft.com/en-us/dotnet/api/system.data.datatable.select?view=net-8.0) | m_aKeyTablesTemplates | An array of DataTable templates used for key tables in the dataset. |
| [ICollection\<String\>](https://docs.microsoft.com/en-us/dotnet/api/system.collections.icollection) | StringKeys | Gets the collection of format names in the AdgDataSet. |
| [ICollection\<AdgTable\>](https://docs.microsoft.com/en-us/dotnet/api/system.collections.icollection) | Values | Gets the collection of AdgTable instances in the AdgDataSet. |

## Methods

| Signature | Description |
| --- | --- |
| [AddPreparedRowAndSetActive](adg-data-set-addpreparedrowandsetactive.html)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Adds a prepared row to the DataTable associated with the specified format index and sets it as the active row.
| [AddRow](adg-data-set-addrow.html#void-addrowstring)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Adds a new row to the DataTable associated with the specified format name.
| [AddRow](adg-data-set-addrow.html#void-addrowint32)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Adds a new row to the DataTable associated with the specified format index.
| [Contains](adg-data-set-contains.html)([KeyValuePair\<Int32, AdgTable\>](https://learn.microsoft.com/en-us/dotnet/api/system.collections.generic.keyvaluepair-2?view=net-8.0)) | Determines whether the AdgDataSet contains a specific key-value pair.
| [ContainsKey](adg-data-set-containskey.html)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Determines whether the AdgDataSet contains an AdgTable with the specified format index.
| [CopyTo](adg-data-set-copyto.html)([KeyValuePair`2\[\]](https://learn.microsoft.com/en-us/dotnet/api/system.collections.generic.keyvaluepair-2?view=net-8.0), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Copies the elements of the AdgDataSet to an array, starting at a particular array index.
| [DeleteRow](adg-data-set-deleterow.html)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Deletes the row at the specified relative record number (rrn) in the DataTable associated with the specified format name.
| [GetEnumerator()](adg-data-set-getenumerator.html) | Returns an enumerator that iterates through the AdgDataSet.
| [GetFormatIndex](adg-data-set-getformatindex.html)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Retrieves the format index associated with the specified format name.
| [GetFormatName](adg-data-set-getformatname.html)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Retrieves the format name associated with the specified format index.
| [GetFormatTable](adg-data-set-getformattable.html#datatable-getformattableint32)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Retrieves the DataTable associated with the specified format index.
| [GetFormatTable](adg-data-set-getformattable.html#datatable-getformattablestring)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Retrieves the DataTable associated with the specified format name.
| [Initialize()](adg-data-set-initialize.html) | Initializes the instance of the  class.
| [InitializeCommon()](adg-data-set-initializecommon.html) | Initializes common elements of the  instance.
| [InitializeFormats()](adg-data-set-initializeformats.html) | Initializes the format strings of the  instance.
| [InsertRow](adg-data-set-insertrow.html#void-insertrowstring-int32)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Inserts a new row at the specified relative record number (rrn) in the DataTable associated with the specified format name.
| [InsertRow](adg-data-set-insertrow.html#void-insertrowint32-int32)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Inserts a new row at the specified relative record number (rrn) in the DataTable associated with the specified format index.
| [NewKeyTable](adg-data-set-newkeytable.html#adgkeytable-newkeytableint32)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Creates a new AdgKeyTable for the DataTable associated with the specified format index.
| [NewKeyTable](adg-data-set-newkeytable.html#adgkeytable-newkeytablestring)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Creates a new AdgKeyTable for the DataTable associated with the specified format name.
| [PrepareRow](adg-data-set-preparerow.html#datarow-preparerowstring)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Prepares a new row for the DataTable associated with the specified format name.
| [PrepareRow](adg-data-set-preparerow.html#void-preparerowstring-datarow)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [DataRow](https://learn.microsoft.com/en-us/dotnet/api/system.data.datarow?view=net-8.0)) | Prepares the specified row for the DataTable associated with the specified format name.
| [PrepareRow](adg-data-set-preparerow.html#datarow-preparerowint32)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Prepares a new row for the DataTable associated with the specified format index.
| [SetActive](adg-data-set-setactive.html#bool-setactiveint32-int32)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Sets the active row to the row at the specified relative record number (rrn) in the DataTable associated with the specified format index.
| [SetActive](adg-data-set-setactive.html#bool-setactivestring-int32)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Sets the active row to the row at the specified relative record number (rrn) in the DataTable associated with the specified format name.


<!-- Inline constructor and method details removed; see dedicated pages linked above. -->

## Example 1

```cs 
/* This example will open a file and find the record for
     the customer "Thilmany of Bread Co Resources".
     It omits error trapping for clearity's sake. */

  AdgConnection db = createAdgConnection("MyLocalDB");
  db.Open();
  FileAdapter file = new FileAdapter(db);
  file.FileName = "Examples//CMastNewL2";
  AdgDataSet dataSet;
  file.OpenNewAdgDataSet( out dataSet );

  //This next line creates a key based on record format RCMMastL2
  AdgKeyTable key = dataSet.NewKeyTable("RCMMastL2");

  //We specifiy KeyPartCount to avoid specifiying the second key field.
  //We then set the keyfield "CMName" to our search argument.
  key.KeyPartCount = 1;
  key.Row["CMName"] = "Thilmany Of Bread Co Resources";

  //The following read will find the record associated with the 
  //customer name "Thilmany Of Bread Co Resources" and store it in dataSet.
  file.ReadRandomKey(dataSet, ReadRandomMode.Equal, LockRequest.Default, key);</pre>
```

> See [AdgConnection Example](/reference/datagate/datagate-client/adg-connection.html#create-an-adgconnection) for an implementation of `createAdgConnection()`
