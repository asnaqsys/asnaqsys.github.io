---
title: "IAdgObject interface          | QSYS API Reference Guide"
description: "Defines the properties and methods for an ADG (ASNA DataGate) object. "
last_modified_at: 2024-08-08T21:41:32Z
---

Defines the properties and methods for an ADG (ASNA DataGate) object.

**Namespace:** ASNA.DataGate.Client
**Assembly:** ASNA.QSys.DataGate.Client.dll

**Extends:** [IComparable](https://learn.microsoft.com/en-us/dotnet/api/system.icomparable-1?view=net-8.0), [IConnectionHandler](/reference/datagate/datagate-client/i-connection-handler.html), [IDisposable](https://learn.microsoft.com/en-us/dotnet/api/system.idisposable?view=net-8.0)
<br>
<br>
## Thread Safety

Implementations of **IAdgObject** are safe for multithreaded operations.

## Remarks
An ADG object represents a resource in an ASNA DataGate environment, such as a file or a database object. 
This interface defines the common properties and methods that all ADG objects must implement, 
such as methods for managing authorities, locks, and XML serialization, and properties for getting object information.

<br>
<br>

## Properties

| Type | Name | Description
| --- | --- | --- 
| [AdgObjectTypes](/reference/datagate/datagate-common/adg-object-types.html) | AdgObjectType | Gets the type of the ADG object. |
| [AdgSubTypes](/reference/datagate/datagate-common/adg-sub-types.html) | AdgSubType | Gets the subtype of the ADG object. |
| [IEnumerable\<AuthorityEntry\>](https://learn.microsoft.com/en-us/dotnet/api/system.collections.generic.ienumerable-1?view=net-8.0) | Authorities | Gets the authorities of the ADG object. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | Basename | Gets the base name of the ADG object. |
| [IEnumerable\<String\>](https://learn.microsoft.com/en-us/dotnet/api/system.collections.generic.ienumerable-1?view=net-8.0) | BaseObjects | Setting this property to null assigns an empty enumerable value. |
| [XmlDocument](https://learn.microsoft.com/en-us/dotnet/api/system.xml.xmldocument?view=net-8.0) | BasesXml | Gets or sets the XML document representing the base objects of the ADG object. |
| [IEnumerable\<IAdgObject\>](https://learn.microsoft.com/en-us/dotnet/api/system.collections.generic.ienumerable-1?view=net-8.0) | ChildObjects | Gets the child objects of the ADG object. |
| [AdgConnection](/reference/datagate/datagate-client/adg-connection.html) | Connection | Gets the connection associated with the ADG object. |
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | DateCreated | Gets the date and time when the ADG object was created. |
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | DateModified | Gets the date and time when the ADG object was last modified. |
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | DateReferenced | Gets the date and time when the ADG object was last referenced. |
| [IEnumerable\<Dependent\>](https://learn.microsoft.com/en-us/dotnet/api/system.collections.generic.ienumerable-1?view=net-8.0) | DependentObjects | Gets the dependent objects of the ADG object. |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | IsSystemObject | Gets a value indicating whether the ADG object is a system object. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | NameOnServer | Gets the name of the ADG object on the server. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | ObjectID | Gets the ID of the ADG object. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | Owner | Gets the owner of the ADG object. |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | OwnerIsGroup | Gets a value indicating whether the owner of the ADG object is a group. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | ParentID | Gets the ID of the parent of the ADG object. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | PrimaryGroup | Gets the primary group of the ADG object. |
| [XmlSchemaSet](https://learn.microsoft.com/en-us/dotnet/api/system.xml.schema.xmlschemaset?view=net-8.0) | Schema | Gets the XML schema for the ADG object. |
| [IComparer](https://learn.microsoft.com/en-us/dotnet/api/system.collections.icomparer?view=net-8.0) | SortByName | Gets the comparer for sorting ADG objects by name. |
| [IComparer](https://learn.microsoft.com/en-us/dotnet/api/system.collections.icomparer?view=net-8.0) | SortByNameCaseInsensitive | Gets the comparer for sorting ADG objects by name, ignoring case. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | Text | Setting this property to null assigns an empty string value. |

## Methods

| Signature | Description |
| --- | --- |
| [Create()](#void-create) | Creates the ADG object.
| [Duplicate](#void-duplicatestring-scopepath-string-targetpath-string-newname-duplicateoptions-options)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [DuplicateOptions](/reference/datagate/datagate-common/duplicate-options.html)) | Duplicates the ADG object.
| [GrantAuthority](#void-grantauthoritystring-user-authoritytypes-authority)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [AuthorityTypes](/reference/datagate/datagate-common/authority-types.html)) | Grants authority to a user or group for the ADG object.
| [HasLock](#bool-haslocksharetypes-sharetype)([ShareTypes](/reference/datagate/datagate-common/share-types.html)) | Determines whether the ADG object has a lock of the specified type.
| [Lock](#void-locksharetypes-sharetype-waitoptions-waitoption-short-waittime)([ShareTypes](/reference/datagate/datagate-common/share-types.html), [WaitOptions](/reference/datagate/datagate-common/wait-options.html), [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16)) | Locks the ADG object with the specified share type and wait option.
| [MoveTo](#void-movetostring-newpathname)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Moves the ADG object to a new path.
| [ReadBases](#void-readbasesxmlreader-reader)([XmlReader](https://learn.microsoft.com/en-us/dotnet/api/system.xml.xmlreader?view=net-8.0)) | Reads the base objects of the ADG object from an XML reader.
| [Remove()](#void-remove) | Removes the ADG object.
| [Rename](#void-renamestring-newname)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Renames the ADG object.
| [ResolvePathName()](#string-resolvepathname) | Resolves the path name of the ADG object.
| [RevokeAuthority](#void-revokeauthoritystring-username-authoritytypes-authoritytype)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [AuthorityTypes](/reference/datagate/datagate-common/authority-types.html)) | Revokes a specific authority from a user for the ADG object.
| [ToString()](#string-tostring) | Returns a string that represents the ADG object.
| [Unlock](#void-unlocksharetypes-sharetype)([ShareTypes](/reference/datagate/datagate-common/share-types.html)) | Unlocks the ADG object with the specified share type.
| [WriteBases](#void-writebasesxmlwriter-writer)([XmlWriter](https://learn.microsoft.com/en-us/dotnet/api/system.xml.xmlwriter?view=net-8.0)) | Writes the base objects of the ADG object to an XML writer.
| [WriteXml](#void-writexmlxmlwriter-writer-xmloptions-options)([XmlWriter](https://learn.microsoft.com/en-us/dotnet/api/system.xml.xmlwriter?view=net-8.0), [XmlOptions](/reference/datagate/datagate-client/xml-options.html)) | Writes the ADG object to an XML writer using the specified options.
| [WriteXml](#void-writexmlxmlwriter-writer-xmloptions-options-xmlcanceleventhandler-hndlr)([XmlWriter](https://learn.microsoft.com/en-us/dotnet/api/system.xml.xmlwriter?view=net-8.0), [XmlOptions](/reference/datagate/datagate-client/xml-options.html), [XmlCancelEventHandler](/reference/datagate/datagate-client/xml-cancel-event-handler.html)) | Writes the ADG object to an XML writer using the specified options and event handler.
| [WriteXml](#void-writexmlxmlwriter-writer-xmloptions-options-xmlcanceleventhandler-hndlr-openfileadapterdelegate-fileopener)([XmlWriter](https://learn.microsoft.com/en-us/dotnet/api/system.xml.xmlwriter?view=net-8.0), [XmlOptions](/reference/datagate/datagate-client/xml-options.html), [XmlCancelEventHandler](/reference/datagate/datagate-client/xml-cancel-event-handler.html), [OpenFileAdapterDelegate](/reference/datagate/datagate-client/open-file-adapter-delegate.html)) | Writes the ADG object to an XML writer using the specified options, event handler, and file opener delegate.

### void Create()

Creates the ADG object.


#### Remarks
This method is used to create the ADG object. It should be called after the properties of the object have been set, but before the object is used. This method may perform various initialization tasks, such as establishing a connection to the server or allocating resources.

```cs
void Create()
```

### void Duplicate([string ScopePath](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string TargetPath](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string NewName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [DuplicateOptions options](/reference/datagate/datagate-common/duplicate-options.html))

Duplicates the ADG object.


#### Remarks
This method is used to create a duplicate of the ADG object. The ScopePath parameter specifies the path of the object to duplicate. The TargetPath parameter specifies the path where the duplicate object will be placed. The NewName parameter specifies the name for the duplicate object. The options parameter specifies the options for the duplication operation, such as whether to overwrite existing objects.

```cs
void Duplicate(string ScopePath, string TargetPath, string NewName, DuplicateOptions options)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | ScopePath | The scope path of the object to duplicate.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | TargetPath | The target path where the duplicate object will be placed.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | NewName | The new name for the duplicate object.
| [DuplicateOptions](/reference/datagate/datagate-common/duplicate-options.html) | options | The options for the duplication operation.

### void GrantAuthority([string user](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [AuthorityTypes authority](/reference/datagate/datagate-common/authority-types.html))

Grants authority to a user or group for the ADG object.


#### Remarks
This method is used to grant a specific authority to a user or group for the ADG object. The user parameter specifies the user or group to grant the authority to. The authority parameter specifies the authority to grant, which can be read, write, execute, or other types of authority.

```cs
void GrantAuthority(string user, AuthorityTypes authority)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | user | The user or group to grant authority to.
| [AuthorityTypes](/reference/datagate/datagate-common/authority-types.html) | authority | The authority type to grant.

### bool HasLock([ShareTypes ShareType](/reference/datagate/datagate-common/share-types.html))

Determines whether the ADG object has a lock of the specified type.


#### Remarks
This method is used to check if the ADG object has a lock of the specified type. The ShareType parameter specifies the type of lock to check for, which can be read, write, or other types of locks. This can be useful for managing concurrent access to the object.

```cs
bool HasLock(ShareTypes ShareType)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [ShareTypes](/reference/datagate/datagate-common/share-types.html) | ShareType | The type of lock to check for.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | True if the object has a lock of the specified type, false otherwise.

### void Lock([ShareTypes ShareType](/reference/datagate/datagate-common/share-types.html), [WaitOptions WaitOption](/reference/datagate/datagate-common/wait-options.html), [short WaitTime](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Locks the ADG object with the specified share type and wait option.


#### Remarks
This method is used to apply a lock of the specified type to the ADG object. The ShareType parameter specifies the type of lock to apply, which can be read, write, or other types of locks. The WaitOption parameter specifies what to do if the lock cannot be immediately acquired, such as waiting for the lock to become available or throwing an exception.

```cs
void Lock(ShareTypes ShareType, WaitOptions WaitOption, short WaitTime)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [ShareTypes](/reference/datagate/datagate-common/share-types.html) | ShareType | The type of lock to apply.
| [WaitOptions](/reference/datagate/datagate-common/wait-options.html) | WaitOption | The wait option to use if the lock cannot be immediately acquired.
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | WaitTime | The wait time to use if the lock cannot be immediately acquired.

### void MoveTo([string NewPathName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Moves the ADG object to a new path.


#### Remarks
This method is used to move the ADG object to a new path. The NewPathName parameter specifies the new path for the object. This can be useful for organizing objects or for changing the location of an object without changing its contents.

```cs
void MoveTo(string NewPathName)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | NewPathName | The new path for the object.

### void ReadBases([XmlReader reader](https://learn.microsoft.com/en-us/dotnet/api/system.xml.xmlreader?view=net-8.0))

Reads the base objects of the ADG object from an XML reader.


#### Remarks
This method is used to read the base objects of the ADG object from an XML reader. The reader parameter specifies the XML reader to read from. This can be useful for deserializing the object's state from XML.

```cs
void ReadBases(XmlReader reader)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [XmlReader](https://learn.microsoft.com/en-us/dotnet/api/system.xml.xmlreader?view=net-8.0) | reader | The XML reader to read from.

### void Remove()

Removes the ADG object.


#### Remarks
This method is used to remove the ADG object. This can be useful for cleaning up resources or for deleting an object that is no longer needed.

```cs
void Remove()
```

### void Rename([string NewName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Renames the ADG object.


#### Remarks
This method is used to rename the ADG object. The NewName parameter specifies the new name for the object. This can be useful for changing the name of an object without changing its contents or location.

```cs
void Rename(string NewName)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | NewName | The new name for the object.

### string ResolvePathName()

Resolves the path name of the ADG object.


#### Remarks
This method is used to resolve the path name of the ADG object. The path name is resolved according to the rules of the database where the object is stored. This can be useful for obtaining the absolute path of the object, especially if the object was specified with a relative path.

```cs
string ResolvePathName()
```

### void RevokeAuthority([string userName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [AuthorityTypes authorityType](/reference/datagate/datagate-common/authority-types.html))

Revokes a specific authority from a user for the ADG object.


#### Remarks
This method is used to revoke a specific authority from a user for the ADG object. The userName parameter specifies the user to revoke the authority from. The authorityType parameter specifies the type of authority to revoke, which can be read, write, execute, or other types of authority.

```cs
void RevokeAuthority(string userName, AuthorityTypes authorityType)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | userName | The user to revoke the authority from.
| [AuthorityTypes](/reference/datagate/datagate-common/authority-types.html) | authorityType | The type of authority to revoke.

### string ToString()

Returns a string that represents the ADG object.


#### Remarks
This method is used to obtain a string that represents the ADG object. The string typically includes information about the object, such as its name or type. This can be useful for debugging or for displaying information about the object to a user.

```cs
string ToString()
```

### void Unlock([ShareTypes ShareType](/reference/datagate/datagate-common/share-types.html))

Unlocks the ADG object with the specified share type.


#### Remarks
This method is used to remove a lock of the specified type from the ADG object. The ShareType parameter specifies the type of lock to remove, which can be read, write, or other types of locks. This can be useful for managing concurrent access to the object.

```cs
void Unlock(ShareTypes ShareType)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [ShareTypes](/reference/datagate/datagate-common/share-types.html) | ShareType | The type of lock to remove.

### void WriteBases([XmlWriter writer](https://learn.microsoft.com/en-us/dotnet/api/system.xml.xmlwriter?view=net-8.0))

Writes the base objects of the ADG object to an XML writer.


#### Remarks
This method is used to write the base objects of the ADG object to an XML writer. The writer parameter specifies the XML writer to write to. This can be useful for serializing the object's state to XML.

```cs
void WriteBases(XmlWriter writer)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [XmlWriter](https://learn.microsoft.com/en-us/dotnet/api/system.xml.xmlwriter?view=net-8.0) | writer | The XML writer to write to.

### void WriteXml([XmlWriter writer](https://learn.microsoft.com/en-us/dotnet/api/system.xml.xmlwriter?view=net-8.0), [XmlOptions options](/reference/datagate/datagate-client/xml-options.html))

Writes the ADG object to an XML writer using the specified options.


#### Remarks
This method is used to write the ADG object to an XML writer using the specified options. The writer parameter specifies the XML writer to write to. The options parameter specifies the options to use when writing the XML, such as whether to include schema information or whether to indent the XML.This can be useful for serializing the object's state to XML.

```cs
void WriteXml(XmlWriter writer, XmlOptions options)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [XmlWriter](https://learn.microsoft.com/en-us/dotnet/api/system.xml.xmlwriter?view=net-8.0) | writer | The XML writer to write to.
| [XmlOptions](/reference/datagate/datagate-client/xml-options.html) | options | The options to use when writing the XML.

### void WriteXml([XmlWriter writer](https://learn.microsoft.com/en-us/dotnet/api/system.xml.xmlwriter?view=net-8.0), [XmlOptions options](/reference/datagate/datagate-client/xml-options.html), [XmlCancelEventHandler hndlr](/reference/datagate/datagate-client/xml-cancel-event-handler.html))

Writes the ADG object to an XML writer using the specified options and event handler.


#### Remarks
This method is used to write the ADG object to an XML writer using the specified options and event handler. The writer parameter specifies the XML writer to write to. The options parameter specifies the options to use when writing the XML, such as whether to include schema information or whether to indent the XML.The hndlr parameter specifies the event handler for handling cancel events during the write operation. This can be useful for interrupting the write operation based on custom logic.

```cs
void WriteXml(XmlWriter writer, XmlOptions options, XmlCancelEventHandler hndlr)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [XmlWriter](https://learn.microsoft.com/en-us/dotnet/api/system.xml.xmlwriter?view=net-8.0) | writer | The XML writer to write to.
| [XmlOptions](/reference/datagate/datagate-client/xml-options.html) | options | The options to use when writing the XML.
| [XmlCancelEventHandler](/reference/datagate/datagate-client/xml-cancel-event-handler.html) | hndlr | The event handler for handling cancel events during the write operation.

### void WriteXml([XmlWriter writer](https://learn.microsoft.com/en-us/dotnet/api/system.xml.xmlwriter?view=net-8.0), [XmlOptions options](/reference/datagate/datagate-client/xml-options.html), [XmlCancelEventHandler hndlr](/reference/datagate/datagate-client/xml-cancel-event-handler.html), [OpenFileAdapterDelegate fileOpener](/reference/datagate/datagate-client/open-file-adapter-delegate.html))

Writes the ADG object to an XML writer using the specified options, event handler, and file opener delegate.


#### Remarks
This method is used to write the ADG object to an XML writer using the specified options, event handler, and file opener delegate. The writer parameter specifies the XML writer to write to. The options parameter specifies the options to use when writing the XML, such as whether to include schema information or whether to indent the XML.The hndlr parameter specifies the event handler for handling cancel events during the write operation. This can be useful for interrupting the write operation based on custom logic.The fileOpener parameter specifies the delegate for opening a file during the write operation. This can be useful for writing the XML to a specific file or stream.

```cs
void WriteXml(XmlWriter writer, XmlOptions options, XmlCancelEventHandler hndlr, OpenFileAdapterDelegate fileOpener)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [XmlWriter](https://learn.microsoft.com/en-us/dotnet/api/system.xml.xmlwriter?view=net-8.0) | writer | The XML writer to write to.
| [XmlOptions](/reference/datagate/datagate-client/xml-options.html) | options | The options to use when writing the XML.
| [XmlCancelEventHandler](/reference/datagate/datagate-client/xml-cancel-event-handler.html) | hndlr | The event handler for handling cancel events during the write operation.
| [OpenFileAdapterDelegate](/reference/datagate/datagate-client/open-file-adapter-delegate.html) | fileOpener | The delegate for opening a file during the write operation.
