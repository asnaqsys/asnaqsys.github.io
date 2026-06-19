---
title: "IAdgObject interface"
description: "Defines the properties and methods for an ADG (ASNA DataGate) object. "
last_modified_at: 2024-08-09T17:25:07Z
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
| [Create()](i-adg-object-create.html#void-create) | Creates the ADG object.
| [Duplicate](i-adg-object-duplicate.html#void-duplicate-string-scopepath-string-targetpath-string-newname-duplicateoptions-options)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [DuplicateOptions](/reference/datagate/datagate-common/duplicate-options.html)) | Duplicates the ADG object.
| [GrantAuthority](i-adg-object-grantauthority.html#void-grantauthority-string-user-authoritytypes-authority)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [AuthorityTypes](/reference/datagate/datagate-common/authority-types.html)) | Grants authority to a user or group for the ADG object.
| [HasLock](i-adg-object-haslock.html#bool-haslock-sharetypes-sharetype)([ShareTypes](/reference/datagate/datagate-common/share-types.html)) | Determines whether the ADG object has a lock of the specified type.
| [Lock](i-adg-object-lock.html#void-lock-sharetypes-sharetype-waitoptions-waitoption-short-waittime)([ShareTypes](/reference/datagate/datagate-common/share-types.html), [WaitOptions](/reference/datagate/datagate-common/wait-options.html), [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16)) | Locks the ADG object with the specified share type and wait option.
| [MoveTo](i-adg-object-moveto.html#void-moveto-string-newpathname)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Moves the ADG object to a new path.
| [ReadBases](i-adg-object-readbases.html#void-readbases-xmlreader-reader)([XmlReader](https://learn.microsoft.com/en-us/dotnet/api/system.xml.xmlreader?view=net-8.0)) | Reads the base objects of the ADG object from an XML reader.
| [Remove()](i-adg-object-remove.html#void-remove) | Removes the ADG object.
| [Rename](i-adg-object-rename.html#void-rename-string-newname)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Renames the ADG object.
| [ResolvePathName()](i-adg-object-resolvepathname.html#string-resolvepathname) | Resolves the path name of the ADG object.
| [RevokeAuthority](i-adg-object-revokeauthority.html#void-revokeauthority-string-username-authoritytypes-authoritytype)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [AuthorityTypes](/reference/datagate/datagate-common/authority-types.html)) | Revokes a specific authority from a user for the ADG object.
| [ToString()](i-adg-object-tostring.html#string-tostring) | Returns a string that represents the ADG object.
| [Unlock](i-adg-object-unlock.html#void-unlock-sharetypes-sharetype)([ShareTypes](/reference/datagate/datagate-common/share-types.html)) | Unlocks the ADG object with the specified share type.
| [WriteBases](i-adg-object-writebases.html#void-writebases-xmlwriter-writer)([XmlWriter](https://learn.microsoft.com/en-us/dotnet/api/system.xml.xmlwriter?view=net-8.0)) | Writes the base objects of the ADG object to an XML writer.
| [WriteXml](i-adg-object-writexml.html#void-writexml-xmlwriter-writer-xmloptions-options)([XmlWriter](https://learn.microsoft.com/en-us/dotnet/api/system.xml.xmlwriter?view=net-8.0), [XmlOptions](/reference/datagate/datagate-client/xml-options.html)) | Writes the ADG object to an XML writer using the specified options.
| [WriteXml](i-adg-object-writexml.html#void-writexml-xmlwriter-writer-xmloptions-options-xmlcanceleventhandler-hndlr)([XmlWriter](https://learn.microsoft.com/en-us/dotnet/api/system.xml.xmlwriter?view=net-8.0), [XmlOptions](/reference/datagate/datagate-client/xml-options.html), [XmlCancelEventHandler](/reference/datagate/datagate-client/xml-cancel-event-handler.html)) | Writes the ADG object to an XML writer using the specified options and event handler.
| [WriteXml](i-adg-object-writexml.html#void-writexml-xmlwriter-writer-xmloptions-options-xmlcanceleventhandler-hndlr-openfileadapterdelegate-fileopener)([XmlWriter](https://learn.microsoft.com/en-us/dotnet/api/system.xml.xmlwriter?view=net-8.0), [XmlOptions](/reference/datagate/datagate-client/xml-options.html), [XmlCancelEventHandler](/reference/datagate/datagate-client/xml-cancel-event-handler.html), [OpenFileAdapterDelegate](/reference/datagate/datagate-client/open-file-adapter-delegate.html)) | Writes the ADG object to an XML writer using the specified options, event handler, and file opener delegate.

