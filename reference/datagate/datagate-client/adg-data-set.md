---
title: AdgDataSet class
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
| [AdgDataSet](#adgdatasetstring)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Initializes a new instance of the  class with the specified name.

### AdgDataSet([String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Initializes a new instance of the  class with the specified name.

```cs
AdgDataSet(String)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | name | 

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
| [ICollection\<String\>](https://docs.microsoft.com/en-us/dotnet/api/system.collections.icollection) | StringKeys | Gets the collection of format names in the AdgDataSet. |
| [ICollection\<AdgTable\>](https://docs.microsoft.com/en-us/dotnet/api/system.collections.icollection) | Values | Gets the collection of AdgTable instances in the AdgDataSet. |

## Methods

| Signature | Description |
| --- | --- |
| [AddPreparedRowAndSetActive](#bool-addpreparedrowandsetactiveint-iformat)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Adds a prepared row to the DataTable associated with the specified format index and sets it as the active row.
| [AddRow](#void-addrowstring-strformat)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Adds a new row to the DataTable associated with the specified format name.
| [AddRow](#void-addrowstring-strformat)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Adds a new row to the DataTable associated with the specified format index.
| [Contains](#bool-containskeyvaluepair-int-adgtable-item)([KeyValuePair](https://learn.microsoft.com/en-us/dotnet/api/system.collections.generic.keyvaluepair-2?view=net-8.0), [AdgTable](/reference/datagate/datagate-client/adg-table.html)) | Determines whether the AdgDataSet contains a specific key-value pair.
| [ContainsKey](#bool-containskeyint-key)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Determines whether the AdgDataSet contains an AdgTable with the specified format index.
| [CopyTo](#void-copytokeyvaluepair-2--array-int-arrayindex)([KeyValuePair](https://learn.microsoft.com/en-us/dotnet/api/system.collections.generic.keyvaluepair-2?view=net-8.0), [AdgTable](/reference/datagate/datagate-client/adg-table.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Copies the elements of the AdgDataSet to an array, starting at a particular array index.
| [DeleteRow](#void-deleterowstring-strformat-int-rrn)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Deletes the row at the specified relative record number (rrn) in the DataTable associated with the specified format name.
| [GetEnumerator()](#ienumerator-keyvaluepair-int-adgtable--getenumerator) | Returns an enumerator that iterates through the AdgDataSet.
| [GetFormatIndex](#int-getformatindexstring-strformat)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Retrieves the format index associated with the specified format name.
| [GetFormatName](#string-getformatnameint-iformat)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Retrieves the format name associated with the specified format index.
| [GetFormatTable](#datatable-getformattableint-iformat)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Retrieves the DataTable associated with the specified format index.
| [GetFormatTable](#datatable-getformattableint-iformat)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Retrieves the DataTable associated with the specified format name.
| [Initialize()](#void-initialize) | Initializes the instance of the  class.
| [InitializeCommon()](#void-initializecommon) | Initializes common elements of the  instance.
| [InitializeFormats()](#void-initializeformats) | Initializes the format strings of the  instance.
| [InsertRow](#void-insertrowstring-strformat-int-rrn)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Inserts a new row at the specified relative record number (rrn) in the DataTable associated with the specified format name.
| [InsertRow](#void-insertrowstring-strformat-int-rrn)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Inserts a new row at the specified relative record number (rrn) in the DataTable associated with the specified format index.
| [NewKeyTable](#adgkeytable-newkeytableint-iformat)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Creates a new AdgKeyTable for the DataTable associated with the specified format index.
| [NewKeyTable](#adgkeytable-newkeytableint-iformat)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [DataRow](https://learn.microsoft.com/en-us/dotnet/api/system.data.datarow?view=net-8.0)) | Creates a new AdgKeyTable for the DataTable associated with the specified format index and sets the key row.
| [NewKeyTable](#adgkeytable-newkeytableint-iformat)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Creates a new AdgKeyTable for the DataTable associated with the specified format name.
| [NewKeyTable](#adgkeytable-newkeytableint-iformat)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [DataRow](https://learn.microsoft.com/en-us/dotnet/api/system.data.datarow?view=net-8.0)) | Creates a new AdgKeyTable for the DataTable associated with the specified format name and sets the key row.
| [PrepareRow](#datarow-preparerowstring-strformat)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Prepares a new row for the DataTable associated with the specified format name.
| [PrepareRow](#datarow-preparerowstring-strformat)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [DataRow](https://learn.microsoft.com/en-us/dotnet/api/system.data.datarow?view=net-8.0)) | Prepares the specified row for the DataTable associated with the specified format name.
| [PrepareRow](#datarow-preparerowstring-strformat)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Prepares a new row for the DataTable associated with the specified format index.
| [SetActive](#bool-setactiveint-iformat-int-rrn)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Sets the active row to the row at the specified relative record number (rrn) in the DataTable associated with the specified format index.
| [SetActive](#bool-setactiveint-iformat-int-rrn)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Sets the active row to the row at the specified relative record number (rrn) in the DataTable associated with the specified format name.
| [TryGetValue](#bool-trygetvaluestring-key-adgtable-value)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [AdgTable](/reference/datagate/datagate-client/adg-table.html)) | Tries to get the AdgTable associated with the specified format name.
| [TryGetValue](#bool-trygetvaluestring-key-adgtable-value)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [AdgTable](/reference/datagate/datagate-client/adg-table.html)) | Tries to get the AdgTable associated with the specified format index.

### bool AddPreparedRowAndSetActive([int iFormat](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Adds a prepared row to the DataTable associated with the specified format index and sets it as the active row.

```cs
bool AddPreparedRowAndSetActive(int iFormat)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | iFormat | 

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | True if the active row was successfully set; otherwise, false.

### void AddRow([string strFormat](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Adds a new row to the DataTable associated with the specified format name.

```cs
void AddRow(string strFormat)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | strFormat | 

### void AddRow([string strFormat](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Adds a new row to the DataTable associated with the specified format index.

```cs
void AddRow(string strFormat)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | iFormat | 

### bool Contains([KeyValuePair\<int, AdgTable\> item](https://learn.microsoft.com/en-us/dotnet/api/system.collections.generic.keyvaluepair-2?view=net-8.0))

Determines whether the AdgDataSet contains a specific key-value pair.

```cs
bool Contains(KeyValuePair<int, AdgTable> item)
```

### bool ContainsKey([int key](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Determines whether the AdgDataSet contains an AdgTable with the specified format index.

```cs
bool ContainsKey(int key)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | key | 

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | true if the AdgDataSet contains an AdgTable with the specified format index; otherwise, false.

### void CopyTo([KeyValuePair`2\[\] array](https://learn.microsoft.com/en-us/dotnet/api/system.collections.generic.keyvaluepair-2?view=net-8.0), [int arrayIndex](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Copies the elements of the AdgDataSet to an array, starting at a particular array index.

```cs
void CopyTo(KeyValuePair`2[] array, int arrayIndex)
```

### void DeleteRow([string strFormat](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [int rrn](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Deletes the row at the specified relative record number (rrn) in the DataTable associated with the specified format name.

```cs
void DeleteRow(string strFormat, int rrn)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | strFormat | 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | rrn | 

