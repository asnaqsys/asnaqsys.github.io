---
title: "FileAdapter class             | QSYS API Reference Guide"
description: "The  class manages file operations like opening, closing, reading, writing, and querying, handling various access modes and settings. "
last_modified_at: 2024-08-09T17:25:07Z
---

The  class manages file operations like opening, closing, reading, writing, and querying, handling various access modes and settings.

**Namespace:** ASNA.DataGate.Client
**Assembly:** ASNA.QSys.DataGate.Client.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>
## Thread Safety

Any public static (Shared) members of this type are safe for multithreaded operations. Any instance members are not guaranteed to be thread safe.


## Constructors

| Name | Description |
| --- | --- |
| [FileAdapter()](#fileadapter) | Initializes a new instance of the FileAdapter class without a connection.
| [FileAdapter](#fileadapteradgconnection)([AdgConnection](/reference/datagate/datagate-client/adg-connection.html)) | Initializes a new instance of the FileAdapter class with a connection.
| [FileAdapter](#fileadapteradgconnection-string)([AdgConnection](/reference/datagate/datagate-client/adg-connection.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Initializes a new instance of the FileAdapter class with a connection and a file name.
| [FileAdapter](#fileadapteradgconnection-string-string)([AdgConnection](/reference/datagate/datagate-client/adg-connection.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Initializes a new instance of the FileAdapter class with a connection, a file name, and a member name.
| [FileAdapter](#fileadapterifileobject-string)([IFileObject](/reference/datagate/datagate-client/i-file-object.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Initializes a new instance of the FileAdapter class with a FileObject and a member name.
| [FileAdapter](#fileadapterifileobject)([IFileObject](/reference/datagate/datagate-client/i-file-object.html)) | Initializes a new instance of the FileAdapter class with a FileObject.

### FileAdapter()

Initializes a new instance of the FileAdapter class without a connection.

```cs
FileAdapter()
```

### FileAdapter([AdgConnection](/reference/datagate/datagate-client/adg-connection.html))

Initializes a new instance of the FileAdapter class with a connection.

```cs
FileAdapter(AdgConnection)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [AdgConnection](/reference/datagate/datagate-client/adg-connection.html) | cn | The connection to use for the FileAdapter.

### FileAdapter([AdgConnection](/reference/datagate/datagate-client/adg-connection.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Initializes a new instance of the FileAdapter class with a connection and a file name.

```cs
FileAdapter(AdgConnection, String)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [AdgConnection](/reference/datagate/datagate-client/adg-connection.html) | cn | The connection to use for the FileAdapter.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | FileName | The name of the file to work with.

### FileAdapter([AdgConnection](/reference/datagate/datagate-client/adg-connection.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Initializes a new instance of the FileAdapter class with a connection, a file name, and a member name.

```cs
FileAdapter(AdgConnection, String, String)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [AdgConnection](/reference/datagate/datagate-client/adg-connection.html) | cn | The connection to use for the FileAdapter.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | FileNamePm | The name of the file to work with.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | MemberNamePm | The name of the member to work with.

### FileAdapter([IFileObject](/reference/datagate/datagate-client/i-file-object.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Initializes a new instance of the FileAdapter class with a FileObject and a member name.

```cs
FileAdapter(IFileObject, String)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [IFileObject](/reference/datagate/datagate-client/i-file-object.html) | fileObject | The FileObject to use for the FileAdapter.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | memberName | The name of the member to work with.

### FileAdapter([IFileObject](/reference/datagate/datagate-client/i-file-object.html))

Initializes a new instance of the FileAdapter class with a FileObject.

```cs
FileAdapter(IFileObject)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [IFileObject](/reference/datagate/datagate-client/i-file-object.html) | fileObject | The FileObject to use for the FileAdapter.

## Properties

| Type | Name | Description
| --- | --- | --- 
| [AccessMode](/reference/datagate/datagate-common/access-mode.html) | AccessMode | Gets or sets the access mode of the FileAdapter. |
| [AdgConnection](/reference/datagate/datagate-client/adg-connection.html) | Connection | Gets or sets the connection of the FileAdapter. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | CurrentFormatIndex | Gets the index of the current format in the file that the FileAdapter is working with. |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | ExactSeek | Gets a value indicating whether the file that the FileAdapter is working with is in exact seek mode. |
| [Hashtable](https://learn.microsoft.com/en-us/dotnet/api/system.collections.hashtable?view=net-8.0) | ExtendedResults | Gets a Hashtable containing the extended results for the file that the FileAdapter is working with. |
| [Int64](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | FileLength | Gets the length of the file that the FileAdapter is working with. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | FileName | Gets or sets the name of the file that the FileAdapter is working with. |
| [IFileObject](/reference/datagate/datagate-client/i-file-object.html) | FileObject | Gets the FileObject that the FileAdapter is working with. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | FormatRequested | Gets the index of the format that was requested for the file that the FileAdapter is working with. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | FormatToUse | Gets the index of the format that is currently being used in the file that the FileAdapter is working with. |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | IsBulkWriter | Gets a value indicating whether the file that the FileAdapter is working with supports bulk writing. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | LibraryName | Gets the name of the library that the file that the FileAdapter is working with is located in. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | MemberName | Gets or sets the name of the member that the FileAdapter is working with. |
| [FileOpenAttr](/reference/datagate/datagate-providers/file-open-attr.html) | OpenAttributes | Gets or sets the open attributes of the FileAdapter. |
| [Int64](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | RecordCount | Gets the record count of the file that the FileAdapter is working with. |
| [Int64](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | RRN | Gets the relative record number (RRN) of the current record in the file that the FileAdapter is working with. |
| [AdapterStatus](/reference/datagate/datagate-client/adapter-status.html) | Status | Gets the current status of the FileAdapter. |

## Methods

| Signature | Description |
| --- | --- |
| [AddRecord](#void-addrecordadgdataset-ds)([AdgDataSet](/reference/datagate/datagate-client/adg-data-set.html)) | Adds a record to the file using the provided AdgDataSet.
| [AddRecord](#void-addrecordxmlreader-xr-adgdataset-ds)([XmlReader](https://learn.microsoft.com/en-us/dotnet/api/system.xml.xmlreader?view=net-8.0), [AdgDataSet](/reference/datagate/datagate-client/adg-data-set.html)) | Adds a record to the file using the provided XmlReader and AdgDataSet.
| [AddRecord](#void-addrecordadgdataset-ds-char--appindicators)([AdgDataSet](/reference/datagate/datagate-client/adg-data-set.html), [Char\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.char)) | Adds a record to the file using the provided AdgDataSet and application indicators.
| [ChangeCurrent](#void-changecurrentadgdataset-ds)([AdgDataSet](/reference/datagate/datagate-client/adg-data-set.html)) | Changes the current record in the file using the provided AdgDataSet.
| [ChangeRRN](#void-changerrnadgdataset-ds-long-rrn)([AdgDataSet](/reference/datagate/datagate-client/adg-data-set.html), [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64)) | Changes the current record in the file to the record at the specified relative record number (RRN).
| [CheckKey](#void-checkkeyadgkeytable-keytable)([AdgKeyTable](/reference/datagate/datagate-client/adg-key-table.html)) | Checks the validity of the provided key table.
| [Close()](#void-close) | Closes the FileAdapter and releases all resources used by it.
| [CreateDataSet()](#adgdataset-createdataset) | Creates a new AdgDataSet for the FileAdapter.
| [DeleteAllRecords()](#void-deleteallrecords) | Deletes all records from the file that the FileAdapter is working with.
| [DeleteCurrent()](#void-deletecurrent) | Deletes the current record from the file that the FileAdapter is working with.
| [DeleteKey](#void-deletekeyadgkeytable-keytable)([AdgKeyTable](/reference/datagate/datagate-client/adg-key-table.html)) | Deletes the record with the specified key from the file that the FileAdapter is working with.
| [DeleteRange](#void-deleterangeadgkeytable-firstkey-rangefirst-rangefirst-adgkeytable-lastkey-rangelast-rangelast)([AdgKeyTable](/reference/datagate/datagate-client/adg-key-table.html), [RangeFirst](/reference/datagate/datagate-common/range-first.html), [AdgKeyTable](/reference/datagate/datagate-client/adg-key-table.html), [RangeLast](/reference/datagate/datagate-common/range-last.html)) | Deletes a range of records from the file that the FileAdapter is working with.
| [DeleteRRN](#void-deleterrnlong-rrn)([Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64)) | Deletes the record at the specified relative record number (RRN) from the file that the FileAdapter is working with.
| [Dispose()](#void-dispose) | Releases all resources used by the FileAdapter.
| [Dispose](#void-disposebool-isdisposing)([Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Releases the unmanaged resources used by the FileAdapter and optionally releases the managed resources.
| [Finalize()](#void-finalize) | Finalizes an instance of the FileAdapter class.
| [ForceEOD()](#void-forceeod) | Forces the end of data (EOD) for the file that the FileAdapter is working with.
| [GetFormatName](#string-getformatnameint-i)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Gets the name of the format at the specified index in the file that the FileAdapter is working with.
| [GetPrintProperties](#iprintproperties-getprintpropertiesstring-format)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Gets the print properties for the specified format in the file that the FileAdapter is working with.
| [Open](#void-openadgdataset-ds)([AdgDataSet](/reference/datagate/datagate-client/adg-data-set.html)) | Opens the FileAdapter with the specified AdgDataSet.
| [OpenNewAdgDataSet](#void-opennewadgdatasetadgdataset-ds)([AdgDataSet&](/reference/datagate/datagate-client/adg-data-set.html)) | Opens a new AdgDataSet for the FileAdapter.
| [OpenSimpleQuery](#void-opensimplequeryadgdataset-ds-string-queryfile-string-query-string--keynames-keyusages--keyflags)([AdgDataSet&](/reference/datagate/datagate-client/adg-data-set.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.string), [KeyUsages\[\]](/reference/datagate/datagate-common/key-usages.html)) | Opens the FileAdapter with a simple query.
| [ReadRandomKey](#void-readrandomkeyadgdataset-ds-readrandommode-mode-lockrequest-lr-adgkeytable-keytable)([AdgDataSet](/reference/datagate/datagate-client/adg-data-set.html), [ReadRandomMode](/reference/datagate/datagate-common/read-random-mode.html), [LockRequest](/reference/datagate/datagate-common/lock-request.html), [AdgKeyTable](/reference/datagate/datagate-client/adg-key-table.html)) | Reads a record from the file that the FileAdapter is working with using the specified key.
| [ReadRandomRRN](#void-readrandomrrnadgdataset-ds-readrandommode-mode-lockrequest-lr-long-rrn)([AdgDataSet](/reference/datagate/datagate-client/adg-data-set.html), [ReadRandomMode](/reference/datagate/datagate-common/read-random-mode.html), [LockRequest](/reference/datagate/datagate-common/lock-request.html), [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64)) | Reads a record from the file that the FileAdapter is working with using the specified relative record number (RRN).
| [ReadRange](#void-readrangeadgdataset-ds-rangemode-mode-lockrequest-lr-adgkeytable-firstkey-rangefirst-rangefirst-adgkeytable-lastkey-rangelast-rangelast)([AdgDataSet](/reference/datagate/datagate-client/adg-data-set.html), [RangeMode](/reference/datagate/datagate-common/range-mode.html), [LockRequest](/reference/datagate/datagate-common/lock-request.html), [AdgKeyTable](/reference/datagate/datagate-client/adg-key-table.html), [RangeFirst](/reference/datagate/datagate-common/range-first.html), [AdgKeyTable](/reference/datagate/datagate-client/adg-key-table.html), [RangeLast](/reference/datagate/datagate-common/range-last.html)) | Reads a range of records from the file that the FileAdapter is working with using the specified keys.
| [ReadSequential](#void-readsequentialadgdataset-ds-readsequentialmode-mode-lockrequest-lr)([AdgDataSet](/reference/datagate/datagate-client/adg-data-set.html), [ReadSequentialMode](/reference/datagate/datagate-common/read-sequential-mode.html), [LockRequest](/reference/datagate/datagate-common/lock-request.html)) | Reads a record from the file that the FileAdapter is working with sequentially.
| [ReadSequentialEqual](#void-readsequentialequaladgdataset-ds-readequalmode-mode-lockrequest-lr-adgkeytable-keytable)([AdgDataSet](/reference/datagate/datagate-client/adg-data-set.html), [ReadEqualMode](/reference/datagate/datagate-common/read-equal-mode.html), [LockRequest](/reference/datagate/datagate-common/lock-request.html), [AdgKeyTable](/reference/datagate/datagate-client/adg-key-table.html)) | Reads a record from the file that the FileAdapter is working with sequentially and equal to the specified key.
| [ReleaseCurrent()](#void-releasecurrent) | Releases the lock on the current record in the file that the FileAdapter is working with.
| [ReleaseRRN](#void-releaserrnlockrequest-lr-long-rrn)([LockRequest](/reference/datagate/datagate-common/lock-request.html), [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64)) | Releases the lock on the record at the specified relative record number (RRN) in the file that the FileAdapter is working with.
| [ResetFormat()](#void-resetformat) | Resets the format of the file that the FileAdapter is working with to the default format.
| [ResetPrintAttr()](#void-resetprintattr) | Resets the print attributes for the file that the FileAdapter is working with.
| [ReuseRRN](#void-reuserrnadgdataset-ds-long-rrn)([AdgDataSet](/reference/datagate/datagate-client/adg-data-set.html), [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64)) | Reuses the record at the specified relative record number (RRN) in the file that the FileAdapter is working with.
| [SeekKey](#void-seekkeyseekmode-mode-adgkeytable-keytable)([SeekMode](/reference/datagate/datagate-common/seek-mode.html), [AdgKeyTable](/reference/datagate/datagate-client/adg-key-table.html)) | Positions the file pointer at the record with the specified key in the file that the FileAdapter is working with.
| [SeekRange](#void-seekrangerangemode-mode-adgkeytable-firstkey-rangefirst-rangefirst-adgkeytable-lastkey-rangelast-rangelast)([RangeMode](/reference/datagate/datagate-common/range-mode.html), [AdgKeyTable](/reference/datagate/datagate-client/adg-key-table.html), [RangeFirst](/reference/datagate/datagate-common/range-first.html), [AdgKeyTable](/reference/datagate/datagate-client/adg-key-table.html), [RangeLast](/reference/datagate/datagate-common/range-last.html)) | Positions the file pointer at the first record in the specified range in the file that the FileAdapter is working with.
| [SeekRRN](#void-seekrrnseekmode-mode-long-rrn)([SeekMode](/reference/datagate/datagate-common/seek-mode.html), [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64)) | Positions the file pointer at the record with the specified relative record number (RRN) in the file that the FileAdapter is working with.
| [SetFormat](#void-setformatstring-format)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Sets the format of the file that the FileAdapter is working with to the specified format.
| [ThrowIfNotOpen\<T\>](#t-throwifnotopen-t-t-openstate)([T](https://learn.microsoft.com/en-us/dotnet/api/system.type?view=net-8.0)) | Checks if the provided state is open. If it is, the state is returned. If it is not, an exception is thrown.

### void AddRecord([AdgDataSet ds](/reference/datagate/datagate-client/adg-data-set.html))

Adds a record to the file using the provided AdgDataSet.


#### Remarks
The AddRecord method is used to add a record to the file that the FileAdapter is working with. It first checks if the provided AdgDataSet is null. If it is, it throws an ArgumentNullException. It then calls the AddRecord method of the FileData object of the FileAdapter, passing the provided AdgDataSet. The AddRecord method of the FileData object adds a record to the file with the data from the AdgDataSet. The AdgDataSet should contain the data for the new record in its tables. The structure of the AdgDataSet should match the structure of the file that the FileAdapter is working with.

```cs
void AddRecord(AdgDataSet ds)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [AdgDataSet](/reference/datagate/datagate-client/adg-data-set.html) | ds | The AdgDataSet containing the data for the new record.

### void AddRecord([XmlReader xr](https://learn.microsoft.com/en-us/dotnet/api/system.xml.xmlreader?view=net-8.0), [AdgDataSet ds](/reference/datagate/datagate-client/adg-data-set.html))

Adds a record to the file using the provided XmlReader and AdgDataSet.


#### Remarks
The AddRecord method is used to add a record to the file that the FileAdapter is working with. It first checks if the provided AdgDataSet is null. If it is, it throws an ArgumentNullException. It then calls the AddRecord method of the FileData object of the FileAdapter, passing the provided XmlReader and AdgDataSet. The AddRecord method of the FileData object adds a record to the file with the data from the XmlReader, using the schema from the AdgDataSet. The XmlReader should contain the data for the new record in XML format. The AdgDataSet should contain the schema for the new record. The structure of the AdgDataSet should match the structure of the file that the FileAdapter is working with.

```cs
void AddRecord(XmlReader xr, AdgDataSet ds)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [XmlReader](https://learn.microsoft.com/en-us/dotnet/api/system.xml.xmlreader?view=net-8.0) | xr | The XmlReader containing the data for the new record.
| [AdgDataSet](/reference/datagate/datagate-client/adg-data-set.html) | ds | The AdgDataSet containing the schema for the new record.

### void AddRecord([AdgDataSet ds](/reference/datagate/datagate-client/adg-data-set.html), [Char\[\] appIndicators](https://docs.microsoft.com/en-us/dotnet/api/system.char))

Adds a record to the file using the provided AdgDataSet and application indicators.


#### Remarks
The AddRecord method is used to add a record to the file that the FileAdapter is working with. It first checks if the provided AdgDataSet is null. If it is, it throws an ArgumentNullException. It then calls the AddRecord method of the FileData object of the FileAdapter, passing the provided AdgDataSet and application indicators. The AddRecord method of the FileData object adds a record to the file with the data from the AdgDataSet and the specified application indicators. The AdgDataSet should contain the data for the new record in its tables. The application indicators should be an array of characters that indicate the status of the application for the new record. The structure of the AdgDataSet should match the structure of the file that the FileAdapter is working with.

```cs
void AddRecord(AdgDataSet ds, Char[] appIndicators)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [AdgDataSet](/reference/datagate/datagate-client/adg-data-set.html) | ds | The AdgDataSet containing the data for the new record.
| [Char\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.char) | appIndicators | The application indicators for the new record.

### void ChangeCurrent([AdgDataSet ds](/reference/datagate/datagate-client/adg-data-set.html))

Changes the current record in the file using the provided AdgDataSet.


#### Remarks
The ChangeCurrent method is used to change the current record in the file that the FileAdapter is working with. It first checks if the provided AdgDataSet is null. If it is, it throws an ArgumentNullException. It then calls the ChangeCurrent method of the FileData object of the FileAdapter, passing the provided AdgDataSet. The ChangeCurrent method of the FileData object changes the current record in the file with the data from the AdgDataSet. The AdgDataSet should contain the data for the new record in its tables. The structure of the AdgDataSet should match the structure of the file that the FileAdapter is working with.

```cs
void ChangeCurrent(AdgDataSet ds)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [AdgDataSet](/reference/datagate/datagate-client/adg-data-set.html) | ds | The AdgDataSet containing the data for the new record.

### void ChangeRRN([AdgDataSet ds](/reference/datagate/datagate-client/adg-data-set.html), [long RRN](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Changes the current record in the file to the record at the specified relative record number (RRN).


#### Remarks
The ChangeRRN method is used to change the current record in the file that the FileAdapter is working with to the record at the specified relative record number (RRN). It first checks if the provided AdgDataSet is null. If it is, it throws an ArgumentNullException. It then calls the ChangeRRN method of the FileData object of the FileAdapter, passing the provided AdgDataSet and RRN. The ChangeRRN method of the FileData object changes the current record in the file to the record at the specified RRN with the data from the AdgDataSet. The AdgDataSet should contain the data for the new record in its tables. The structure of the AdgDataSet should match the structure of the file that the FileAdapter is working with.

```cs
void ChangeRRN(AdgDataSet ds, long RRN)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [AdgDataSet](/reference/datagate/datagate-client/adg-data-set.html) | ds | The AdgDataSet containing the data for the new record.
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | RRN | The relative record number of the record to change to.

### void CheckKey([AdgKeyTable keyTable](/reference/datagate/datagate-client/adg-key-table.html))

Checks the validity of the provided key table.


#### Remarks
The CheckKey method is used to check the validity of the provided key table. It first checks if the provided AdgKeyTable is null. If it is, it throws an ArgumentNullException. It then calls the CheckKey method of the FileData object of the FileAdapter, passing the provided AdgKeyTable. The CheckKey method of the FileData object checks the validity of the key table. The AdgKeyTable should contain the keys for the records in the file that the FileAdapter is working with. If the key table is not valid, the CheckKey method throws an exception.

```cs
void CheckKey(AdgKeyTable keyTable)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [AdgKeyTable](/reference/datagate/datagate-client/adg-key-table.html) | keyTable | The AdgKeyTable to check.

### void Close()

Closes the FileAdapter and releases all resources used by it.


#### Remarks
The Close method is used to close the FileAdapter and release all resources used by it. It calls the Dispose method, which releases both managed and unmanaged resources. After the Close method is called, the FileAdapter can no longer be used unless it is reopened with a new connection, file name, and member name. It is recommended to call this method when you are finished using the FileAdapter to free up system resources.

```cs
void Close()
```

### AdgDataSet CreateDataSet()

Creates a new AdgDataSet for the FileAdapter.


#### Remarks
The CreateDataSet method is used to create a new AdgDataSet for the FileAdapter. It first calls the PrepareParms method to prepare the parameters for the FileAdapter. Then it calls the NewDataSet method of the FileFactory class, passing the FileObject of the FileAdapter. The NewDataSet method creates a new AdgDataSet for the FileObject. The ThrowIfNotOpen method is used to check if the FileObject is null. If it is, it throws an exception. Otherwise, it returns the FileObject. The created AdgDataSet can be used to interact with the data in the file that the FileAdapter is working with.

```cs
AdgDataSet CreateDataSet()
```

### void DeleteAllRecords()

Deletes all records from the file that the FileAdapter is working with.


#### Remarks
The DeleteAllRecords method is used to delete all records from the file that the FileAdapter is working with. It calls the DeleteAllRecords method of the FileData object of the FileAdapter. The DeleteAllRecords method of the FileData object deletes all records from the file. This operation is irreversible, so it should be used with caution. It is recommended to have a backup of the file before calling this method.

```cs
void DeleteAllRecords()
```

### void DeleteCurrent()

Deletes the current record from the file that the FileAdapter is working with.


#### Remarks
The DeleteCurrent method is used to delete the current record from the file that the FileAdapter is working with. It calls the DeleteCurrent method of the FileData object of the FileAdapter. The DeleteCurrent method of the FileData object deletes the current record from the file. This operation is irreversible, so it should be used with caution. It is recommended to have a backup of the file before calling this method.

```cs
void DeleteCurrent()
```

### void DeleteKey([AdgKeyTable keyTable](/reference/datagate/datagate-client/adg-key-table.html))

Deletes the record with the specified key from the file that the FileAdapter is working with.


#### Remarks
The DeleteKey method is used to delete the record with the specified key from the file that the FileAdapter is working with. It first checks if the provided AdgKeyTable is null. If it is, it throws an ArgumentNullException. It then calls the DeleteKey method of the FileData object of the FileAdapter, passing the provided AdgKeyTable. The DeleteKey method of the FileData object deletes the record with the specified key from the file. The AdgKeyTable should contain the key of the record to delete. This operation is irreversible, so it should be used with caution. It is recommended to have a backup of the file before calling this method.

```cs
void DeleteKey(AdgKeyTable keyTable)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [AdgKeyTable](/reference/datagate/datagate-client/adg-key-table.html) | keyTable | The AdgKeyTable containing the key of the record to delete.

### void DeleteRange([AdgKeyTable firstKey](/reference/datagate/datagate-client/adg-key-table.html), [RangeFirst rangeFirst](/reference/datagate/datagate-common/range-first.html), [AdgKeyTable lastKey](/reference/datagate/datagate-client/adg-key-table.html), [RangeLast rangeLast](/reference/datagate/datagate-common/range-last.html))

Deletes a range of records from the file that the FileAdapter is working with.


#### Remarks
The DeleteRange method is used to delete a range of records from the file that the FileAdapter is working with. It first checks if the provided AdgKeyTables are null. If they are, it throws an ArgumentNullException. It then calls the DeleteRange method of the FileData object of the FileAdapter, passing the provided AdgKeyTables and RangeFirst and RangeLast values. The DeleteRange method of the FileData object deletes the range of records from the file. The AdgKeyTables should contain the keys of the first and last records in the range to delete. The RangeFirst and RangeLast values indicate whether to include the first and last records in the deletion. This operation is irreversible, so it should be used with caution. It is recommended to have a backup of the file before calling this method.

```cs
void DeleteRange(AdgKeyTable firstKey, RangeFirst rangeFirst, AdgKeyTable lastKey, RangeLast rangeLast)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [AdgKeyTable](/reference/datagate/datagate-client/adg-key-table.html) | firstKey | The AdgKeyTable containing the key of the first record in the range to delete.
| [RangeFirst](/reference/datagate/datagate-common/range-first.html) | rangeFirst | The RangeFirst value indicating whether to include the first record in the deletion.
| [AdgKeyTable](/reference/datagate/datagate-client/adg-key-table.html) | lastKey | The AdgKeyTable containing the key of the last record in the range to delete.
| [RangeLast](/reference/datagate/datagate-common/range-last.html) | rangeLast | The RangeLast value indicating whether to include the last record in the deletion.

### void DeleteRRN([long RRN](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Deletes the record at the specified relative record number (RRN) from the file that the FileAdapter is working with.


#### Remarks
The DeleteRRN method is used to delete the record at the specified relative record number (RRN) from the file that the FileAdapter is working with. It calls the DeleteRRN method of the FileData object of the FileAdapter, passing the provided RRN. The DeleteRRN method of the FileData object deletes the record at the specified RRN from the file. This operation is irreversible, so it should be used with caution. It is recommended to have a backup of the file before calling this method.

```cs
void DeleteRRN(long RRN)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | RRN | The relative record number of the record to delete.

### void Dispose()

Releases all resources used by the FileAdapter.


#### Remarks
The Dispose method is used to release all resources used by the FileAdapter. It calls the Dispose method with true as the argument, indicating that the FileAdapter is being explicitly disposed by the user, not cleaned up by the garbage collector. This means that both managed and unmanaged resources should be released. It also calls the GC.SuppressFinalize method, which prevents the garbage collector from calling the finalizer of the FileAdapter. This is done because the Dispose method has already done all the cleanup necessary. After the Dispose method is called, the FileAdapter can no longer be used unless it is reopened with a new connection, file name, and member name. It is recommended to call this method when you are finished using the FileAdapter to free up system resources.

```cs
void Dispose()
```

### void Dispose([bool isDisposing](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Releases the unmanaged resources used by the FileAdapter and optionally releases the managed resources.


#### Remarks
The Dispose method is used to release the resources used by the FileAdapter. If the isDisposing parameter is true, both managed and unmanaged resources are released. If the isDisposing parameter is false, only unmanaged resources are released. This method is called by the public Dispose method and the Finalize method. Dispose invokes the protected Dispose method with the isDisposing parameter set to true. Finalize invokes Dispose with isDisposing set to false.When the isDisposing parameter is true, this method releases all resources held by any managed objects that this FileAdapter references. This method invokes the Dispose method of every object in m_file and FileObject that implements the IDisposable interface.

```cs
void Dispose(bool isDisposing)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | isDisposing | true to release both managed and unmanaged resources; false to release only unmanaged resources.

### void Finalize()

Finalizes an instance of the FileAdapter class.


#### Remarks
This destructor is called when the garbage collector finalizes an instance of the FileAdapter class. It calls the Dispose method with false as the argument, indicating that the FileAdapter is being cleaned up by the garbage collector, not explicitly disposed by the user. This means that only unmanaged resources should be released, as managed resources will be released by the garbage collector.

```cs
void Finalize()
```

### void ForceEOD()

Forces the end of data (EOD) for the file that the FileAdapter is working with.


#### Remarks
The ForceEOD method is used to force the end of data (EOD) for the file that the FileAdapter is working with. It calls the ForceEOD method of the FileData object of the FileAdapter, passing the member name and open attributes of the FileAdapter. The ForceEOD method of the FileData object forces the EOD for the file. This method is typically used when you have finished reading or writing data to the file and want to ensure that all data has been processed.

```cs
void ForceEOD()
```

### string GetFormatName([int i](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Gets the name of the format at the specified index in the file that the FileAdapter is working with.


#### Remarks
The GetFormatName method is used to get the name of the format at the specified index in the file that the FileAdapter is working with. It first checks if the FileAdapter is currently working with a file (i.e., the FileData object of the FileAdapter is not null). If it is not, it throws an InvalidOperationException. It then calls the GetFormatName method of the FileData object of the FileAdapter, passing the provided index. The GetFormatName method of the FileData object returns the name of the format at the specified index in the file. This method is typically used when you need to know the name of a specific format in the file.

```cs
string GetFormatName(int i)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | i | The index of the format to get the name of.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The name of the format at the specified index.

### IPrintProperties GetPrintProperties([string format](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Gets the print properties for the specified format in the file that the FileAdapter is working with.


#### Remarks
The GetPrintProperties method is used to get the print properties for the specified format in the file that the FileAdapter is working with. It first checks if the file is a print file by checking if the ExtendedResults of the FileData object of the FileAdapter contains the key "NetPrintFile". If the file is a print file, it gets the PrintFile object from the ExtendedResults and calls its GetPrintProperties method, passing the provided format name. The GetPrintProperties method of the PrintFile object returns the print properties for the specified format. If the file is not a print file, it throws an dgException with the error number dgEcINVFILETYPE. This method is typically used when you need to get the print properties for a specific format in a print file.

```cs
IPrintProperties GetPrintProperties(string format)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | format | The name of the format to get the print properties for.

#### Returns

| Type | Description
| --- | ---
| [IPrintProperties](/reference/datagate/datagate-providers/i-print-properties.html) | The print properties for the specified format, or null if the file is not a print file.

### void Open([AdgDataSet ds](/reference/datagate/datagate-client/adg-data-set.html))

Opens the FileAdapter with the specified AdgDataSet.


#### Remarks
The Open method is used to open the FileAdapter with the specified AdgDataSet. It first checks if the FileAdapter is already open. If it is, it throws an exception. Then it calls the PrepareParms method to prepare the parameters for the FileAdapter. It then calls the NewFileData method of the FileFactory class, passing the FileObject and member name of the FileAdapter, the access mode, the open attributes, and a reference to the AdgDataSet. The NewFileData method creates a new FileData object for the FileObject and member name, with the specified access mode and open attributes, and assigns it to the AdgDataSet. The AdgDataSet can be used to interact with the data in the file that the FileAdapter is working with.

```cs
void Open(AdgDataSet ds)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [AdgDataSet](/reference/datagate/datagate-client/adg-data-set.html) | ds | The AdgDataSet to use for the FileAdapter.

### void OpenNewAdgDataSet([AdgDataSet& ds](/reference/datagate/datagate-client/adg-data-set.html))

Opens a new AdgDataSet for the FileAdapter.


#### Remarks
The OpenNewAdgDataSet method is used to open a new AdgDataSet for the FileAdapter. It first checks if the FileAdapter is already open. If it is, it throws an exception. Then it calls the PrepareParms method to prepare the parameters for the FileAdapter. It then calls the NewFileData method of the FileFactory class, passing the FileObject and member name of the FileAdapter, the access mode, the open attributes, and a reference to the new AdgDataSet. The NewFileData method creates a new FileData object for the FileObject and member name, with the specified access mode and open attributes, and assigns it to the new AdgDataSet. The new AdgDataSet can be used to interact with the data in the file that the FileAdapter is working with.

```cs
void OpenNewAdgDataSet(AdgDataSet& ds)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [AdgDataSet&](/reference/datagate/datagate-client/adg-data-set.html) | ds | The new AdgDataSet that is opened.

### void OpenSimpleQuery([AdgDataSet& ds](/reference/datagate/datagate-client/adg-data-set.html), [string queryFile](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string query](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [String\[\] keyNames](https://docs.microsoft.com/en-us/dotnet/api/system.string), [KeyUsages\[\] keyFlags](/reference/datagate/datagate-common/key-usages.html))

Opens the FileAdapter with a simple query.


#### Remarks
The OpenSimpleQuery method is used to open the FileAdapter with a simple query. It first checks if the FileAdapter is already open. If it is, it throws an exception. It then checks if the keyNames and keyFlags parameters are valid. If they are not, it throws an exception. It also checks if the query and queryFile parameters are not null. If they are, it throws an exception. It then sets the query, queryFile, queryKeyNames, and queryKeyUsage properties of the FileAdapter to the provided values. It then calls the PrepareParms method to prepare the parameters for the FileAdapter. It then calls the NewFileData method of the FileFactory class, passing the FileObject and member name of the FileAdapter, the access mode, the open attributes, a reference to the AdgDataSet, and the query parameters. The NewFileData method creates a new FileData object for the FileObject and member name, with the specified access mode and open attributes, and assigns it to the AdgDataSet. The AdgDataSet can be used to interact with the data in the file that the FileAdapter is working with.

```cs
void OpenSimpleQuery(AdgDataSet& ds, string queryFile, string query, String[] keyNames, KeyUsages[] keyFlags)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [AdgDataSet&](/reference/datagate/datagate-client/adg-data-set.html) | ds | The AdgDataSet to use for the FileAdapter.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | queryFile | The file to query.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | query | The query to execute.
| [String\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.string) | keyNames | The names of the keys to use in the query.
| [KeyUsages\[\]](/reference/datagate/datagate-common/key-usages.html) | keyFlags | The flags to use for the keys in the query.

### void ReadRandomKey([AdgDataSet ds](/reference/datagate/datagate-client/adg-data-set.html), [ReadRandomMode mode](/reference/datagate/datagate-common/read-random-mode.html), [LockRequest lr](/reference/datagate/datagate-common/lock-request.html), [AdgKeyTable keyTable](/reference/datagate/datagate-client/adg-key-table.html))

Reads a record from the file that the FileAdapter is working with using the specified key.


#### Remarks
The ReadRandomKey method is used to read a record from the file that the FileAdapter is working with using the specified key. It first checks if the provided AdgDataSet is null. If it is, it throws an ArgumentNullException. It then calls the ReadRandomKey method of the FileData object of the FileAdapter, passing the provided AdgDataSet, ReadRandomMode, LockRequest, and AdgKeyTable. The ReadRandomKey method of the FileData object reads the record with the specified key from the file and fills the AdgDataSet with the data from the record. The AdgDataSet should be empty before calling this method. The structure of the AdgDataSet should match the structure of the file that the FileAdapter is working with.

```cs
void ReadRandomKey(AdgDataSet ds, ReadRandomMode mode, LockRequest lr, AdgKeyTable keyTable)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [AdgDataSet](/reference/datagate/datagate-client/adg-data-set.html) | ds | The AdgDataSet to fill with the data from the record.
| [ReadRandomMode](/reference/datagate/datagate-common/read-random-mode.html) | mode | The ReadRandomMode to use when reading the record.
| [LockRequest](/reference/datagate/datagate-common/lock-request.html) | lr | The LockRequest to use when reading the record.
| [AdgKeyTable](/reference/datagate/datagate-client/adg-key-table.html) | keyTable | The AdgKeyTable containing the key of the record to read.

### void ReadRandomRRN([AdgDataSet ds](/reference/datagate/datagate-client/adg-data-set.html), [ReadRandomMode mode](/reference/datagate/datagate-common/read-random-mode.html), [LockRequest lr](/reference/datagate/datagate-common/lock-request.html), [long RRN](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Reads a record from the file that the FileAdapter is working with using the specified relative record number (RRN).


#### Remarks
The ReadRandomRRN method is used to read a record from the file that the FileAdapter is working with using the specified relative record number (RRN). It first checks if the provided AdgDataSet is null. If it is, it throws an ArgumentNullException. It then calls the ReadRandomRRN method of the FileData object of the FileAdapter, passing the provided AdgDataSet, ReadRandomMode, LockRequest, and RRN. The ReadRandomRRN method of the FileData object reads the record at the specified RRN from the file and fills the AdgDataSet with the data from the record. The AdgDataSet should be empty before calling this method. The structure of the AdgDataSet should match the structure of the file that the FileAdapter is working with.

```cs
void ReadRandomRRN(AdgDataSet ds, ReadRandomMode mode, LockRequest lr, long RRN)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [AdgDataSet](/reference/datagate/datagate-client/adg-data-set.html) | ds | The AdgDataSet to fill with the data from the record.
| [ReadRandomMode](/reference/datagate/datagate-common/read-random-mode.html) | mode | The ReadRandomMode to use when reading the record.
| [LockRequest](/reference/datagate/datagate-common/lock-request.html) | lr | The LockRequest to use when reading the record.
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | RRN | The relative record number of the record to read.

### void ReadRange([AdgDataSet ds](/reference/datagate/datagate-client/adg-data-set.html), [RangeMode mode](/reference/datagate/datagate-common/range-mode.html), [LockRequest lr](/reference/datagate/datagate-common/lock-request.html), [AdgKeyTable firstKey](/reference/datagate/datagate-client/adg-key-table.html), [RangeFirst rangeFirst](/reference/datagate/datagate-common/range-first.html), [AdgKeyTable lastKey](/reference/datagate/datagate-client/adg-key-table.html), [RangeLast rangeLast](/reference/datagate/datagate-common/range-last.html))

Reads a range of records from the file that the FileAdapter is working with using the specified keys.


#### Remarks
The ReadRange method is used to read a range of records from the file that the FileAdapter is working with using the specified keys. It first checks if the provided AdgDataSet is null. If it is, it throws an ArgumentNullException. It then calls the ReadRange method of the FileData object of the FileAdapter, passing the provided AdgDataSet, RangeMode, LockRequest, AdgKeyTables, and RangeFirst and RangeLast values. The ReadRange method of the FileData object reads the range of records from the file and fills the AdgDataSet with the data from the records. The AdgDataSet should be empty before calling this method. The structure of the AdgDataSet should match the structure of the file that the FileAdapter is working with.

```cs
void ReadRange(AdgDataSet ds, RangeMode mode, LockRequest lr, AdgKeyTable firstKey, RangeFirst rangeFirst, AdgKeyTable lastKey, RangeLast rangeLast)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [AdgDataSet](/reference/datagate/datagate-client/adg-data-set.html) | ds | The AdgDataSet to fill with the data from the records.
| [RangeMode](/reference/datagate/datagate-common/range-mode.html) | mode | The RangeMode to use when reading the records.
| [LockRequest](/reference/datagate/datagate-common/lock-request.html) | lr | The LockRequest to use when reading the records.
| [AdgKeyTable](/reference/datagate/datagate-client/adg-key-table.html) | firstKey | The AdgKeyTable containing the key of the first record in the range to read.
| [RangeFirst](/reference/datagate/datagate-common/range-first.html) | rangeFirst | The RangeFirst value indicating whether to include the first record in the read.
| [AdgKeyTable](/reference/datagate/datagate-client/adg-key-table.html) | lastKey | The AdgKeyTable containing the key of the last record in the range to read.
| [RangeLast](/reference/datagate/datagate-common/range-last.html) | rangeLast | The RangeLast value indicating whether to include the last record in the read.

### void ReadSequential([AdgDataSet ds](/reference/datagate/datagate-client/adg-data-set.html), [ReadSequentialMode mode](/reference/datagate/datagate-common/read-sequential-mode.html), [LockRequest lr](/reference/datagate/datagate-common/lock-request.html))

Reads a record from the file that the FileAdapter is working with sequentially.


#### Remarks
The ReadSequential method is used to read a record from the file that the FileAdapter is working with sequentially. It first checks if the provided AdgDataSet is null. If it is, it throws an ArgumentNullException. It then calls the ReadSequential method of the FileData object of the FileAdapter, passing the provided AdgDataSet, ReadSequentialMode, and LockRequest. The ReadSequential method of the FileData object reads the next record in the file and fills the AdgDataSet with the data from the record. The AdgDataSet should be empty before calling this method. The structure of the AdgDataSet should match the structure of the file that the FileAdapter is working with.

```cs
void ReadSequential(AdgDataSet ds, ReadSequentialMode mode, LockRequest lr)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [AdgDataSet](/reference/datagate/datagate-client/adg-data-set.html) | ds | The AdgDataSet to fill with the data from the record.
| [ReadSequentialMode](/reference/datagate/datagate-common/read-sequential-mode.html) | mode | The ReadSequentialMode to use when reading the record.
| [LockRequest](/reference/datagate/datagate-common/lock-request.html) | lr | The LockRequest to use when reading the record.

### void ReadSequentialEqual([AdgDataSet ds](/reference/datagate/datagate-client/adg-data-set.html), [ReadEqualMode mode](/reference/datagate/datagate-common/read-equal-mode.html), [LockRequest lr](/reference/datagate/datagate-common/lock-request.html), [AdgKeyTable keyTable](/reference/datagate/datagate-client/adg-key-table.html))

Reads a record from the file that the FileAdapter is working with sequentially and equal to the specified key.


#### Remarks
The ReadSequentialEqual method is used to read a record from the file that the FileAdapter is working with sequentially and equal to the specified key. It first checks if the provided AdgDataSet is null. If it is, it throws an ArgumentNullException. It then calls the ReadSequentialEqual method of the FileData object of the FileAdapter, passing the provided AdgDataSet, ReadEqualMode, LockRequest, and AdgKeyTable. The ReadSequentialEqual method of the FileData object reads the next record in the file that is equal to the specified key and fills the AdgDataSet with the data from the record. The AdgDataSet should be empty before calling this method. The structure of the AdgDataSet should match the structure of the file that the FileAdapter is working with.

```cs
void ReadSequentialEqual(AdgDataSet ds, ReadEqualMode mode, LockRequest lr, AdgKeyTable keyTable)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [AdgDataSet](/reference/datagate/datagate-client/adg-data-set.html) | ds | The AdgDataSet to fill with the data from the record.
| [ReadEqualMode](/reference/datagate/datagate-common/read-equal-mode.html) | mode | The ReadEqualMode to use when reading the record.
| [LockRequest](/reference/datagate/datagate-common/lock-request.html) | lr | The LockRequest to use when reading the record.
| [AdgKeyTable](/reference/datagate/datagate-client/adg-key-table.html) | keyTable | The AdgKeyTable containing the key of the record to read.

### void ReleaseCurrent()

Releases the lock on the current record in the file that the FileAdapter is working with.


#### Remarks
The ReleaseCurrent method is used to release the lock on the current record in the file that the FileAdapter is working with. It calls the ReleaseCurrent method of the FileData object of the FileAdapter. The ReleaseCurrent method of the FileData object releases the lock on the current record in the file. This method should be called after you have finished working with a record that you have locked, to allow other users to access the record.

```cs
void ReleaseCurrent()
```

### void ReleaseRRN([LockRequest lr](/reference/datagate/datagate-common/lock-request.html), [long RRN](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Releases the lock on the record at the specified relative record number (RRN) in the file that the FileAdapter is working with.


#### Remarks
The ReleaseRRN method is used to release the lock on the record at the specified relative record number (RRN) in the file that the FileAdapter is working with. It first checks if the provided LockRequest is a ReadWrite lock. If it is not, it throws a dgException. It then calls the ReleaseRRN method of the FileData object of the FileAdapter, passing the provided LockRequest and RRN. The ReleaseRRN method of the FileData object releases the lock on the record at the specified RRN in the file. This method should be called after you have finished working with a record that you have locked, to allow other users to access the record.

```cs
void ReleaseRRN(LockRequest lr, long RRN)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [LockRequest](/reference/datagate/datagate-common/lock-request.html) | lr | The LockRequest to use when releasing the lock.
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | RRN | The relative record number of the record to release the lock on.

### void ResetFormat()

Resets the format of the file that the FileAdapter is working with to the default format.


#### Remarks
The ResetFormat method is used to reset the format of the file that the FileAdapter is working with to the default format. It calls the ResetFormat method of the FileData object of the FileAdapter. The ResetFormat method of the FileData object resets the format of the file to the default format. This method is typically used when you have changed the format of the file using the SetFormat method and you want to reset it to the default format.

```cs
void ResetFormat()
```

### void ResetPrintAttr()

Resets the print attributes for the file that the FileAdapter is working with.


#### Remarks
The ResetPrintAttr method is used to reset the print attributes for the file that the FileAdapter is working with. It first checks if the FileAdapter is currently working with a file (i.e., the FileData object of the FileAdapter is not null). If it is not, it throws an InvalidOperationException. It then calls the ResetPrintAttr method of the FileData object of the FileAdapter, passing the member name and the open attributes. The ResetPrintAttr method of the FileData object resets the print attributes for the file. This method is typically used when you have changed the print attributes of the file and you want to reset them to their default values.

```cs
void ResetPrintAttr()
```

### void ReuseRRN([AdgDataSet ds](/reference/datagate/datagate-client/adg-data-set.html), [long RRN](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Reuses the record at the specified relative record number (RRN) in the file that the FileAdapter is working with.


#### Remarks
The ReuseRRN method is used to reuse the record at the specified relative record number (RRN) in the file that the FileAdapter is working with. It first checks if the provided AdgDataSet is null. If it is, it throws an ArgumentNullException. It then calls the ReuseRRN method of the FileData object of the FileAdapter, passing the provided AdgDataSet and RRN. The ReuseRRN method of the FileData object reuses the record at the specified RRN in the file and fills the AdgDataSet with the data from the record. The AdgDataSet should be empty before calling this method. The structure of the AdgDataSet should match the structure of the file that the FileAdapter is working with.

```cs
void ReuseRRN(AdgDataSet ds, long RRN)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [AdgDataSet](/reference/datagate/datagate-client/adg-data-set.html) | ds | The AdgDataSet to fill with the data from the record.
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | RRN | The relative record number of the record to reuse.

### void SeekKey([SeekMode mode](/reference/datagate/datagate-common/seek-mode.html), [AdgKeyTable keyTable](/reference/datagate/datagate-client/adg-key-table.html))

Positions the file pointer at the record with the specified key in the file that the FileAdapter is working with.


#### Remarks
The SeekKey method is used to position the file pointer at the record with the specified key in the file that the FileAdapter is working with. It first checks if the provided AdgKeyTable is null. If it is, it throws an ArgumentNullException. It then calls the SeekKey method of the FileData object of the FileAdapter, passing the provided SeekMode and AdgKeyTable. The SeekKey method of the FileData object positions the file pointer at the record with the specified key in the file. This method does not read the record; it only positions the file pointer. To read the record after calling this method, you can use the ReadRandomKey or ReadSequential methods.

```cs
void SeekKey(SeekMode mode, AdgKeyTable keyTable)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [SeekMode](/reference/datagate/datagate-common/seek-mode.html) | mode | The SeekMode to use when seeking the record.
| [AdgKeyTable](/reference/datagate/datagate-client/adg-key-table.html) | keyTable | The AdgKeyTable containing the key of the record to seek.

### void SeekRange([RangeMode mode](/reference/datagate/datagate-common/range-mode.html), [AdgKeyTable firstKey](/reference/datagate/datagate-client/adg-key-table.html), [RangeFirst rangeFirst](/reference/datagate/datagate-common/range-first.html), [AdgKeyTable lastKey](/reference/datagate/datagate-client/adg-key-table.html), [RangeLast rangeLast](/reference/datagate/datagate-common/range-last.html))

Positions the file pointer at the first record in the specified range in the file that the FileAdapter is working with.


#### Remarks
The SeekRange method is used to position the file pointer at the first record in the specified range in the file that the FileAdapter is working with. It first checks if the provided AdgKeyTables are null. If they are, it throws an ArgumentNullException. It then calls the SeekRange method of the FileData object of the FileAdapter, passing the provided SeekMode, AdgKeyTables, and RangeFirst and RangeLast values. The SeekRange method of the FileData object positions the file pointer at the first record in the specified range in the file. This method does not read the record; it only positions the file pointer. To read the record after calling this method, you can use the ReadRange method.

```cs
void SeekRange(RangeMode mode, AdgKeyTable firstKey, RangeFirst rangeFirst, AdgKeyTable lastKey, RangeLast rangeLast)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [RangeMode](/reference/datagate/datagate-common/range-mode.html) | mode | The SeekMode to use when seeking the record.
| [AdgKeyTable](/reference/datagate/datagate-client/adg-key-table.html) | firstKey | The AdgKeyTable containing the key of the first record in the range to seek.
| [RangeFirst](/reference/datagate/datagate-common/range-first.html) | rangeFirst | The RangeFirst value indicating whether to include the first record in the seek.
| [AdgKeyTable](/reference/datagate/datagate-client/adg-key-table.html) | lastKey | The AdgKeyTable containing the key of the last record in the range to seek.
| [RangeLast](/reference/datagate/datagate-common/range-last.html) | rangeLast | The RangeLast value indicating whether to include the last record in the seek.

### void SeekRRN([SeekMode mode](/reference/datagate/datagate-common/seek-mode.html), [long RRN](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Positions the file pointer at the record with the specified relative record number (RRN) in the file that the FileAdapter is working with.


#### Remarks
The SeekRRN method is used to position the file pointer at the record with the specified relative record number (RRN) in the file that the FileAdapter is working with. It calls the SeekRRN method of the FileData object of the FileAdapter, passing the provided SeekMode and RRN. The SeekRRN method of the FileData object positions the file pointer at the record with the specified RRN in the file. This method does not read the record; it only positions the file pointer. To read the record after calling this method, you can use the ReadRandomRRN or ReadSequential methods.

```cs
void SeekRRN(SeekMode mode, long RRN)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [SeekMode](/reference/datagate/datagate-common/seek-mode.html) | mode | The SeekMode to use when seeking the record.
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | RRN | The relative record number of the record to seek.

### void SetFormat([string Format](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Sets the format of the file that the FileAdapter is working with to the specified format.


#### Remarks
The SetFormat method is used to set the format of the file that the FileAdapter is working with to the specified format. It first checks if the FileAdapter is currently working with a file (i.e., the FileData object of the FileAdapter is not null). If it is not, it throws an InvalidOperationException. It then calls the SetFormat method of the FileData object of the FileAdapter, passing the provided format name. The SetFormat method of the FileData object sets the format of the file to the specified format. This method is typically used when you need to change the format of the file to a specific format.

```cs
void SetFormat(string Format)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | Format | The name of the format to set.

### T ThrowIfNotOpen\<T\>([T openState](https://learn.microsoft.com/en-us/dotnet/api/system.type?view=net-8.0))

Checks if the provided state is open. If it is, the state is returned. If it is not, an exception is thrown.


#### Remarks
This method is used to ensure that a certain state (like a file or a connection) is open before proceeding with operations that require it to be open.If the state is not open (i.e., it is null), it throws a dgException with a specific error number and a message indicating that the file adapter is not open.

```cs
T ThrowIfNotOpen<T>(T openState)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [T](https://learn.microsoft.com/en-us/dotnet/api/system.type?view=net-8.0) | openState | The state to check.

#### Returns

| Type | Description
| --- | ---
| [T](https://learn.microsoft.com/en-us/dotnet/api/system.type?view=net-8.0) | The open state if it is not null.

## Examples
Most of the following examples create an AdgConnection by calling the `createAdgConnection()` method which is part of the [AdgConnection Example](/reference/datagate/datagate-client/adg-connection.html#create-an-adgconnection) showing how to `new` an `AdgConnection` using a Database Source Profile Name.


### Example 1. Use of WaitForRecord Open attribute property. 


```cs 
  /* Opens a record which will spend no time waiting for a record
   * if that record is locked. */
  AdgConnection db = createAdgConnection("MyDatabaseName");
  FileAdapter dbFile = new FileAdapter(db, "*Libl/CMASTNEW", "CMMASTER");
  dbFile.AccessMode = AccessMode.Delete;
  dbFile.OpenAttributes.WaitForRecord = 0;
  AdgDataSet myDS = null;
  dbFile.OpenNewAdgDataSet(out myDS);

```


### Example 2. Use of ShareTypes Open attribute property.

```cs 
  /* We open the file in order to delete all of its records. */
  AdgConnection db = createAdgConnection("MyDatabaseName");
  FileAdapter dbFile = new FileAdapter(db, "*Libl/CMASTNEW", "CMMASTER");
  dbFile.AccessMode = AccessMode.Delete;
  /* Its generally good practice to make sure you have an exclusive lock
   * on a file that you are deleting all of the records from, but some
   * databases do not require it. */
  dbFile.OpenAttributes.ShareTypes = ShareTypes.Exclusive;
  AdgDataSet myDS = null;

  try
  {
      dbFile.Open(myDS);
      dbFile.DeleteAllRecords();
  }
  catch(dgException dgEx)
  {
      db.Close();
      if (dgEx.Error == dgErrorNumber.dgEmBUSYOBJ)
      {
          MessageBox.Show("Couldn't open the file for exclusive access.", "Error opening file.");
          //Exit routine or procedure here to avoid preceding file operations.
      }
      else 
          throw dgEx;
  }
  dbFile.DeleteAllRecords();

  dbFile.Close();
  db.Close();
```

### Example 3. Use of BlockingFactor Open attribute property.

```cs 
  AdgConnection db = createAdgConnection("MyDatabaseName");
  FileAdapter dbFile = new FileAdapter(db, "*Libl/CMASTNEWL1", "CMMASTERL1");
  dbFile.AccessMode = AccessMode.Read;

  /* Automatically calculates the best blocking factor. */
  dbFile.OpenAttributes.BlockingFactor = FileOpenAttr.OptimalBlockingFactor;
  AdgDataSet ds = null;
  dbFile.OpenNewAdgDataSet(out ds);
```

### Example 4. Use of OmitBlocking BlockingFactor Open attribute property.

```cs
  AdgConnection db = createAdgConnection("MyDatabaseName"); 
  FileAdapter dbFile = new FileAdapter(db, "*Libl/CMASTNEWL1", "CMMASTERL1"); 
  dbFile.AccessMode = AccessMode.Read; /* Omits record blocking feature. */
  dbFile.OpenAttributes.BlockingFactor = FileOpenAttr.OmitBlocking;
  AdgDataSet ds = null;
  dbFile.OpenNewAdgDataSet(out ds);
```

### Example 5. Using the FileLocks property of a FileAdapter's OpenAttributes

```cs 
  /* Using the FileLocks property of a FileAdapter's OpenAttributes,
   * you can set file locking to manual, which allows you to lock more
   * than one record at a time. Note that manual file locking
   * is database dependent- for instance, it will work with a Acceler8
   * database but not with an IBM i. */
  AdgConnection db = createAdgConnection("MyDatabaseName");
  FileAdapter dbFile = new FileAdapter(db, "*Libl/CMASTNEWL1", "CMMASTERL1");
  dbFile.OpenAttributes.FileLocks = FileLocks.Manual;
  dbFile.AccessMode = AccessMode.RWCD;

  AdgDataSet myDS = null;
  dbFile.OpenNewAdgDataSet(out myDS);
  AdgKeyTable keyTbl = myDS.NewKeyTable("RCMMASTL1");

  /* In the code below, we read records for customer numbers
   * 400 - 800. When it ends, we will still have locks on customer numbers
   * 500 and 700. */
  try
  {
      /* Read customer number 400 but don't lock it. */
      keyTbl.Row["CMCUSTNO"] = 400;
      dbFile.ReadRandomKey(myDS, ReadRandomMode.Equal, LockRequest.NoLock, keyTbl);

      /* Read customer number 500 and lock it. */
      keyTbl.Row["CMCUSTNO"] = 500;
      dbFile.ReadRandomKey(myDS, ReadRandomMode.Equal, LockRequest.Read, keyTbl);

      /* Read customer number 600 and lock it. */
      dbFile.ReadSequential(myDS, ReadSequentialMode.Next, LockRequest.Read);

      /* Read customer number 700 and lock it. */
      dbFile.ReadSequential(myDS, ReadSequentialMode.Next, LockRequest.Read);

      /* Read customer number 800 without locking it. */
      dbFile.ReadSequential(myDS, ReadSequentialMode.Next, LockRequest.NoLock);

      /* Unlock customer number 600. */
      keyTbl.Row["CMCUSTNO"] = 600;
      dbFile.ReadRandomKey(myDS, ReadRandomMode.Equal, LockRequest.NoLock, keyTbl);
      dbFile.ReleaseCurrent();

  }
  catch(dgException dgEx)
  { 
      MessageBox.Show("Couldn't find one or more records. " + dgEx.Message,
          dgEx.Error.ToString());
  }

  dbFile.Close(); /* Release all locks. */
  db.Close();
```

### Example 6. Using an specific BlockingFactor value to periodically update a progress bar.

```cs 
  AdgConnection db = createAdgConnection("MyDatabaseName");
  FileAdapter dbFile = new FileAdapter(db, "*Libl/CMASTNEWL1", "CMMASTERL1");
  dbFile.AccessMode = AccessMode.Read;
  AdgDataSet myDS = null;

  int refreshInterval = 10; //Used so we don't slow down refreshing too much...
  dbFile.OpenAttributes.BlockingFactor = refreshInterval;
  dbFile.OpenNewAdgDataSet(out myDS);

    /* Here, we read every record until end of file is reached.
    * Because this is an fairly long process, we set up a progress bar
    * to keep the user from being discouraged. We set its Maximum
    * value to the number of records in the file, which is found
    * using FileAdapter's RecordCount property, divided by
    * our refreshInterval. */
  int recordsReadSinceLastRefresh = 0;
  prgBar.Minimum = 0;
  prgBar.Maximum = Convert.ToInt32(dbFile.RecordCount) / refreshInterval;

  bool EOF = false;
  while(!EOF)
  {
      try
      {
         /* Though it seems like we have to read each record one at a time,
          * in reality DG stores the first 10 records the first time we read
          * and then afterwards we simply read from the cache. When those run out, 
          * DG will automatically grab another ten records from the database.
          * Note that 10 is our refresh interval, meaning that this I/O operation
          * occurs at the same time that we update our progress bar. If the blocking
          * factor was higher than our refresh interval, not only would we have to 
          * wait longer to read the first record but the progress bar would go longer
          * without being updated. */
         dbFile.ReadSequential(myDS, ReadSequentialMode.Next, LockRequest.NoWait);
         /* Perform some action on each record here... */
         recordsReadSinceLastRefresh ++;
         if (recordsReadSinceLastRefresh == refreshInterval)
         {
             recordsReadSinceLastRefresh = 0;
             prgBar.PerformStep();
             this.Refresh(); //Refreshes the form.
         }
      }
      catch(dgException dgEx)
      {
          if (dgEx.Error == dgErrorNumber.dgEaEOF)
              EOF = true;
          else
          {
              //Exit procedure or end application here.
          }
      }
  }
  dbFile.Close();
  db.Close()
```


### Example 7. Use of FileLocks enumeration to allow locking more than one record at a time.

```cs 
  /* Using the FileLocks property of a FileAdapter's OpenAttributes,
   * you can set file locking to manual, which allows you to lock more
   * than one record at a time. Note that manual file locking
   * is database dependent- for instance, it will work with a Acceler8
   * database but not with an IBM i. */
  AdgConnection db = createAdgConnection("MyDatabaseName");
  FileAdapter dbFile = new FileAdapter(db, "*Libl/CMASTNEWL1", "CMMASTERL1");
  dbFile.OpenAttributes.FileLocks = FileLocks.Manual;
  dbFile.AccessMode = AccessMode.RWCD;

  AdgDataSet myDS = null;
  dbFile.OpenNewAdgDataSet(out myDS);
  AdgKeyTable keyTbl = myDS.NewKeyTable("RCMMASTL1");

  /* In the code below, we read records for customer numbers
   * 400 - 800. When it ends, we will still have locks on customer numbers
   * 500 and 700. */
  try
  {
      /* Read customer number 400 but don't lock it. */
      keyTbl.Row["CMCUSTNO"] = 400;
      dbFile.ReadRandomKey(myDS, ReadRandomMode.Equal, LockRequest.NoLock, keyTbl);

      /* Read customer number 500 and lock it. */
      keyTbl.Row["CMCUSTNO"] = 500;
      dbFile.ReadRandomKey(myDS, ReadRandomMode.Equal, LockRequest.Read, keyTbl);

      /* Read customer number 600 and lock it. */
      dbFile.ReadSequential(myDS, ReadSequentialMode.Next, LockRequest.Read);

      /* Read customer number 700 and lock it. */
      dbFile.ReadSequential(myDS, ReadSequentialMode.Next, LockRequest.Read);

      /* Read customer number 800 without locking it. */
      dbFile.ReadSequential(myDS, ReadSequentialMode.Next, LockRequest.NoLock);

      /* Unlock customer number 600. */
      keyTbl.Row["CMCUSTNO"] = 600;
      dbFile.ReadRandomKey(myDS, ReadRandomMode.Equal, LockRequest.NoLock, keyTbl);
      dbFile.ReleaseCurrent();

  }
  catch(dgException dgEx)
  {
      MessageBox.Show("Couldn't find one or more records. " + dgEx.Message,
      dgEx.Error.ToString());
  }

  dbFile.Close(); /* Release all locks. */
  db.Close();
```


### Example 8. Checking the status of a FileAdapter object before using it.

Using a fileAdapter object named "dbFile" but are unsure as to whether or not it is been initialized, so we check for null and use the Status property to make sure it is opened and open it if it isn't.

```cs 
  if (dbFile == null)
      dbFile = new FileAdapter();
  if (dbFile.Status == FileAdapter.AdapterStatus.Closed)
  {
      dbFile.SetConnection( myAdgConnection );
      dbFile.FileName = fileName;
      dbFile.MemberName = memberName;
      dbFile.OpenNewAdgDataSet(out myDataSet);
  }
  
```

### Example 9. Use of FileAdapter.SetFormat Method.

```cs 
  /* Read only records from format one. */
  AdgConnection db = createAdgConnection("MyDatabaseName");
  FileAdapter dbFile = new FileAdapter(db, "*Libl/SalesMem", "SalesMem");
  dbFile.AccessMode = AccessMode.Read | AccessMode.Write;
  AdgDataSet myDS = null;
  dbFile.OpenNewAdgDataSet(out myDS);

  /* Add a record to format 0, "RCustMast". */
  /* Get new customer number to avoid adding a duplicate key. */
  dbFile.ReadSequential(myDS, ReadSequentialMode.Last, LockRequest.Read);
  decimal newCustNo = Convert.ToDecimal(myDS.ActiveRow["CMCustNo"]) + 100m;

  DataRow newRecord = myDS.PrepareRow("RCustMast");
  /* Create a customer record. */

  newRecord["CMCustNo"] = newCustNo;
  newRecord["CMName"] = "Amalgamated Software of North America";
  newRecord["CMAddr1"] = "9901 IH-10 West, Suite 1000";
  newRecord["CMCity"] = "San Antonio";
  newRecord["CMState"] = "TX";
  newRecord["CMCntry"] = "US";
  newRecord["CMPostCode"] = "78230";
  newRecord["CMActive"] = "1";
  newRecord["CMPhone"] = "2104080212";

  myDS.AddPreparedRowAndSetActive(0);
  dbFile.SetFormat("RCustMast");
  try
  {
      dbFile.AddRecord(myDS);
  }
  catch(dgException dgEx)
  {
      if (dgEx.Error != dgErrorNumber.dgEaDUPKEY)
          throw dgEx; /* If the 
            exception wasn't thrown due to a duplicate key, throw it again. */
      MessageBox.Show("Key value \"" + 
            newRecord["CMName"].ToString() +
          "\" already in this 
            file.", "Error");
      dbFile.Close();
      db.Close();
      //Exit procedure or take other action here to 
            avoid adding next record.
  }
  /* Now add a record to format 1, "RSalesMast". */
  DataRow newRecord2 = myDS.PrepareRow("RSalesMast");

  /* Create a record of sales for 2004. */
  newRecord2["CSCustNo"] = newRecord["CMCustNo"];
  newRecord2["CSYear"] = 2004m;
  newRecord2["CSType"] = 1m;
  newRecord2["CSSales01"] = 100m;
  newRecord2["CSSales02"] = 200m;
  newRecord2["CSSales03"] = 300m;
  newRecord2["CSSales04"] = 400m;
  newRecord2["CSSales05"] = 500m;
  newRecord2["CSSales06"] = 600m;
  newRecord2["CSSales07"] = 500m;
  newRecord2["CSSales08"] = 400m;
  newRecord2["CSSales09"] = 200m;
  newRecord2["CSSales10"] = 100m;
  newRecord2["CSSales11"] = 1m;
  newRecord2["CSSales12"] = 0m;

  myDS.AddPreparedRowAndSetActive(1);
  dbFile.SetFormat("RSalesMast");
  try
  {
      dbFile.AddRecord(myDS);
  }
  catch(dgException dgEx)
  {
      if (dgEx.Error != dgErrorNumber.dgEaDUPKEY)
          throw dgEx; /* If the 
            exception wasn't thrown due to a duplicate key, throw it again. */
      MessageBox.Show("Key " + 
            newRecord["CSName"].ToString() + " already in this file.", "Error");
  }

  dbFile.Close();
  db.Close();
```


### Example 10. SeekRange method example.

```cs 
  AdgConnection db = createAdgConnection("MyDatabaseName");
  FileAdapter dbFile = new FileAdapter(db, "*Libl/CSMASTERL1", "CSMASTERL1");
  dbFile.AccessMode = AccessMode.Read;
  AdgDataSet myDS = null;
  dbFile.OpenNewAdgDataSet(out myDS);

  /* The code below will find all of the sales for all 
   * customers with a number from 300 to 1400, 
   * and read all the customer numbers from lowest to highest. */
  AdgKeyTable key1 = myDS.NewKeyTable("RCSMASTL1");
  key1.Row["CSCUSTNO"] = Convert.ToDecimal(300);
  key1.KeyPartCount = 1;
  AdgKeyTable key2 = myDS.NewKeyTable("RCSMASTL1");
  key2.Row["CSCUSTNO"] = Convert.ToDecimal(1400);
  key2.KeyPartCount = 1;
  dbFile.SeekRange(RangeMode.First, key1, RangeFirst.Include, key2, RangeLast.Include);

  /* Read until we go past record 1421. */
  bool EOF = false;
  decimal Total = 0;
  while(!EOF)
  {
      try
      {
          dbFile.ReadSequential(myDS, ReadSequentialMode.Next, LockRequest.NoWait);
          for (int j=1; j &lt;= 12; j++)
          {
              string number = j.ToString();
              if (number.Length &lt; 2)
                  number = "0" + number;
              Total += Convert.ToDecimal(myDS.ActiveRow["CSSALES" + number]); 
          }
      }
      catch(dgException dgEx)
      {
          if (dgEx.Error == dgErrorNumber.dgEaEOF)
              EOF = true;
          else
          {
              throw dgEx; //Throw exception if we didn't expect it.
          }
      }
  }
  MessageBox.Show("Total sales for customers 300 to 1400 totalled " 
      + Total.ToString() + ".", "Result");

  dbFile.Close();
  db.Clone();
```


### Example 11. SeekKey method example.

```cs 
  AdgConnection db = createAdgConnection("MyDatabaseName");
  FileAdapter dbFile = new FileAdapter(db, "*Libl/CMASTNEWL1", "CMMASTERL1");
  dbFile.AccessMode = AccessMode.Read;
  AdgDataSet myDS = null;
  dbFile.OpenNewAdgDataSet(out myDS);

  /* Seek the file pointer to just before Customer number 1500. */
  AdgKeyTable key = myDS.NewKeyTable("RCMMASTL1");
  key.Row["CMCustNo"] = Convert.ToDecimal(1500);
  dbFile.SeekKey(SeekMode.SetLL, key);
  /* We read the next record to get customer number 1500.*/
  dbFile.ReadSequential(myDS, ReadSequentialMode.Next, LockRequest.Default);
  string CustomerName1 = myDS.ActiveRow["CMName"].ToString();

  /* We set the file pointer to just after customer number 2000. */
  key.Row["CMCustNo"] = Convert.ToDecimal(2000);
  dbFile.SeekKey(SeekMode.SetGT, key);
  /* We read backwards one record to get customer number 2000. */
  dbFile.ReadSequential(myDS, ReadSequentialMode.Previous, LockRequest.Default);
  string CustomerName2 = myDS.ActiveRow["CMName"].ToString();

  /* We set the file pointer to greater than or equal to 2979. */
  key.Row["CMCustNo"] = Convert.ToDecimal(2979);
  dbFile.SeekKey(SeekMode.SetGE, key);
  /* Record 2979 usually does not exist, so we should be on record
  * 3000, which we read by reading the current record (using
  * SeekMode.SetLL would have gotten us record 2900). */
  dbFile.ReadSequential(myDS, ReadSequentialMode.Next, LockRequest.Default);
  string CustomerName3 = myDS.ActiveRow["CMName"].ToString();

  /* We set the file pointer to greater than or equal to 4000. */
  key.Row["CMCustNo"] = Convert.ToDecimal(4000);
  dbFile.SeekKey(SeekMode.SetGE, key);
  /* Record 4000 does exist, and by reading the next record we should access it. */
  dbFile.ReadSequential(myDS, ReadSequentialMode.Next, LockRequest.Default);
  string CustomerName4 = myDS.ActiveRow["CMName"].ToString();

  dbFile.Close();
  db.Close();
```


### Example 12. FileAdaptor ResetFormat method example.


```cs 
AdgConnection db = createAdgConnection("MyDatabaseName");
FileAdapter dbFile = new FileAdapter(db, "Examples/SalesMem", "SalesMem");
dbFile.AccessMode = AccessMode.Read;
AdgDataSet myDS = null;
dbFile.OpenNewAdgDataSet(out myDS);

/* Here we find the name of the customer whose sales (not counting returns) were
 * the best on average in January from 1998 to 2004. This example assumes
 * there are no customer numbers in the second format which are not found in the
 * first format, and that there are no years on record past 1998 to 2004.
 * We use the ResetFormat method to read from both formats, and
 * this gives us the ability to easy see the next customer's name before we
 * read their records. */

decimal total = 0;
decimal currentAverage = 0;
string currentName = "";
decimal maxAverage = -1;
string maxName = "";

dbFile.ResetFormat(); /* Read from both formats automatically. */
/* Make sure we start off on format 0. */
do{
    dbFile.ReadSequential(myDS,ReadSequentialMode.Next, LockRequest.Read);
  }while(dbFile.CurrentFormatIndex != 0);
try /* Read until end of file. Throw exception again if it was not due to EOF. */
    {
    while(true) /* Hitting end of file will throw an exception and let us leave. */
    {
/* Remember, the ActiveRow changes depending on the current format. */
        currentName = myDS.ActiveRow["CMName"].ToString();
        total = 0;
        dbFile.ReadSequential(myDS, ReadSequentialMode.Next, LockRequest.Read);
        while (dbFile.CurrentFormatIndex == 1)
        {
            total += Convert.ToDecimal(myDS.ActiveRow["CSSales01"]);
            dbFile.ReadSequential(myDS, ReadSequentialMode.Next, LockRequest.Read);
        }
/* there could be as many as seven records from 1998 - 2004. */
        currentAverage = total / 7;
        if (currentAverage &gt; maxAverage)
        {
            maxName = currentName;
            maxAverage = currentAverage;
        }
    }
}
catch(dgException dgEx)
{
    if (dgEx.Error != dgErrorNumber.dgEaEOF)
        throw dgEx;
}
string decimalResult = maxAverage.ToString();
decimalResult = decimalResult.Substring(0, decimalResult.IndexOf('.') + 3);
MessageBox.Show("The cusomter with the highest average sales in " +
    "January from 1998 - 2004 is \"" + maxName +
     "\", with an average of " + decimalResult + ".",
     "Result");
dbFile.Close();
db.Close();
```


### Example 13. FileAdaptor ReleaseCurrent method example.

```cs 
 /* Here, we are using a pre-initialized FileAdapter (named "dbFile")
  * which was opened using AccessMode.RWCD, which automatically locks
  * each read record read, so it will remain unchanged until we
  * update it or read a new record. Here we don't want to
  * update the record if the customer is not from Texas, and if
  * this code is being called by unknown client code it could be awhile
  * before the next read. In order to remove the lock without
  * performing some additional action, we use the ReleaseCurrent method . */
 dbFile.ReadSequential(myDS, ReadSequentialMode.Next, LockRequest.Default);
 if (myDS.ActiveRow["CMState"].ToString() == "TX" &amp;&amp;
     myDS.ActiveRow["CMActive"].ToString() == "0")
 {
     myDS.ActiveRow["CMActive"] = '1';
     dbFile.ChangeCurrent(myDS);
 }
 else
 {
     dbFile.ReleaseCurrent();
 }

```

### Example 14. FileAdaptor RecordCount property usage example.

```cs 
  AdgConnection db = createAdgConnection("MyDatabaseName");
  FileAdapter dbFile = new FileAdapter(db, "*Libl/CMASTNEWL1", "CMMASTERL1");
  dbFile.AccessMode = AccessMode.Read;
  AdgDataSet myDS = null;

  int refreshInterval = 10; //Used so we don't slow down refreshing too much...
  dbFile.OpenAttributes.BlockingFactor = refreshInterval;
  dbFile.OpenNewAdgDataSet(out myDS);

  /* Here, we read every record until end of file is reached.
   * Because this is an fairly long process, we set up a progress bar
   * to keep the user from being discouraged. We set its Maximum
   * value to the number of records in the file, which is found
   * using FileAdapter's RecordCount propert, divided by
   * our refreshInterval. */
  int recordsReadSinceLastRefresh = 0;
  prgBar.Minimum = 0;
  prgBar.Maximum = Convert.ToInt32(dbFile.RecordCount) / refreshInterval;

  bool EOF = false;
  while(!EOF)
  {
      try
      {
          /* Though it seems like we have to read each record one at a time,
           * in reality DG stores the first 10 records the first time we read
           * and then afterwards we simply read from the cache. When those run out, 
           * DG will automatically grab another ten records from the database.
           * Note that 10 is our refresh interval, meaning that this I/O operation
           * occurs at the same time that we update our progress bar. If the blocking
           * factor was higher than our refresh interval, not only would we have to 
           * wait longer to read the first record but the progress bar would go longer
           * without being updated. */
          dbFile.ReadSequential(myDS, ReadSequentialMode.Next, LockRequest.NoWait);
          /* Perform some action on each record here... */
          recordsReadSinceLastRefresh ++;
          if (recordsReadSinceLastRefresh == refreshInterval)
          {
              recordsReadSinceLastRefresh = 0;
              prgBar.PerformStep();
              this.Refresh(); //Refreshes the form.
          }
      }
      catch(dgException dgEx)
      {
          if (dgEx.Error == dgErrorNumber.dgEaEOF)
              EOF = true;
          else
          {
              //Exit procedure or end application here.
          }
      }
  }
  dbFile.Close();
  db.Close();
```


### Example 15. ReadSequential FileAdaptor method example.

```cs 
   AdgConnection db = createAdgConnection("MyDatabaseName");
   FileAdapter dbFile = new FileAdapter(db, "*Libl/CMASTNEWL1",
           "CMMASTERL1");
   dbFile.AccessMode = AccessMode.Read;
   AdgDataSet myDS = null;
   dbFile.OpenNewAdgDataSet(out myDS);

   /* Read the first record (in terms of Customer number, which CMASTNEWL1 is
    * keyed by.) */
   dbFile.ReadSequential(myDS, ReadSequentialMode.First, LockRequest.Default);
   string FirstCustomerName = myDS.ActiveRow["CMCustNo"].ToString();

   /* Seek the file pointer to just before Customer number 1500. */
   AdgKeyTable key = myDS.NewKeyTable("RCMMastL1");
   key.Row["CMCustNo"] = Convert.ToDecimal(1500);
   dbFile.SeekKey(SeekMode.SetLL, key);
   /* We read the next record to get customer number 1500.*/
   dbFile.ReadSequential(myDS, ReadSequentialMode.Next, LockRequest.Default);
   string OneThousandFiveHundrethCustomerName =
           myDS.ActiveRow["CMName"].ToString();
```


### Example 16. ReadSequentialEqual FileAdaptor method example.

```cs 
  AdgConnection db = createAdgConnection("MyDatabaseName");
  FileAdapter dbFile = new FileAdapter(db, "*Libl/CSMASTERL1", "CSMASTERL1");
  dbFile.AccessMode = AccessMode.Read;
  AdgDataSet myDS = null;
  dbFile.OpenNewAdgDataSet(out myDS);

  /* We read all of the records for customer 300 in order to get 
   * their net sales as well as their average yearly gross sales
   * and returns. */
  AdgKeyTable custNoKey = myDS.NewKeyTable("RCSMastL1");
  custNoKey.Row["CSCustNo"] = Convert.ToDecimal(300);
  custNoKey.KeyPartCount = 1; //Only use the first field of the key.
  decimal totalSales = 0;
  decimal totalReturns = 0;
  int saleRecordsRead = 0;
  int returnRecordsRead = 0;
  bool EOF = false;
  /* Because ReadSequentialEqual will return EOF if the record
   * it immediately gets is not equal to its search key, we need
   * to first seek to an equal record. */ 
  dbFile.SeekKey(SeekMode.SetLL, custNoKey);
  while(!EOF){
      try{
          dbFile.ReadSequentialEqual(myDS, ReadEqualMode.NextEqual, LockRequest.Read, custNoKey);
          if (Convert.ToDecimal(myDS.ActiveRow["CSType"]) == 1)
          {
              totalSales += Convert.ToDecimal(myDS.ActiveRow["CSSales01"]) + 
                  Convert.ToDecimal(myDS.ActiveRow["CSSales02"]) +
                  Convert.ToDecimal(myDS.ActiveRow["CSSales03"]) + 
                  Convert.ToDecimal(myDS.ActiveRow["CSSales04"]) +
                  Convert.ToDecimal(myDS.ActiveRow["CSSales05"]) + 
                  Convert.ToDecimal(myDS.ActiveRow["CSSales06"]) +
                  Convert.ToDecimal(myDS.ActiveRow["CSSales07"]) + 
                  Convert.ToDecimal(myDS.ActiveRow["CSSales08"]) +
                  Convert.ToDecimal(myDS.ActiveRow["CSSales09"]) + 
                  Convert.ToDecimal(myDS.ActiveRow["CSSales10"]) +
                  Convert.ToDecimal(myDS.ActiveRow["CSSales11"]) + 
                  Convert.ToDecimal(myDS.ActiveRow["CSSales12"]);
              saleRecordsRead ++;
          }
          else
          {
              totalReturns -= Convert.ToDecimal(myDS.ActiveRow["CSSales01"]) + 
                  Convert.ToDecimal(myDS.ActiveRow["CSSales02"]) +
                  Convert.ToDecimal(myDS.ActiveRow["CSSales03"]) + 
                  Convert.ToDecimal(myDS.ActiveRow["CSSales04"]) +
                  Convert.ToDecimal(myDS.ActiveRow["CSSales05"]) + 
                  Convert.ToDecimal(myDS.ActiveRow["CSSales06"]) +
                  Convert.ToDecimal(myDS.ActiveRow["CSSales07"]) + 
                  Convert.ToDecimal(myDS.ActiveRow["CSSales08"]) +
                  Convert.ToDecimal(myDS.ActiveRow["CSSales09"]) + 
                  Convert.ToDecimal(myDS.ActiveRow["CSSales10"]) +
                  Convert.ToDecimal(myDS.ActiveRow["CSSales11"]) + 
                  Convert.ToDecimal(myDS.ActiveRow["CSSales12"]);
              returnRecordsRead ++;
          }
      }
      catch(dgException dgEx){
          if (dgEx.Error == dgErrorNumber.dgEaEOF)
          {
              EOF = true;
          }
          else
          {
              MessageBox.Show("Error getting next record for customer 300:" + 
                  dgEx.Message, "Error");
              //Exit procedure or end application here.
          }
      }
  }
  /* Compute additional results. */
  decimal netSales = totalSales - totalReturns;
  decimal averageSalesPerYear;
  if (saleRecordsRead &gt; 0)
      averageSalesPerYear = totalSales / saleRecordsRead;
  else
      averageSalesPerYear = 0;
  decimal averageReturnsPerYear;
  if (returnRecordsRead &gt; 0)
      averageReturnsPerYear = totalReturns / returnRecordsRead;
  else
      averageReturnsPerYear = 0;
  dbFile.Close();
  db.Close();

```

### Example 17. ReadRange FileAdaptor method example.

```cs 
  AdgConnection db = createAdgConnection("MyDatabaseName");
  FileAdapter dbFile = new FileAdapter(db, "*Libl/CMASTNEWL1", 
            "CMMASTERL1");
  dbFile.AccessMode = AccessMode.Read;

  AdgDataSet myDS = null;
  try
  {
      dbFile.OpenNewAdgDataSet(out myDS);
  }
  catch(dgException dgEx)
  {
      MessageBox.Show("Error opening file! " + 
            dgEx.Message, "Error");
      //Exit procedure or end application here.
  }

  /* We read all records with a customer number greater
   * than, but not equal to 10000 and less than or equal
   * to, 40000. */
  AdgKeyTable OneKey = myDS.NewKeyTable("RCMMastL1");
  OneKey.Row["CMCustNo"] = 10000;
  AdgKeyTable TwoKey = myDS.NewKeyTable("RCMMastL1");
  TwoKey.Row["CMCustNo"] = 40000;

  try
  {
      dbFile.ReadRange(myDS, RangeMode.First,
      LockRequest.Read, OneKey,
      RangeFirst.Exclude, TwoKey,
      RangeLast.Include);
  }
  catch(dgException dgEx)
  {
      MessageBox.Show("Error getting records 
            10000-40000 :" +
          dgEx.Message, "Error");
      //Exit procedure or end application here.
  }

  int totalSum = 0;
  int activeSum = 0;
  bool EOF = false;
  while(!EOF)
  {
      try
      {

            dbFile.ReadSequential(myDS, ReadSequentialMode.Next, 
            LockRequest.NoWait);
          if (Convert.ToChar(myDS.ActiveRow["CMActive"]).ToString() 
            == "1")
          activeSum ++;
          totalSum ++;
      }
      catch(dgException dgEx)
      {
          if (dgEx.Error == 
            dgErrorNumber.dgEaEOF)

            EOF = true;
          else
          {
 
            //Exit procedure or end application here.
          }
      }
  }

  string percent = Convert.ToDecimal((Convert.ToDecimal(activeSum)
      /Convert.ToDecimal(totalSum)) * 100).ToString();
  MessageBox.Show(percent.Substring(0, percent.IndexOf('.')) +
      "% of the customers sampled are active.");
  dbFile.Close();
  db.Close(); 
```


### Example 18. ReadRandomKey FileAdaptor method example.

```cs 
  AdgConnection db = createAdgConnection("MyDatabaseName");
  FileAdapter dbFile = new FileAdapter(db, "*Libl/CMASTNEWL1", "CMMASTERL1");
  dbFile.AccessMode = AccessMode.Read;
  AdgDataSet myDS = null;
  dbFile.OpenNewAdgDataSet(out myDS);
  /* We retrieve the record for customer number 92300. */
  AdgKeyTable keyTbl = myDS.NewKeyTable("RCMMASTL2");
  keyTbl.Row["CMCUSTNO"] = 92300;
  try
  {
      dbFile.ReadRandomKey(myDS, ReadRandomMode.Equal, LockRequest.Default, keyTbl);
  }
  catch(dgException dgEx)
  {
      MessageBox.Show("Error finding the record: " + dgEx.Message,
          dgEx.Error.ToString());
  }

  dbFile.Close();
  db.Close();
```


### Example 19. OpenSimpleQuery FileAdaptor method example.

```cs 
  AdgConnection db = createAdgConnection("MyDatabaseName");
  FileAdapter dbFile = new FileAdapter(db, "*Libl/CMASTNEWL1", "CMMASTERL1");
  dbFile.AccessMode = AccessMode.Read; 
  AdgDataSet myDS = null;

  string[] keys = new string[]{"CMCUSTNO"};
  KeyUsages[] usages = new KeyUsages[]{KeyUsages.ASCEND};

  /* Read the first customer name listed for Texas. */
  dbFile.OpenSimpleQuery(ref myDS, "*UNIQUE", "CMSTATE=\"TX\"", keys, usages);
  dbFile.ReadSequential(myDS, ReadSequentialMode.First, LockRequest.Read);
  string FirstInTexas = myDS.ActiveRow["CMName"].ToString();
  /* First close the file to avoid throwing an exception... */
  dbFile.Close();
  /* Read the first customer name listed in Tennessee. */ 
  dbFile.OpenSimpleQuery(ref myDS, "*UNIQUE", "CMSTATE=\"TN\"", keys, usages);
  dbFile.ReadSequential(myDS, ReadSequentialMode.First, LockRequest.Read);
  string FirstInTennessee = myDS.ActiveRow["CMName"].ToString();

  dbFile.Close();
  db.Close();

```

### Example 20. OpenNewAdgDataSet FileAdaptor method example.

```cs 
  AdgConnection db = createAdgConnection("MyDatabaseName");
  FileAdapter dbFile = new FileAdapter(db, "*Libl/CMASTNEWL1", "CMMASTERL1");
  dbFile.AccessMode = AccessMode.Read;

  /* The AdgDataSet consists of data read from the database file
   * using the FileAdapter class. It also must be used in most
   * of the FileAdapter's operations. */
  AdgDataSet myDS = null;
  try
  {
      dbFile.OpenNewAdgDataSet(out myDS);
  }
  catch(dgException dgEx)
  {
      /* There are many reasons why opening a file can fail. Here, we
       * catch some of the more general ones. */
      if (dgEx.Error == dgErrorNumber.dgEmMNOTFND)
          MessageBox.Show("Member " + dbFile.MemberName + " not found!", "Error opening file");
      else if (dgEx.Error == dgErrorNumber.dgEmFNOTFND)
          MessageBox.Show("File " + dbFile.FileName + " not found!", "Error opening file");
      else
          MessageBox.Show(dgEx.Message, "Error opening file");
      //Exit procedure here.
  }

  /* The code below finds the names of every data field in the 
   * file "*Libl/CMASTNEWL1" and puts them into an array list. */
  ArrayList fieldNames = new ArrayList();

  for (int i = 0; i &lt; myDS.Formats; i ++)
  {
      foreach(DataColumn column in myDS.Tables[i].Columns)
      {
          fieldNames.Add(column.ToString());
      }
  } 

  dbFile.Close();
  db.Close();
```

### Example 20. Open FileAdaptor method example.

```cs 
  /* Unlike OpenNewAdgDataSet, the Open method does not create
   * a new AdgDataSet to meet the requirements of the file being
   * opened. However, it is slightly faster because of this, so
   * Open is a preferable way to open a file if a suitable.
   * AdgDataSet already exists or you don't need one. 
   * Note, however, that opening a file is a relatively slow
   * operation and the need to reopen a file rarely occurs. */

  FileAdapter dbFile = new FileAdapter();
  dbFile.SetConnection( createAdgConnection("MyDatabaseName") );
  dbFile.FileName = "*Libl/CMASTNEW";
  dbFile.MemberName = "CMMASTER";
  AdgDataSet myDS = null;

  /* Only need to open the file to show the number of records,
   * then we're through with it. */
  dbFile.Open(myDS); /* Will not initialize the data set. */

  MessageBox.Show("Number of deleted and non-deleted records still " +
      "taking up space in file \"" + dbFile.FileName +
      "\" is " + dbFile.FileLength.ToString());
  dbFile.Close();
  dbFile.Connection.Close();

```

### Example 21. OpenAttributes property example.

```cs 
  AdgConnection db = createAdgConnection("MyDatabaseName");
  FileAdapter dbFile = new FileAdapter(db, "*Libl/CMASTNEWL1", "CMMASTERL1");
  dbFile.AccessMode = AccessMode.Read;
  AdgDataSet myDS = null;

  int refreshInterval = 10; //Used so we don't slow down refreshing too much...
  dbFile.OpenAttributes.BlockingFactor = refreshInterval;
  dbFile.OpenNewAdgDataSet(out myDS);

  /* Here, we read every record until end of file is reached.
   * Because this is an fairly long process, we set up a progress bar
   * to keep the user from being discouraged. We set its Maximum
   * value to the number of records in the file, which is found
   * using FileAdapter's RecordCount property, divided by
   * our refreshInterval. */
  int recordsReadSinceLastRefresh = 0;
  prgBar.Minimum = 0;
  prgBar.Maximum = Convert.ToInt32(dbFile.RecordCount) / refreshInterval;

  bool EOF = false;
  while(!EOF)
  { 
      try
      {
          /* Though it seems like we have to read each record one at a time,
           * in reality DG stores the first 10 records the first time we read
           * and then afterwards we simply read from the cache. When those run out, 
           * DG will automatically grab another ten records from the database.
           * Note that 10 is our refresh interval, meaning that this I/O operation
           * occurs at the same time that we update our progress bar. If the blocking
           * factor was higher than our refresh interval, not only would we have to 
           * wait longer to read the first record but the progress bar would go longer
           * without being updated. */
          dbFile.ReadSequential(myDS, ReadSequentialMode.Next, LockRequest.NoWait);
          /* Perform some action on each record here... */
          recordsReadSinceLastRefresh ++;
          if (recordsReadSinceLastRefresh == refreshInterval)
          {
              recordsReadSinceLastRefresh = 0;
              prgBar.PerformStep();
              this.Refresh(); //Refreshes the form.
          }
      }
      catch(dgException dgEx)
      {
          if (dgEx.Error == dgErrorNumber.dgEaEOF)
              EOF = true;
          else
          {
              //Exit procedure or end application here.
          }
      }
  }
  dbFile.Close();
  db.Close();
```

### Example 21. MemberName property example.

```cs 
  /* We attempt to open the class variable FileAdapter "dbFile" 
   * which may or may not have been initialized another routine. */
  public void OpenFile(){
      AdgDataSet myDS = null;
      if (dbFile == null)
      {
          MessageBox.Show("FileAdapter not initialized.");
          return;
      }
      try
      {
          dbFile.OpenNewAdgDataSet(out myDS);
      }
      catch(dgException dgEx)
      {
          if (dgEx.Error == dgErrorNumber.dgEmMNOTFND)
          {
              MessageBox.Show("Member " + dbFile.MemberName + " not found!");
          }
          else if (dgEx.Error == dgErrorNumber.dgEmFNOTFND)
          {
              MessageBox.Show("File " + dbFile.FileName + " not found!");
          }
          else 
          {
              MessageBox.Show("Couldn't open file!" + dgEx.Message, "");
          } 
          // Exit routine or end application here.
      }
  }
 
```


### Example 23. GetPrintProperties method example.


```cs 
  /* Will open up "CustReport" and will write a single detail, and
   * change its background color. */
  AdgConnection dataBase = createAdgConnection("MyDatabaseName");
  FileAdapter printFile = new FileAdapter(dataBase, "*Libl/CustReport", "*First");
  printFile.AccessMode = AccessMode.PrintPreview;
  AdgDataSet dataSet;
  printFile.OpenNewAdgDataSet(out dataSet);

  DataRow dr = dataSet.PrepareRow("rptDetail");
  dr["prtCMName"] = "This line is light blue.";

  IPrintProperties ip = printFile.GetPrintProperties("rptDetail");
  int oleColor = ColorTranslator.ToOle(Color.LightBlue);
  ip.SetValue("lblRowColor", "BackColor", oleColor);

  dataSet.AddRow("rptDetail");
  printFile.SetFormat("rptDetail");
  printFile.AddRecord(dataSet);

  printFile.Close(); /* Shows print preview - can also accomplish this with
                      * ForceEOD, which doesn't close the file. */
  dataBase.Close();
```

### Example 24. FileAdapter FileName property example.

```cs 
  /* In this simple routine we wish to write the format names 
   * of a file to a combo box using the FileAdapter "dbFile" 
   * and its accompanying AdgDataSet "myDS", which may or 
   * may not have been initialized and opened elsewhere. */
  if (dbFile == null)
  {
      MessageBox.Show("Error- FileAdapter not initialized.");
      return;
  }
  if (dbFile.Status != FileAdapter.AdapterStatus.Open)
  {
      MessageBox.Show("Error- "+ dbFile.FileName + " not open.");
      return;
  }
  if (myDS == null)
  {
      MessageBox.Show("DataSet not initialized!");
      return;
  }

  for (int i = 0; i &lt; myDS.Formats; i ++)
  {
      /* List the format names in the combo box "cbFmtNames". */
      cbFmtNames.Items.Add(myDS.GetFormatName(i));
  }

```


### Example 24. FileAdapter FileLength property example.

```cs 
  FileAdapter dbFile = new FileAdapter();
  dbFile.SetConnection( createAdgConnection("MyDatabaseName") );
  dbFile.FileName = "*Libl/CMASTNEW";
  dbFile.MemberName = "CMMASTER";
  AdgDataSet myDS = null;
  dbFile.Open(myDS); /* Will not initialize the data set. */

  /* Figure out the number of records which were logically 
   * deleted but are still taking up space on the physical file.
   * FileLength returns the number of deleted and non-deleted 
   * records stored on a physical file, while RecordCount returns
   * the number of non-deleted records only. */
  long deletedRecords = dbFile.FileLength - dbFile.RecordCount;
  MessageBox.Show("Number of deleted records still taking up space in file \"" 
      + dbFile.FileName + "\" is " + deletedRecords.ToString());
  dbFile.Close();
  dbFile.Connection.Close();
```

### Example 25. Specifying FileName and MemberName properties after FileAdapter gets instanced.

```cs 
  AdgConnection dataBase = createAdgConnection("MyDatabaseName");
  FileAdapter dbFile = new FileAdapter(dataBase);
  dbFile.FileName = "*Libl/CMASTNEWL1";
  dbFile.MemberName = "CMMASTERL1";
```

### Example 25. Specifying Connection property after FileAdapter gets instanced.

```cs 
  AdgConnection dataBase = createAdgConnection("MyDatabaseName");
  FileAdapter dbFile = new FileAdapter();
  dbFile.SetConnection( dataBase;
  dbFile.FileName = "*Libl/CMASTNEWL1";
  dbFile.MemberName = "CMMASTERL1";
```

### Example 26. FileAdapter.ExactSeek Property usage example.

```cs 
  AdgConnection db = createAdgConnection("MyDatabaseName");
  using (FileAdapter dbFile = new FileAdapter(db, "*Libl/CMASTNEWL1", "CMMASTERL1"))
  {
      dbFile.AccessMode = AccessMode.Read;
      AdgDataSet myDS = null;
      dbFile.OpenNewAdgDataSet(out myDS);

      /* Seek the file pointer to just before Customer number 3000. */
      AdgKeyTable key = myDS.NewKeyTable("RCMMastL1");
      key.Row["CMCustNo"] = Convert.ToDecimal(3000);
      dbFile.SeekKey(SeekMode.SetGE, key);
      /* We check to see if we matched 3000 or if we went beyond it. */
      if (dbFile.ExactSeek)
          MessageBox.Show("Record 3000 exists.");
      else
          MessageBox.Show("Record 3000 not found.");
      /* Now we try to find Customer number 1125. */
      key.Row["CMCustNo"] = Convert.ToDecimal(1125);
      dbFile.SeekKey(SeekMode.SetGE, key);
      if (dbFile.ExactSeek)
          MessageBox.Show("Record 1125 exists.");
      else
          MessageBox.Show("Record 1125 not found.");
  }//Using statement automatically closes dbFile.
  db.Close();
```

### Example 26. DeleteRange method example.

```cs 
  AdgConnection db = createAdgConnection("MyDatabaseName");
  FileAdapter dbFile = new FileAdapter(db, "*Libl/CMASTNEWL1", "CMMASTERL1");
  dbFile.AccessMode = AccessMode.Delete | AccessMode.Read;

  AdgDataSet myDS = null;
  try
  {
      dbFile.OpenNewAdgDataSet(out myDS);
  }
  catch(dgException dgEx)
  {
      MessageBox.Show("Error opening file! " + dgEx.Message, "Error");
      //Exit procedure or end application here.
  }

  /* We erase all records with a customer number equal to
   * or greater than 5000 and less than, but not
   * equal to, 6000. */
  AdgKeyTable OneKey = myDS.NewKeyTable("RCMMastL1");
  OneKey.Row["CMCustNo"] = 5000;
  AdgKeyTable TwoKey = myDS.NewKeyTable("RCMMastL1");
  TwoKey.Row["CMCustNo"] = 6000;
  try
  {
      dbFile.DeleteRange(OneKey, RangeFirst.Include, TwoKey, RangeLast.Exclude);
  }
  catch(dgException dgEx)
  {
      MessageBox.Show("Error deleting records 5000-6000 :" +
          dgEx.Message, "Error");
  }

  dbFile.Close();
  db.Close();
```

### Example 27. DeleteKey method example.

```cs 
  AdgConnection db = createAdgConnection("MyDatabaseName");
  FileAdapter dbFile = new FileAdapter(db, "*Libl/CMASTNEWL1", "CMMASTERL1");
  /* Open a file for reading and deleting- this allows us to delete a record by its key value. */
  dbFile.AccessMode = AccessMode.Delete | AccessMode.Read;

  AdgDataSet myDS = null;
  try
  {
      dbFile.OpenNewAdgDataSet(out myDS);
  }
  catch(dgException dgEx)
  {
      MessageBox.Show("Error opening file! " + dgEx.Message, "Error");
      //Exit procedure or end application here.
  }

  /* We retrieve the record for customer number 82900 and delete it! */
  AdgKeyTable keyTbl = myDS.NewKeyTable("RCMMASTL1");
  keyTbl.Row["CMCustNo"] = 82900;
  dbFile.DeleteKey(keyTbl);

  dbFile.Close();
  db.Close();
```

### Example 28. DeleteCurrent method example.

```cs 
  AdgConnection db = createAdgConnection("MyDatabaseName");
  FileAdapter dbFile = new FileAdapter(db, "*Libl/CMASTNEWL1", "CMMASTERL1");
  dbFile.AccessMode = AccessMode.Read | AccessMode.Delete;

  AdgDataSet myDS = null;
  try
  {
      dbFile.OpenNewAdgDataSet(out myDS);
  }
  catch(dgException dgEx)
  {
      MessageBox.Show("Error opening file! " + dgEx.Message, "Error");
      //Exit procedure or end application here.
  }

  dbFile.ReadSequential(myDS, ReadSequentialMode.First, LockRequest.Default);

  /* We retrieve the record for customer number 7800... */
  AdgKeyTable keyTbl = myDS.NewKeyTable("RCMMASTL1");
  keyTbl.Row["CMCUSTNO"] = 7800;
  try
  {
      dbFile.ReadRandomKey(myDS, ReadRandomMode.Equal, LockRequest.Default, keyTbl);
      /*... and delete it! */
      dbFile.DeleteCurrent();
  }
  catch(dgException dgEx)
  {
      MessageBox.Show("Error deleting the record: " + dgEx.Message,
      dgEx.Error.ToString());
  }

  dbFile.Close();
  db.Close();
```

### Example 29. DeleteAllRecords method example.

```cs 
  /* We open the file in order to delete all of its records. */
  AdgConnection db = createAdgConnection("MyDatabaseName");
  FileAdapter dbFile = new FileAdapter(db, "*Libl/CMASTNEW", "CMMASTER");
  dbFile.AccessMode = AccessMode.Delete;
  /* Its generally good practice to make sure you have an exclusive lock
   * on a file that you are deleting all of the records from, but some
   * databases do not require it. */
  dbFile.OpenAttributes.ShareTypes = ShareTypes.Exclusive;
  AdgDataSet myDS = null;

  try
  {
      dbFile.Open(myDS);
  }
  catch(dgException dgEx)
  {
      db.Close();
      if (dgEx.Error == dgErrorNumber.dgEmBUSYOBJ)
      {
          MessageBox.Show("Couldn't open the file for exclusive access.", "Error opening file.");
          //Exit routine or procedure here to avoid preceding file operations.
      }
      else 
          throw dgEx;
  }
  dbFile.DeleteAllRecords();
  
  dbFile.Close();
  db.Close();
```

### Example 30. Connection property example.

```cs 
  /* Initialize a new fileadapter. Since the AdgConnection is needed
   * only for this file adapter, it is created and destroyed using the
   * FileAdapter's Connection property. */
  FileAdapter dbFile = new FileAdapter();
  dbFile.SetConnection( createAdgConnection("MyDatabaseName") );
  dbFile.FileName = "*Libl/CMASTNEWL2";
  dbFile.MemberName = "CMMASTERL2";
  dbFile.AccessMode = AccessMode.Read;

  AdgDataSet myDS = null;
  dbFile.OpenNewAdgDataSet(out myDS);

  /* Find first record beginning with M. */
  AdgKeyTable keyTbl = myDS.NewKeyTable("RCMMASTL2");
  keyTbl.Row["CMName"] = "M";
  dbFile.SeekKey(SeekMode.SetLL, keyTbl);

  dbFile.ReadSequential(myDS, ReadSequentialMode.Next, LockRequest.Read);
  string firstMCustomer = myDS.ActiveRow["CMName"].ToString();

  dbFile.Close(); /* Close file. */
  dbFile.Connection.Close(); /* Close database. */
```

### Example 31. Close method example.

```cs 
  AdgConnection db = createAdgConnection("MyDatabaseName");
  FileAdapter dbFile = new FileAdapter(db, "*Libl/CMASTNEWL1", "CMMASTERL1");
  dbFile.AccessMode = AccessMode.Read;
  AdgDataSet myDS = null;

  /* Though all open files will automatically be closed when a process
   * is terminated, it is good practice to close them as soon as you are
   * finished with them. You also may need to close a file in order
   * to reopen it with different attributes or to open it as a query file. */

  /* Read the first customer name listed for Texas. */
  string[] keys = new string[]{"CMCUSTNO"}; //The key fields used in our query.
  KeyUsages[] usages = new KeyUsages[]{KeyUsages.ASCEND}; //How we use them.

  dbFile.OpenSimpleQuery(ref myDS, "*UNIQUE", "CMSTATE=\"TX\"", keys, usages);
  dbFile.ReadSequential(myDS, ReadSequentialMode.First, LockRequest.Read);
  string FirstInTexas = myDS.ActiveRow["CMName"].ToString();

  /* Going to try a new query- first we close the file to avoid 
   * throwing an exception... */
  dbFile.Close();
  /* Read the first customer name listed in Tennessee. */ 
  dbFile.OpenSimpleQuery(ref myDS, "*UNIQUE", "CMSTATE=\"TN\"", keys, usages);
  dbFile.ReadSequential(myDS, ReadSequentialMode.First, LockRequest.Read);
  string FirstInTennessee = myDS.ActiveRow["CMName"].ToString();

  dbFile.Close();
  db.Close();
```

### Example 32. ChangeCurrent method example.

```cs 
  AdgConnection db = createAdgConnection("MyDatabaseName");
  FileAdapter dbFile = new FileAdapter(db, "*Libl/CMASTNEWL1", "CMMASTERL1");
  dbFile.AccessMode = AccessMode.Read | AccessMode.Change;

  AdgDataSet myDS = null;
  try
  {
      dbFile.OpenNewAdgDataSet(out myDS);
  }
  catch(dgException dgEx)
  {
      MessageBox.Show("Error opening file! " + dgEx.Message, "Error");
      //Exit procedure or end application here.
  }
  /* We read the first record of the file... */
  dbFile.ReadSequential(myDS, ReadSequentialMode.First, LockRequest.Default);
  myDS.SetActive(myDS.GetFormatName(0), 0); 
  /* ...and make the customer name all caps. */
  string CustName = System.Convert.ToString(myDS.ActiveRow["CMName"]);
  CustName = CustName.ToUpper();
  myDS.ActiveRow["CMName"] = CustName;
  try
  {
      /* Here we update the record. */
      dbFile.ChangeCurrent(myDS);
  }
  catch (dgException dgEx)
  {
      MessageBox.Show("Error updating record: " + dgEx.Message, "Error.");
      // Exit routine or take alternative action here.
      test.Actual = "Catch occured.";
  }

  dbFile.Close();
  db.Close();
```

### Example 33. AddRecord method example.

```cs 
  AdgConnection db = createAdgConnection("MyDatabaseName");
  FileAdapter dbFile = new FileAdapter(db, "*Libl/CMASTNEWL1", 
            "CMMASTERL1");
  dbFile.AccessMode = AccessMode.RWCD;

  AdgDataSet myDS = null;
  try
  {
     db.Open();
     dbFile.OpenNewAdgDataSet(out myDS);
  }
  catch(dgException dgEx)
  {
     MessageBox.Show("Error opening file! " + dgEx.Message, 
            "Error");
     //Exit procedure or end application here.
  }

  DataRow newRow = myDS.PrepareRow(0);
  newRow["CMCustNo"] = 50;
  newRow["CMName"] = "Amalgamated Software of North America";
  newRow["CMAddr1"] = "IH-10 West";
  newRow["CMCity"] = "San Antonio";
  newRow["CMState"] = "TX";
  newRow["CMCntry"] = "US";
  newRow["CMPostCode"] = "78230";
  newRow["CMActive"] = "1";
  newRow["CMFax"] = "2105554679";
  newRow["CMPhone"] = "555-4678";
  myDS.AddPreparedRowAndSetActive(0);
  try
  {
     dbFile.AddRecord(myDS);
  }
  catch (dgException dgEx)
  {
     MessageBox.Show("Adding new record was unsuccessful! "
        + dgEx.Message, "Error!");
     //Exit procedure or end application here.
  }
```

### Example 34. FileAdapter AccessMode property example.

```cs 
  FileAdapter dbFile = new FileAdapter();
  dbFile.SetConnection( createAdgConnection("MyDatabaseName") );
  dbFile.FileName = "*Libl/CMASTNEWL1";
  dbFile.MemberName = "CMMASTERL1";

  /* Open a file for reading and deleting- this allows us to delete a record by its key value. */
  dbFile.AccessMode = AccessMode.Read | AccessMode.Delete;
  AdgDataSet myDS = null;
  dbFile.OpenNewAdgDataSet(out myDS);

  /* We retrieve the record for customer number 82900 and delete it! */
  AdgKeyTable keyTbl = myDS.NewKeyTable("RCMMASTL1");
  keyTbl.Row["CMCustNo"] = 82900m;
  try
  {
      dbFile.DeleteKey(keyTbl);
  }
  catch(dgException dgEx)
  {
      if (dgEx.Error == dgErrorNumber.dgEaNOTFND)
      {
          MessageBox.Show("Record not found. ");
      }
  }
  dbFile.Close();
  dbFile.Connection.Close();
```

