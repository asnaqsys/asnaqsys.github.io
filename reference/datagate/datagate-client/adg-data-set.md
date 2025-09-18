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
| [AdgDataSet](#adgdatasetstring)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Initializes a new instance of the  class with the specified name.

### AdgDataSet([String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Initializes a new instance of the  class with the specified name.

```cs
AdgDataSet(String)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | name | The name to give the new .

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
| [AddPreparedRowAndSetActive](#bool-addpreparedrowandsetactiveint-iformat)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Adds a prepared row to the DataTable associated with the specified format index and sets it as the active row.
| [AddRow](#void-addrowstring-strformat)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Adds a new row to the DataTable associated with the specified format name.
| [AddRow](#void-addrowint-iformat)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Adds a new row to the DataTable associated with the specified format index.
| [Contains](#bool-containskeyvaluepair-int-adgtable-item)([KeyValuePair\<Int32, AdgTable\>](https://learn.microsoft.com/en-us/dotnet/api/system.collections.generic.keyvaluepair-2?view=net-8.0)) | Determines whether the AdgDataSet contains a specific key-value pair.
| [ContainsKey](#bool-containskeyint-key)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Determines whether the AdgDataSet contains an AdgTable with the specified format index.
| [CopyTo](#void-copytokeyvaluepair-2--array-int-arrayindex)([KeyValuePair`2\[\]](https://learn.microsoft.com/en-us/dotnet/api/system.collections.generic.keyvaluepair-2?view=net-8.0), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Copies the elements of the AdgDataSet to an array, starting at a particular array index.
| [DeleteRow](#void-deleterowstring-strformat-int-rrn)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Deletes the row at the specified relative record number (rrn) in the DataTable associated with the specified format name.
| [GetEnumerator()](#ienumerator-keyvaluepair-int-adgtable--getenumerator) | Returns an enumerator that iterates through the AdgDataSet.
| [GetFormatIndex](#int-getformatindexstring-strformat)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Retrieves the format index associated with the specified format name.
| [GetFormatName](#string-getformatnameint-iformat)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Retrieves the format name associated with the specified format index.
| [GetFormatTable](#datatable-getformattableint-iformat)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Retrieves the DataTable associated with the specified format index.
| [GetFormatTable](#datatable-getformattablestring-strformat)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Retrieves the DataTable associated with the specified format name.
| [Initialize()](#void-initialize) | Initializes the instance of the  class.
| [InitializeCommon()](#void-initializecommon) | Initializes common elements of the  instance.
| [InitializeFormats()](#void-initializeformats) | Initializes the format strings of the  instance.
| [InsertRow](#void-insertrowstring-strformat-int-rrn)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Inserts a new row at the specified relative record number (rrn) in the DataTable associated with the specified format name.
| [InsertRow](#void-insertrowint-iformat-int-rrn)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Inserts a new row at the specified relative record number (rrn) in the DataTable associated with the specified format index.
| [NewKeyTable](#adgkeytable-newkeytableint-iformat)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Creates a new AdgKeyTable for the DataTable associated with the specified format index.
| [NewKeyTable](#adgkeytable-newkeytablestring-strformat)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Creates a new AdgKeyTable for the DataTable associated with the specified format name.
| [PrepareRow](#datarow-preparerowstring-strformat)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Prepares a new row for the DataTable associated with the specified format name.
| [PrepareRow](#void-preparerowstring-strformat-datarow-row)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [DataRow](https://learn.microsoft.com/en-us/dotnet/api/system.data.datarow?view=net-8.0)) | Prepares the specified row for the DataTable associated with the specified format name.
| [PrepareRow](#datarow-preparerowint-iformat)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Prepares a new row for the DataTable associated with the specified format index.
| [SetActive](#bool-setactiveint-iformat-int-rrn)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Sets the active row to the row at the specified relative record number (rrn) in the DataTable associated with the specified format index.
| [SetActive](#bool-setactivestring-strformat-int-rrn)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Sets the active row to the row at the specified relative record number (rrn) in the DataTable associated with the specified format name.

### bool AddPreparedRowAndSetActive([int iFormat](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Adds a prepared row to the DataTable associated with the specified format index and sets it as the active row.


#### Remarks
This method is used to add a prepared row to a specific DataTable in the AdgDataSet and set it as the active row.The method retrieves the AdgTable instance from the AdgTable dictionary using the provided format index and calls its AddRow method to add a new row.Then, it sets the NewFormatIndex to the provided format index and calls the SetActive method with the index of the last row in the DataTable to set the new row as the active row.The SetActive method returns true if the active row was successfully set; otherwise, it returns false.This method is used in scenarios where a prepared row needs to be added to a DataTable and set as the active row based on its format index.

```cs
bool AddPreparedRowAndSetActive(int iFormat)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | iFormat | The format index of the DataTable.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | True if the active row was successfully set; otherwise, false.

### void AddRow([string strFormat](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Adds a new row to the DataTable associated with the specified format name.


#### Remarks
This method is used to add a new row to a specific DataTable in the AdgDataSet.The method first calls the GetFormatIndex method with the provided format name to retrieve the corresponding format index.Then, it calls the AddRow method with the retrieved format index to add a new row.The AddRow method retrieves the AdgTable instance from the AdgTable dictionary using the format index and calls its AddRow method to add a new row.This method is used in scenarios where a new row needs to be added to a DataTable based on its format name.

```cs
void AddRow(string strFormat)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | strFormat | The format name of the DataTable.

### void AddRow([int iFormat](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Adds a new row to the DataTable associated with the specified format index.


#### Remarks
This method is used to add a new row to a specific DataTable in the AdgDataSet.The method retrieves the AdgTable instance from the AdgTable dictionary using the provided format index and calls its AddRow method to add a new row.The AddRow method of the AdgTable instance creates a new row, sets the default values for the new row, and adds it to the DataTable.This method is used in scenarios where a new row needs to be added to a DataTable based on its format index.

```cs
void AddRow(int iFormat)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | iFormat | The format index of the DataTable.

### bool Contains([KeyValuePair\<int, AdgTable\> item](https://learn.microsoft.com/en-us/dotnet/api/system.collections.generic.keyvaluepair-2?view=net-8.0))

Determines whether the AdgDataSet contains a specific key-value pair.


#### Remarks
This method is used to determine whether the AdgDataSet contains a specific key-value pair.The method calls the Contains method of the AdgTable dictionary with the provided key-value pair and returns the result.This method is used in scenarios where it needs to be checked whether a specific key-value pair exists in the AdgDataSet.

```cs
bool Contains(KeyValuePair<int, AdgTable> item)
```

### bool ContainsKey([int key](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Determines whether the AdgDataSet contains an AdgTable with the specified format index.


#### Remarks
This method is used to determine whether the AdgDataSet contains an AdgTable with a specific format index.The method calls the ContainsKey method of the AdgTable dictionary with the provided format index and returns the result.This method is used in scenarios where it needs to be checked whether an AdgTable with a specific format index exists in the AdgDataSet.

```cs
bool ContainsKey(int key)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | key | The format index to locate in the AdgDataSet.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | true if the AdgDataSet contains an AdgTable with the specified format index; otherwise, false.

### void CopyTo([KeyValuePair`2\[\] array](https://learn.microsoft.com/en-us/dotnet/api/system.collections.generic.keyvaluepair-2?view=net-8.0), [int arrayIndex](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Copies the elements of the AdgDataSet to an array, starting at a particular array index.


#### Remarks
This method is used to copy the elements of the AdgDataSet to an array, starting at a particular array index.The method calls the CopyTo method of the AdgTable dictionary with the provided array and array index.This method is used in scenarios where the elements of the AdgDataSet need to be copied to an array for further processing or storage.

```cs
void CopyTo(KeyValuePair`2[] array, int arrayIndex)
```

### void DeleteRow([string strFormat](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [int rrn](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Deletes the row at the specified relative record number (rrn) in the DataTable associated with the specified format name.


#### Remarks
This method is used to delete a specific row in a DataTable in the AdgDataSet.The method first calls the SetActive method with the provided format name and rrn to set the active row to the specified row.If the SetActive method returns false, indicating that the specified row could not be found, an ArgumentException is thrown.Otherwise, the method retrieves the AdgTable instance from the AdgTable dictionary using the CurrentFormatIndex and calls its Delete method with the active row.This method is used in scenarios where a specific row in a DataTable needs to be deleted based on its format name and rrn.

```cs
void DeleteRow(string strFormat, int rrn)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | strFormat | The format name of the DataTable.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | rrn | The relative record number of the row to delete.

### IEnumerator<KeyValuePair<int, AdgTable>> GetEnumerator()

Returns an enumerator that iterates through the AdgDataSet.


#### Remarks
This method is used to get an enumerator that iterates through the AdgDataSet.The method returns the enumerator of the AdgTable dictionary which contains all the AdgTable instances in the AdgDataSet.This method is used in scenarios where it needs to be iterated over all the AdgTable instances in the AdgDataSet, such as when using a foreach loop.

```cs
IEnumerator<KeyValuePair<int, AdgTable>> GetEnumerator()
```

### int GetFormatIndex([string strFormat](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Retrieves the format index associated with the specified format name.


#### Remarks
This method is used to retrieve the format index associated with a specific format name in the AdgDataSet.The format index corresponds to a specific format for the data in a DataTable.The method iterates over the format strings array and returns the index of the first occurrence of the provided format name.If the format name is not found in the format strings array, a dgException is thrown.This method is used in various methods like GetFormatTable, SetActive, and AddRow where a specific format index is required based on its format name.

```cs
int GetFormatIndex(string strFormat)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | strFormat | The format name to retrieve the index for.

#### Returns

| Type | Description
| --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | The format index associated with the specified format name.

### string GetFormatName([int iFormat](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Retrieves the format name associated with the specified format index.


#### Remarks
This method is used to retrieve the format name for a specific format index in the AdgDataSet.The method first checks if the format strings array is null or if the provided format index is out of range.If the format strings array is null or the format index is out of range, the method throws a dgException with the dgEaNOCURR error number and an ArgumentOutOfRangeException.Otherwise, the method returns the format name from the format strings array at the provided format index.This method is used in scenarios where the format name needs to be retrieved based on its format index.

```cs
string GetFormatName(int iFormat)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | iFormat | The format index.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The format name associated with the specified format index.

### DataTable GetFormatTable([int iFormat](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Retrieves the DataTable associated with the specified format index.


#### Remarks
This method is used to retrieve the DataTable associated with a specific format index in the AdgDataSet.The format index corresponds to a specific format for the data in a DataTable.If the format index is less than 0 or greater than or equal to the total number of formats, a dgException is thrown.Otherwise, the method retrieves the AdgTable instance from the AdgTable dictionary using the format index and returns its DataTable.This method is used in various methods like SetActive, PrepareRow, and AddRow where a specific DataTable is required based on its format index.

```cs
DataTable GetFormatTable(int iFormat)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | iFormat | The format index of the DataTable to retrieve.

#### Returns

| Type | Description
| --- | ---
| [DataTable](https://learn.microsoft.com/en-us/dotnet/api/system.data.datatable.select?view=net-8.0) | The DataTable associated with the specified format index.

### DataTable GetFormatTable([string strFormat](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Retrieves the DataTable associated with the specified format name.


#### Remarks
This method is used to retrieve the DataTable associated with a specific format name in the AdgDataSet.The format name corresponds to a specific format for the data in a DataTable.The method first calls the GetFormatIndex method with the provided format name to retrieve the corresponding format index.Then, it calls the GetFormatTable method with the retrieved format index to get the DataTable.This method is used in various methods where a specific DataTable is required based on its format name.

```cs
DataTable GetFormatTable(string strFormat)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | strFormat | The format name of the DataTable to retrieve.

#### Returns

| Type | Description
| --- | ---
| [DataTable](https://learn.microsoft.com/en-us/dotnet/api/system.data.datatable.select?view=net-8.0) | The DataTable associated with the specified format name.

### void Initialize()

Initializes the instance of the  class.


#### Remarks
This method is intended to be overridden in derived classes to provide custom initialization logic.It is called in the constructors and deserialization methods of the  class.The specific implementation of this method in a derived class should initialize any additional properties or fields that are not initialized in the base class.

```cs
void Initialize()
```

### void InitializeCommon()

Initializes common elements of the  instance.


#### Remarks
This method is used to initialize common elements of the  instance, such as the format strings and AdgTable instances.If the Tables collection is empty, it sets the format strings array and the key tables templates array to null and returns.Otherwise, it parses the count of formats from the ExtendedProperties and initializes the format strings array with this count.It then iterates over each DataTable in the Tables collection, retrieves the format name from the ExtendedProperties, and stores it in the format strings array.If the AdgTable dictionary does not contain an entry for the format index, it creates a new AdgTable instance for the DataTable and adds it to the dictionary.Finally, it sets the Formats property to the length of the format strings array, initializes the key tables templates array with the count of formats, and resets the CurrentFormatIndex.This method is called in the constructors and deserialization methods of the  class.

```cs
void InitializeCommon()
```

### void InitializeFormats()

Initializes the format strings of the  instance.


#### Remarks
This method is intended to be overridden in derived classes to provide custom initialization logic for the format strings.The format strings represent the specific formats for the data in each DataTable in the AdgDataSet.The specific implementation of this method in a derived class should parse the format strings from the DataTables and store them in the format strings array.It is called in the constructors and deserialization methods of the  class.

```cs
void InitializeFormats()
```

### void InsertRow([string strFormat](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [int rrn](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Inserts a new row at the specified relative record number (rrn) in the DataTable associated with the specified format name.


#### Remarks
This method is used to insert a new row at a specific position in a DataTable in the AdgDataSet.The method first calls the GetFormatIndex method with the provided format name to retrieve the corresponding format index.Then, it calls the InsertRow method with the retrieved format index and the provided rrn to insert a new row.The InsertRow method retrieves the AdgTable instance from the AdgTable dictionary using the format index and calls its InsertRow method with the provided rrn.This method is used in scenarios where a new row needs to be inserted at a specific position in a DataTable based on its format name and rrn.

```cs
void InsertRow(string strFormat, int rrn)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | strFormat | The format name of the DataTable.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | rrn | The relative record number at which to insert the new row.

### void InsertRow([int iFormat](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int rrn](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Inserts a new row at the specified relative record number (rrn) in the DataTable associated with the specified format index.


#### Remarks
This method is used to insert a new row at a specific position in a DataTable in the AdgDataSet.The method retrieves the AdgTable instance from the AdgTable dictionary using the provided format index and calls its InsertRow method with the provided rrn.The InsertRow method of the AdgTable instance creates a new row, sets the default values for the new row, and inserts it at the specified rrn in the DataTable.This method is used in scenarios where a new row needs to be inserted at a specific position in a DataTable based on its format index and rrn.

```cs
void InsertRow(int iFormat, int rrn)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | iFormat | The format index of the DataTable.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | rrn | The relative record number at which to insert the new row.

### AdgKeyTable NewKeyTable([int iFormat](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Creates a new AdgKeyTable for the DataTable associated with the specified format index.


#### Remarks
This method is used to create a new AdgKeyTable for a specific DataTable in the AdgDataSet.The method calls the NewKeyTable method with the provided format index and a discard out variable to create a new AdgKeyTable.The NewKeyTable method retrieves the AdgTable instance from the AdgTable dictionary using the format index, creates a new AdgKeyTable, and sets the key row in the AdgKeyTable to a new row in the DataTable.This method is used in scenarios where a new AdgKeyTable needs to be created for a DataTable based on its format index.

```cs
AdgKeyTable NewKeyTable(int iFormat)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | iFormat | The format index of the DataTable.

#### Returns

| Type | Description
| --- | ---
| [AdgKeyTable](/reference/datagate/datagate-client/adg-key-table.html) | A new AdgKeyTable for the DataTable associated with the specified format index.

### AdgKeyTable NewKeyTable([string strFormat](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Creates a new AdgKeyTable for the DataTable associated with the specified format name.


#### Remarks
This method is used to create a new AdgKeyTable for a specific DataTable in the AdgDataSet.The method calls the NewKeyTable method with the provided format name and a discard out variable to create a new AdgKeyTable.The NewKeyTable method calls the GetFormatIndex method with the provided format name to retrieve the corresponding format index, and creates a new AdgKeyTable for the DataTable associated with the format index.This method is used in scenarios where a new AdgKeyTable needs to be created for a DataTable based on its format name.

```cs
AdgKeyTable NewKeyTable(string strFormat)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | strFormat | The format name of the DataTable.

#### Returns

| Type | Description
| --- | ---
| [AdgKeyTable](/reference/datagate/datagate-client/adg-key-table.html) | A new AdgKeyTable for the DataTable associated with the specified format name.

### DataRow PrepareRow([string strFormat](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Prepares a new row for the DataTable associated with the specified format name.


#### Remarks
This method is used to prepare a new row for a specific DataTable in the AdgDataSet.The method first calls the GetFormatIndex method with the provided format name to retrieve the corresponding format index.Then, it calls the PrepareRow method with the retrieved format index to prepare a new row.The PrepareRow method retrieves the AdgTable instance from the AdgTable dictionary using the format index, calls its PrepareRow method to create a new row, and sets the active row to the new row.This method is used in various methods like AddRow, InsertRow, and SetActive where a new row needs to be prepared for a DataTable based on its format name.

```cs
DataRow PrepareRow(string strFormat)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | strFormat | The format name of the DataTable.

#### Returns

| Type | Description
| --- | ---
| [DataRow](https://learn.microsoft.com/en-us/dotnet/api/system.data.datarow?view=net-8.0) | A new row prepared for the DataTable associated with the specified format name.

### void PrepareRow([string strFormat](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [DataRow row](https://learn.microsoft.com/en-us/dotnet/api/system.data.datarow?view=net-8.0))

Prepares the specified row for the DataTable associated with the specified format name.


#### Remarks
This method is used to prepare a specific row for a DataTable in the AdgDataSet.The method first calls the GetFormatIndex method with the provided format name to retrieve the corresponding format index.Then, it retrieves the AdgTable instance from the AdgTable dictionary using the retrieved format index and calls its PrepareRow method with the provided row.The PrepareRow method of the AdgTable instance sets the default values for the row and sets the active row to the provided row.This method is used in scenarios where a specific row in a DataTable needs to be prepared based on its format name.

```cs
void PrepareRow(string strFormat, DataRow row)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | strFormat | The format name of the DataTable.
| [DataRow](https://learn.microsoft.com/en-us/dotnet/api/system.data.datarow?view=net-8.0) | row | The row to prepare.

### DataRow PrepareRow([int iFormat](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Prepares a new row for the DataTable associated with the specified format index.


#### Remarks
This method is used to prepare a new row for a specific DataTable in the AdgDataSet.The method retrieves the AdgTable instance from the AdgTable dictionary using the provided format index and calls its PrepareRow method to create a new row.The PrepareRow method of the AdgTable instance sets the default values for the new row and sets the active row to the new row.This method is used in various methods like AddRow, InsertRow, and SetActive where a new row needs to be prepared for a DataTable based on its format index.

```cs
DataRow PrepareRow(int iFormat)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | iFormat | The format index of the DataTable.

#### Returns

| Type | Description
| --- | ---
| [DataRow](https://learn.microsoft.com/en-us/dotnet/api/system.data.datarow?view=net-8.0) | A new row prepared for the DataTable associated with the specified format index.

### bool SetActive([int iFormat](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int rrn](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Sets the active row to the row at the specified relative record number (rrn) in the DataTable associated with the specified format index.


#### Remarks
This method is used to set the active row in a DataTable in the AdgDataSet.If the provided format index is less than 0, the method calls the SetActive method with the provided rrn to set the active row in the DataTable associated with the CurrentFormatIndex.Otherwise, the method retrieves the AdgTable instance from the AdgTable dictionary using the provided format index and calls the SetActiveInternal method with the AdgTable instance, the format index, and the rrn.The SetActiveInternal method sets the active row in the DataTable associated with the provided format index to the row at the provided rrn.This method is used in various methods like AddRow, InsertRow, and DeleteRow where the active row needs to be set based on a format index and rrn.

```cs
bool SetActive(int iFormat, int rrn)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | iFormat | The format index of the DataTable.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | rrn | The relative record number of the row to set as active.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | True if the active row was successfully set; otherwise, false.

### bool SetActive([string strFormat](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [int rrn](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Sets the active row to the row at the specified relative record number (rrn) in the DataTable associated with the specified format name.


#### Remarks
This method is used to set the active row in a DataTable in the AdgDataSet.If the provided format name is null or empty, the method calls the SetActive method with the provided rrn to set the active row in the DataTable associated with the CurrentFormatIndex.Otherwise, the method calls the GetFormatIndex method with the provided format name to retrieve the corresponding format index and calls the SetActive method with the format index and the rrn.The SetActive method sets the active row in the DataTable associated with the provided format index to the row at the provided rrn.This method is used in various methods like AddRow, InsertRow, and DeleteRow where the active row needs to be set based on a format name and rrn.

```cs
bool SetActive(string strFormat, int rrn)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | strFormat | The format name of the DataTable.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | rrn | The relative record number of the row to set as active.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | True if the active row was successfully set; otherwise, false.

## Example 1. NewKeyTable method example.

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

> See [AdgConnection Example](/reference/datagate/datagate-client/adg-connection.html#create-an-adgconnection) for an implementation of `createAdgConnection()`
