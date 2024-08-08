---
title: "IFileObject interface         | QSYS API Reference Guide"
description: "Defines the contract for managing a file in the ASNA DataGate client. "
last_modified_at: 2024-08-08T21:41:32Z
---

Defines the contract for managing a file in the ASNA DataGate client.

**Namespace:** ASNA.DataGate.Client
**Assembly:** ASNA.QSys.DataGate.Client.dll

**Extends:** [IAdgObject](/reference/datagate/datagate-client/i-adg-object.html), [IComparable](https://learn.microsoft.com/en-us/dotnet/api/system.icomparable-1?view=net-8.0), [IConnectionHandler](/reference/datagate/datagate-client/i-connection-handler.html), [IDisposable](https://learn.microsoft.com/en-us/dotnet/api/system.idisposable?view=net-8.0)
<br>
<br>
In DG implementations of **IFileObject** , instance members are not guaranteed to be thread safe.

## Remarks
This interface provides properties and methods to manage a file in the ASNA DataGate client. 
It includes properties to get the number of members in the file, the members of the file, 
the XML documents that define the file and its creation attributes, 
and various other properties related to the file. It also provides methods to copy the file, 
copy data from the file to a new file or from an import file to the file, 
read and write the definition and creation attributes of the file, 
get the AdgDataSet of the file, inspect the file, and repair the file.

<br>
<br>

## Properties

| Type | Name | Description
| --- | --- | --- 
| [XmlDocument](https://learn.microsoft.com/en-us/dotnet/api/system.xml.xmldocument?view=net-8.0) | CreationAttributes | Gets or sets the XML document that defines the creation attributes of the file. |
| [XmlDocument](https://learn.microsoft.com/en-us/dotnet/api/system.xml.xmldocument?view=net-8.0) | Definition | Gets or sets the XML document that defines the file. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | FileWaitTime | Gets the file wait time in milliseconds. |
| [IReadOnlyDictionary\<String, String\>](https://learn.microsoft.com/en-us/dotnet/api/system.collections.generic.ireadonlydictionary-2?view=net-8.0) | FormatIdentifiers | Provides access to the file's format names and format identifiers. |
| [Hashtable](https://learn.microsoft.com/en-us/dotnet/api/system.collections.hashtable?view=net-8.0) | FormatIDs | Gets the format IDs of the file. This property is obsolete, use 'FormatIdentifiers' instead. |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | HasKeys | Gets a value indicating whether the file has keys. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | MemberCount | Gets the number of members in the file. |
| [IEnumerable\<IMember\>](https://learn.microsoft.com/en-us/dotnet/api/system.collections.generic.ienumerable-1?view=net-8.0) | MemberObjects | Gets the members of the file. |
| [XmlDocument](https://learn.microsoft.com/en-us/dotnet/api/system.xml.xmldocument?view=net-8.0) | PrintCreationAttributes | Gets or sets the XML document that defines the print creation attributes of the file. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | RecordLength | Gets the length of a record in the file. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | RecordWaitTime | Gets the record wait time in milliseconds. |
| [IEnumerable\<String\>](https://learn.microsoft.com/en-us/dotnet/api/system.collections.generic.ienumerable-1?view=net-8.0) | ReferencedFields | Gets the fields referenced by the file. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | ReferenceFieldsFilePath | Gets the file path of the referenced fields. |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | ReuseDeleted | Gets a value indicating whether deleted records should be reused. |
| [ShareTypes](/reference/datagate/datagate-common/share-types.html) | ShareType | Gets the share type of the file. |

## Methods

| Signature | Description |
| --- | --- |
| [AsyncCopyFromImportFile](#ifileobject-asynccopyfromimportfilestring-filepath-copyfromimportfileoptions-options)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [CopyFromImportFileOptions](/reference/datagate/datagate-client/copy-from-import-file-options.html)) | Asynchronously copies data from an import file to the file.
| [Copy](#ifileobject-copystring-targetdir-string-newname)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Copies the file to a new location with a new name.
| [CopyData](#ifileobject-copydatastring-targetdir-string-newname-string-srcmember-string-newmember-copydataoptions-options-int-fromrrn-int-torrn-int-crecords)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [CopyDataOptions](/reference/datagate/datagate-common/copy-data-options.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Copies data from the file to a new file. If this object does not represent a physical file, returns null.
| [CopyFromImportFile](#ifileobject-copyfromimportfilestring-filepath-copyfromimportfileoptions-options)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [CopyFromImportFileOptions](/reference/datagate/datagate-client/copy-from-import-file-options.html)) | Copies data from an import file to the file.
| [GetAdgDataSet](#adgdataset-getadgdatasetdatasetoptions-opts)([DataSetOptions](/reference/datagate/datagate-common/data-set-options.html)) | Gets the AdgDataSet of the file.
| [ReadCreationAttributes](#void-readcreationattributesxmlreader-reader)([XmlReader](https://learn.microsoft.com/en-us/dotnet/api/system.xml.xmlreader?view=net-8.0)) | Reads the creation attributes of the file from an XML reader.
| [ReadDefinition](#void-readdefinitionxmlreader-reader)([XmlReader](https://learn.microsoft.com/en-us/dotnet/api/system.xml.xmlreader?view=net-8.0)) | Reads the definition of the file from an XML reader.
| [RepairFile](#void-repairfilerepairoptions-repairoptions-adgobserver-observer)([RepairOptions](/reference/datagate/datagate-common/repair-options.html), [AdgObserver](/reference/datagate/datagate-client/adg-observer.html)) | Repairs the file.
| [WriteCreationAttributes](#void-writecreationattributesxmlwriter-writer)([XmlWriter](https://learn.microsoft.com/en-us/dotnet/api/system.xml.xmlwriter?view=net-8.0)) | Writes the creation attributes of the file to an XML writer.
| [WriteDefinition](#void-writedefinitionxmlwriter-writer)([XmlWriter](https://learn.microsoft.com/en-us/dotnet/api/system.xml.xmlwriter?view=net-8.0)) | Writes the definition of the file to an XML writer.

### IFileObject AsyncCopyFromImportFile([string filePath](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [CopyFromImportFileOptions options](/reference/datagate/datagate-client/copy-from-import-file-options.html))

Asynchronously copies data from an import file to the file.

```cs
IFileObject AsyncCopyFromImportFile(string filePath, CopyFromImportFileOptions options)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | filePath | The path of the import file.
| [CopyFromImportFileOptions](/reference/datagate/datagate-client/copy-from-import-file-options.html) | options | The options to use when copying the data.

#### Returns

| Type | Description
| --- | ---
| [IFileObject](/reference/datagate/datagate-client/i-file-object.html) | The file with the copied data.

### IFileObject Copy([string targetDir](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string newName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Copies the file to a new location with a new name.

```cs
IFileObject Copy(string targetDir, string newName)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | targetDir | The target directory to copy the file to.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | newName | The new name of the file.

#### Returns

| Type | Description
| --- | ---
| [IFileObject](/reference/datagate/datagate-client/i-file-object.html) | The copied file.

### IFileObject CopyData([string targetDir](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string newName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string srcMember](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string newMember](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [CopyDataOptions options](/reference/datagate/datagate-common/copy-data-options.html), [int fromRRN](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int toRRN](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int cRecords](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Copies data from the file to a new file. If this object does not represent a physical file, returns null.

```cs
IFileObject CopyData(string targetDir, string newName, string srcMember, string newMember, CopyDataOptions options, int fromRRN, int toRRN, int cRecords)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | targetDir | The target directory to copy the data to.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | newName | The name of the new file.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | srcMember | The source member to copy from.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | newMember | The new member to copy to.
| [CopyDataOptions](/reference/datagate/datagate-common/copy-data-options.html) | options | The options to use when copying the data.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | fromRRN | The relative record number to start copying from.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | toRRN | The relative record number to stop copying at.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | cRecords | The number of records to copy.

#### Returns

| Type | Description
| --- | ---
| [IFileObject](/reference/datagate/datagate-client/i-file-object.html) | The new file with the copied data, or null if this object does not represent a physical file.

### IFileObject CopyFromImportFile([string filePath](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [CopyFromImportFileOptions options](/reference/datagate/datagate-client/copy-from-import-file-options.html))

Copies data from an import file to the file.

```cs
IFileObject CopyFromImportFile(string filePath, CopyFromImportFileOptions options)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | filePath | The path of the import file.
| [CopyFromImportFileOptions](/reference/datagate/datagate-client/copy-from-import-file-options.html) | options | The options to use when copying the data.

#### Returns

| Type | Description
| --- | ---
| [IFileObject](/reference/datagate/datagate-client/i-file-object.html) | The file with the copied data.

### AdgDataSet GetAdgDataSet([DataSetOptions opts](/reference/datagate/datagate-common/data-set-options.html))

Gets the AdgDataSet of the file.

```cs
AdgDataSet GetAdgDataSet(DataSetOptions opts)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DataSetOptions](/reference/datagate/datagate-common/data-set-options.html) | opts | The options to use when getting the AdgDataSet.

#### Returns

| Type | Description
| --- | ---
| [AdgDataSet](/reference/datagate/datagate-client/adg-data-set.html) | The AdgDataSet of the file.

### void ReadCreationAttributes([XmlReader reader](https://learn.microsoft.com/en-us/dotnet/api/system.xml.xmlreader?view=net-8.0))

Reads the creation attributes of the file from an XML reader.

```cs
void ReadCreationAttributes(XmlReader reader)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [XmlReader](https://learn.microsoft.com/en-us/dotnet/api/system.xml.xmlreader?view=net-8.0) | reader | The XML reader to read from.

### void ReadDefinition([XmlReader reader](https://learn.microsoft.com/en-us/dotnet/api/system.xml.xmlreader?view=net-8.0))

Reads the definition of the file from an XML reader.

```cs
void ReadDefinition(XmlReader reader)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [XmlReader](https://learn.microsoft.com/en-us/dotnet/api/system.xml.xmlreader?view=net-8.0) | reader | The XML reader to read from.

### void RepairFile([RepairOptions repairOptions](/reference/datagate/datagate-common/repair-options.html), [AdgObserver observer](/reference/datagate/datagate-client/adg-observer.html))

Repairs the file.

```cs
void RepairFile(RepairOptions repairOptions, AdgObserver observer)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [RepairOptions](/reference/datagate/datagate-common/repair-options.html) | repairOptions | The options to use when repairing the file.
| [AdgObserver](/reference/datagate/datagate-client/adg-observer.html) | observer | The observer to use during the repair.

### void WriteCreationAttributes([XmlWriter writer](https://learn.microsoft.com/en-us/dotnet/api/system.xml.xmlwriter?view=net-8.0))

Writes the creation attributes of the file to an XML writer.

```cs
void WriteCreationAttributes(XmlWriter writer)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [XmlWriter](https://learn.microsoft.com/en-us/dotnet/api/system.xml.xmlwriter?view=net-8.0) | writer | The XML writer to write to.

### void WriteDefinition([XmlWriter writer](https://learn.microsoft.com/en-us/dotnet/api/system.xml.xmlwriter?view=net-8.0))

Writes the definition of the file to an XML writer.

```cs
void WriteDefinition(XmlWriter writer)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [XmlWriter](https://learn.microsoft.com/en-us/dotnet/api/system.xml.xmlwriter?view=net-8.0) | writer | The XML writer to write to.
