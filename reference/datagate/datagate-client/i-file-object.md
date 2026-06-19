---
title: "IFileObject interface"
description: "Defines the contract for managing a file in the ASNA DataGate client. "
last_modified_at: 2024-08-09T17:25:07Z
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
| [AsyncCopyFromImportFile](i-file-object-asynccopyfromimportfile.html#ifileobject-asynccopyfromimportfile-string-filepath-copyfromimportfileoptions-options)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [CopyFromImportFileOptions](/reference/datagate/datagate-client/copy-from-import-file-options.html)) | Asynchronously copies data from an import file to the file.
| [Copy](i-file-object-copy.html#ifileobject-copy-string-targetdir-string-newname)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Copies the file to a new location with a new name.
| [CopyData](i-file-object-copydata.html#ifileobject-copydata-string-targetdir-string-newname-string-srcmember-string-newmember-copydataoptions-options-int-fromrrn-int-torrn-int-crecords)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [CopyDataOptions](/reference/datagate/datagate-common/copy-data-options.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Copies data from the file to a new file. If this object does not represent a physical file, returns null.
| [CopyFromImportFile](i-file-object-copyfromimportfile.html#ifileobject-copyfromimportfile-string-filepath-copyfromimportfileoptions-options)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [CopyFromImportFileOptions](/reference/datagate/datagate-client/copy-from-import-file-options.html)) | Copies data from an import file to the file.
| [GetAdgDataSet](i-file-object-getadgdataset.html#adgdataset-getadgdataset-datasetoptions-opts)([DataSetOptions](/reference/datagate/datagate-common/data-set-options.html)) | Gets the AdgDataSet of the file.
| [InspectFile](i-file-object-inspectfile.html#void-inspectfile-inspectfileparts-parts-inspectfileoutput-output-int32-errorcount-adgobserver-observer)([InspectFileParts](/reference/datagate/datagate-common/inspect-file-parts.html), [InspectFileOutput](/reference/datagate/datagate-common/inspect-file-output.html), [Int32&](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [AdgObserver](/reference/datagate/datagate-client/adg-observer.html)) | Inspects the file.
| [ReadCreationAttributes](i-file-object-readcreationattributes.html#void-readcreationattributes-xmlreader-reader)([XmlReader](https://learn.microsoft.com/en-us/dotnet/api/system.xml.xmlreader?view=net-8.0)) | Reads the creation attributes of the file from an XML reader.
| [ReadDefinition](i-file-object-readdefinition.html#void-readdefinition-xmlreader-reader)([XmlReader](https://learn.microsoft.com/en-us/dotnet/api/system.xml.xmlreader?view=net-8.0)) | Reads the definition of the file from an XML reader.
| [RepairFile](i-file-object-repairfile.html#void-repairfile-repairoptions-repairoptions-adgobserver-observer)([RepairOptions](/reference/datagate/datagate-common/repair-options.html), [AdgObserver](/reference/datagate/datagate-client/adg-observer.html)) | Repairs the file.
| [WriteCreationAttributes](i-file-object-writecreationattributes.html#void-writecreationattributes-xmlwriter-writer)([XmlWriter](https://learn.microsoft.com/en-us/dotnet/api/system.xml.xmlwriter?view=net-8.0)) | Writes the creation attributes of the file to an XML writer.
| [WriteDefinition](i-file-object-writedefinition.html#void-writedefinition-xmlwriter-writer)([XmlWriter](https://learn.microsoft.com/en-us/dotnet/api/system.xml.xmlwriter?view=net-8.0)) | Writes the definition of the file to an XML writer.