### IEnumerator<KeyValuePair<int, AdgTable>> GetEnumerator()

Returns an enumerator that iterates through the AdgDataSet.

```cs
IEnumerator<KeyValuePair<int, AdgTable>> GetEnumerator()
```

### int GetFormatIndex([string strFormat](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Retrieves the format index associated with the specified format name.

```cs
int GetFormatIndex(string strFormat)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | strFormat | 

#### Returns

| Type | Description
| --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | The format index associated with the specified format name.

### string GetFormatName([int iFormat](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Retrieves the format name associated with the specified format index.

```cs
string GetFormatName(int iFormat)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | iFormat | 

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The format name associated with the specified format index.

### DataTable GetFormatTable([int iFormat](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Retrieves the DataTable associated with the specified format index.

```cs
DataTable GetFormatTable(int iFormat)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | iFormat | 

#### Returns

| Type | Description
| --- | ---
| [DataTable](https://learn.microsoft.com/en-us/dotnet/api/system.data.datatable.select?view=net-8.0) | The DataTable associated with the specified format index.

### DataTable GetFormatTable([int iFormat](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Retrieves the DataTable associated with the specified format name.

```cs
DataTable GetFormatTable(int iFormat)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | strFormat | 

#### Returns

| Type | Description
| --- | ---
| [DataTable](https://learn.microsoft.com/en-us/dotnet/api/system.data.datatable.select?view=net-8.0) | The DataTable associated with the specified format name.

### void Initialize()

Initializes the instance of the  class.

```cs
void Initialize()
```

### void InitializeCommon()

Initializes common elements of the  instance.

```cs
void InitializeCommon()
```

### void InitializeFormats()

Initializes the format strings of the  instance.

```cs
void InitializeFormats()
```

### void InsertRow([string strFormat](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [int rrn](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Inserts a new row at the specified relative record number (rrn) in the DataTable associated with the specified format name.

```cs
void InsertRow(string strFormat, int rrn)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | strFormat | 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | rrn | 

### void InsertRow([string strFormat](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [int rrn](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Inserts a new row at the specified relative record number (rrn) in the DataTable associated with the specified format index.

```cs
void InsertRow(string strFormat, int rrn)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | iFormat | 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | rrn | 

### AdgKeyTable NewKeyTable([int iFormat](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Creates a new AdgKeyTable for the DataTable associated with the specified format index.

```cs
AdgKeyTable NewKeyTable(int iFormat)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | iFormat | 

#### Returns

| Type | Description
| --- | ---
| [AdgKeyTable](/reference/datagate/datagate-client/adg-key-table.html) | A new AdgKeyTable for the DataTable associated with the specified format index.

### AdgKeyTable NewKeyTable([int iFormat](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Creates a new AdgKeyTable for the DataTable associated with the specified format index and sets the key row.

```cs
AdgKeyTable NewKeyTable(int iFormat)
```

### AdgKeyTable NewKeyTable([int iFormat](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Creates a new AdgKeyTable for the DataTable associated with the specified format name.

```cs
AdgKeyTable NewKeyTable(int iFormat)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | strFormat | 

#### Returns

| Type | Description
| --- | ---
| [AdgKeyTable](/reference/datagate/datagate-client/adg-key-table.html) | A new AdgKeyTable for the DataTable associated with the specified format name.

### AdgKeyTable NewKeyTable([int iFormat](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Creates a new AdgKeyTable for the DataTable associated with the specified format name and sets the key row.

```cs
AdgKeyTable NewKeyTable(int iFormat)
```

### DataRow PrepareRow([string strFormat](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Prepares a new row for the DataTable associated with the specified format name.

```cs
DataRow PrepareRow(string strFormat)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | strFormat | 

#### Returns

| Type | Description
| --- | ---
| [DataRow](https://learn.microsoft.com/en-us/dotnet/api/system.data.datarow?view=net-8.0) | A new row prepared for the DataTable associated with the specified format name.

### DataRow PrepareRow([string strFormat](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Prepares the specified row for the DataTable associated with the specified format name.

```cs
DataRow PrepareRow(string strFormat)
```

### DataRow PrepareRow([string strFormat](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Prepares a new row for the DataTable associated with the specified format index.

```cs
DataRow PrepareRow(string strFormat)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | iFormat | 

#### Returns

| Type | Description
| --- | ---
| [DataRow](https://learn.microsoft.com/en-us/dotnet/api/system.data.datarow?view=net-8.0) | A new row prepared for the DataTable associated with the specified format index.

### bool SetActive([int iFormat](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int rrn](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Sets the active row to the row at the specified relative record number (rrn) in the DataTable associated with the specified format index.

```cs
bool SetActive(int iFormat, int rrn)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | iFormat | 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | rrn | 

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | True if the active row was successfully set; otherwise, false.

### bool SetActive([int iFormat](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int rrn](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Sets the active row to the row at the specified relative record number (rrn) in the DataTable associated with the specified format name.

```cs
bool SetActive(int iFormat, int rrn)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | strFormat | 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | rrn | 

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | True if the active row was successfully set; otherwise, false.

### bool TryGetValue([string key](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [AdgTable& value](/reference/datagate/datagate-client/adg-table.html))

Tries to get the AdgTable associated with the specified format name.

```cs
bool TryGetValue(string key, AdgTable& value)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | key | 
| [AdgTable&](/reference/datagate/datagate-client/adg-table.html) | value | 

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | true if the AdgDataSet contains an element with the specified format name; otherwise, false.

### bool TryGetValue([string key](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [AdgTable& value](/reference/datagate/datagate-client/adg-table.html))

Tries to get the AdgTable associated with the specified format index.

```cs
bool TryGetValue(string key, AdgTable& value)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | key | 
| [AdgTable&](/reference/datagate/datagate-client/adg-table.html) | value | 

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | true if the AdgDataSet contains an element with the specified format index; otherwise, false.

## Example 1. NewKeyTable method example.

```cs 
/* This example will open a file and find the record for
     the customer "Thilmany of Bread Co Resources".
     It omits error trapping for clearity's sake. */

  AdgConnection db = new AdgConnection("*Public/DG NET Local");
  db.Open();
  FileAdapter file = new FileAdapter(db);
  file.FileName = "Examples//CMastNewL2";
  AdgDataSet dataSet;
  file.OpenNewAdgDataSet( out dataSet );

  //This next line creates a key based on record format RCMMastL2
  AdgKeyTable key = dataSet.NewKeyTable("RCMMastL2");

  //We specifiy KeyPartCount to avoid specifiying the second
  //key field.
  //We then set the keyfield "CMName" to our search argument.
  key.KeyPartCount = 1;
  key.Row["CMName"] = "Thilmany Of Bread Co Resources";

  //The following read will find the record associated with the 
  //customer name "Thilmany Of Bread Co Resources" and store it
  //in dataSet.
  file.ReadRandomKey(dataSet, ReadRandomMode.Equal, LockRequest.Default, key);</pre>
```
