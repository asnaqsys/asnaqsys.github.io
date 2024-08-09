---
title: "AdgFactory class              | QSYS API Reference Guide"
description: "The AdgFactory class static methods construct instances of IAdgObject representing database files, libraries, and members along with IDataArea for dat"
last_modified_at: 2024-08-09T16:18:40Z
---

The AdgFactory class static methods construct instances of IAdgObject representing database files, libraries, and members along with IDataArea for data areas.

**Namespace:** ASNA.DataGate.Client
**Assembly:** ASNA.QSys.DataGate.Client.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>
## Thread Safety

Any public static (**Shared**) members of this type are safe for multithreaded operations. 

Any instance members are not guaranteed to be thread safe.


## Properties

| Type | Name | Description
| --- | --- | --- 
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | AppDefaultBulkCopyTimeout | Gets or sets the default timeout for bulk copy operations. |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | AppUseBulkCopyByDefault | Gets or sets a value indicating whether the application should use bulk copy by default. |

## Methods

| Signature | Description |
| --- | --- |
| [NewDataArea](#idataarea-newdataareaadgconnection-cn-string-pathname)([AdgConnection](/reference/datagate/datagate-client/adg-connection.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Creates a new instance of the  interface with an unknown subtype.
| [NewDataArea](#idataarea-newdataareaadgconnection-cn-string-pathname-adgsubtypes-dataareatype)([AdgConnection](/reference/datagate/datagate-client/adg-connection.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [AdgSubTypes](/reference/datagate/datagate-common/adg-sub-types.html)) | Creates a new instance of the  interface with a specified subtype.
| [NewDirectory](#idirectory-newdirectoryadgconnection-cn-string-pathname)([AdgConnection](/reference/datagate/datagate-client/adg-connection.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Creates a new instance of the  interface.
| [NewFile](#ifileobject-newfileadgconnection-cn-string-pathname)([AdgConnection](/reference/datagate/datagate-client/adg-connection.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Creates a new instance of the  interface.
| [NewLibraryList](#ilibrarylist-newlibrarylistadgconnection-cn)([AdgConnection](/reference/datagate/datagate-client/adg-connection.html)) | Creates a new instance of the  interface.
| [NewMember](#imember-newmemberadgconnection-cn-string-pathname)([AdgConnection](/reference/datagate/datagate-client/adg-connection.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Creates a new instance of the  interface.
| [NewObject](#iadgobject-newobjectadgconnection-cn-adgobjecttypes-type-string-path)([AdgConnection](/reference/datagate/datagate-client/adg-connection.html), [AdgObjectTypes](/reference/datagate/datagate-common/adg-object-types.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Creates a new instance of the  interface.
| [NewSystemValue](#isystemvalue-newsystemvalueadgconnection-cn-bool-withnewtransaction)([AdgConnection](/reference/datagate/datagate-client/adg-connection.html), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Creates a new instance of the  interface.
| [ReadXml](#iadgobject-readxmladgconnection-cn-string-containerpath-adgobjecttypes-docobjecttype-string-docobjectnewname-xmlreader-reader-xmloptions-options-xmlcanceleventhandler-observer)([AdgConnection](/reference/datagate/datagate-client/adg-connection.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [AdgObjectTypes](/reference/datagate/datagate-common/adg-object-types.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [XmlReader](https://learn.microsoft.com/en-us/dotnet/api/system.xml.xmlreader?view=net-8.0), [XmlOptions](/reference/datagate/datagate-client/xml-options.html), [XmlCancelEventHandler](/reference/datagate/datagate-client/xml-cancel-event-handler.html)) | Reads an XML document and creates a new instance of the  interface.
| [ReadXml](#iadgobject-readxmladgconnection-cn-string-containerpath-adgobjecttypes-docobjecttype-string-docobjectnewname-xmlreader-reader-xmloptions-options)([AdgConnection](/reference/datagate/datagate-client/adg-connection.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [AdgObjectTypes](/reference/datagate/datagate-common/adg-object-types.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [XmlReader](https://learn.microsoft.com/en-us/dotnet/api/system.xml.xmlreader?view=net-8.0), [XmlOptions](/reference/datagate/datagate-client/xml-options.html)) | Reads an XML document and creates a new instance of the  interface.
| [ReadXml](#iadgobject-readxmladgconnection-cn-string-containerpath-adgobjecttypes-docobjecttype-xmlreader-reader-xmloptions-options-xmlcanceleventhandler-observer)([AdgConnection](/reference/datagate/datagate-client/adg-connection.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [AdgObjectTypes](/reference/datagate/datagate-common/adg-object-types.html), [XmlReader](https://learn.microsoft.com/en-us/dotnet/api/system.xml.xmlreader?view=net-8.0), [XmlOptions](/reference/datagate/datagate-client/xml-options.html), [XmlCancelEventHandler](/reference/datagate/datagate-client/xml-cancel-event-handler.html)) | Reads an XML document and creates a new instance of the  interface.
| [ReadXml](#iadgobject-readxmladgconnection-cn-string-containerpath-adgobjecttypes-docobjecttype-xmlreader-reader-xmloptions-options)([AdgConnection](/reference/datagate/datagate-client/adg-connection.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [AdgObjectTypes](/reference/datagate/datagate-common/adg-object-types.html), [XmlReader](https://learn.microsoft.com/en-us/dotnet/api/system.xml.xmlreader?view=net-8.0), [XmlOptions](/reference/datagate/datagate-client/xml-options.html)) | Reads an XML document and creates a new instance of the  interface.
| [Synchronized](#iadgobject-synchronizediadgobject-adgobj)([IAdgObject](/reference/datagate/datagate-client/i-adg-object.html)) | Wraps an  in a synchronized (thread-safe) wrapper.
| [Synchronized](#ilibrarylist-synchronizedilibrarylist-llobj)([ILibraryList](/reference/datagate/datagate-client/i-library-list.html)) | Wraps an  in a synchronized (thread-safe) wrapper.

### IDataArea NewDataArea([AdgConnection cn](/reference/datagate/datagate-client/adg-connection.html), [string PathName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Creates a new instance of the  interface with an unknown subtype.


#### Remarks
This method uses the  method to create a new instance of the  interface.The  method is a generic method that takes a function delegate as a parameter.The function delegate is responsible for creating the new instance.If the  parameter is null, an  is thrown.The subtype of the data area is set to .

```cs
IDataArea NewDataArea(AdgConnection cn, string PathName)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [AdgConnection](/reference/datagate/datagate-client/adg-connection.html) | cn | The  to use for the operation.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | PathName | The path name of the data area.

#### Returns

| Type | Description
| --- | ---
| [IDataArea](/reference/datagate/datagate-client/i-data-area.html) | A new instance of the  interface.

### IDataArea NewDataArea([AdgConnection cn](/reference/datagate/datagate-client/adg-connection.html), [string PathName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [AdgSubTypes DataAreaType](/reference/datagate/datagate-common/adg-sub-types.html))

Creates a new instance of the  interface with a specified subtype.


#### Remarks
This method uses the  method to create a new instance of the  interface.The  method is a generic method that takes a function delegate as a parameter.The function delegate is responsible for creating the new instance.If the  parameter is null, an  is thrown.The subtype of the data area is set to the value of the  parameter.

```cs
IDataArea NewDataArea(AdgConnection cn, string PathName, AdgSubTypes DataAreaType)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [AdgConnection](/reference/datagate/datagate-client/adg-connection.html) | cn | The  to use for the operation.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | PathName | The path name of the data area.
| [AdgSubTypes](/reference/datagate/datagate-common/adg-sub-types.html) | DataAreaType | The subtype of the data area.

#### Returns

| Type | Description
| --- | ---
| [IDataArea](/reference/datagate/datagate-client/i-data-area.html) | A new instance of the  interface.

### IDirectory NewDirectory([AdgConnection cn](/reference/datagate/datagate-client/adg-connection.html), [string PathName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Creates a new instance of the  interface.


#### Remarks
This method uses the  method to create a new instance of the  interface.The  method is a generic method that takes a function delegate as a parameter.The function delegate is responsible for creating the new instance.If the  parameter is null, an  is thrown.

```cs
IDirectory NewDirectory(AdgConnection cn, string PathName)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [AdgConnection](/reference/datagate/datagate-client/adg-connection.html) | cn | The  to use for the operation.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | PathName | The path name of the directory.

#### Returns

| Type | Description
| --- | ---
| [IDirectory](/reference/datagate/datagate-client/i-directory.html) | A new instance of the  interface.

### IFileObject NewFile([AdgConnection cn](/reference/datagate/datagate-client/adg-connection.html), [string PathName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Creates a new instance of the  interface.


#### Remarks
This method uses the  method to create a new instance of the  interface.The  method is a generic method that takes a function delegate as a parameter.The function delegate is responsible for creating the new instance.If the  parameter is null, an  is thrown.

```cs
IFileObject NewFile(AdgConnection cn, string PathName)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [AdgConnection](/reference/datagate/datagate-client/adg-connection.html) | cn | The  to use for the operation.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | PathName | The path name of the file.

#### Returns

| Type | Description
| --- | ---
| [IFileObject](/reference/datagate/datagate-client/i-file-object.html) | A new instance of the  interface.

### ILibraryList NewLibraryList([AdgConnection cn](/reference/datagate/datagate-client/adg-connection.html))

Creates a new instance of the  interface.


#### Remarks
This method uses the  method to create a new instance of the  interface.The  method is a generic method that takes a function delegate as a parameter.The function delegate is responsible for creating the new instance.If the  parameter is null, an  is thrown.

```cs
ILibraryList NewLibraryList(AdgConnection cn)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [AdgConnection](/reference/datagate/datagate-client/adg-connection.html) | cn | The  to use for the operation.

#### Returns

| Type | Description
| --- | ---
| [ILibraryList](/reference/datagate/datagate-client/i-library-list.html) | A new instance of the  interface.

### IMember NewMember([AdgConnection cn](/reference/datagate/datagate-client/adg-connection.html), [string PathName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Creates a new instance of the  interface.


#### Remarks
This method uses the  method to create a new instance of the  interface.The  method is a generic method that takes a function delegate as a parameter.The function delegate is responsible for creating the new instance.If the  parameter is null, an  is thrown.

```cs
IMember NewMember(AdgConnection cn, string PathName)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [AdgConnection](/reference/datagate/datagate-client/adg-connection.html) | cn | The  to use for the operation.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | PathName | The path name of the member.

#### Returns

| Type | Description
| --- | ---
| [IMember](/reference/datagate/datagate-client/i-member.html) | A new instance of the  interface.

### IAdgObject NewObject([AdgConnection cn](/reference/datagate/datagate-client/adg-connection.html), [AdgObjectTypes type](/reference/datagate/datagate-common/adg-object-types.html), [string path](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Creates a new instance of the  interface.


#### Remarks
This method uses the  method to create a new instance of the  interface.The  method is a generic method that takes a function delegate as a parameter.The function delegate is responsible for creating the new instance.If the  parameter is null, an  is thrown.

```cs
IAdgObject NewObject(AdgConnection cn, AdgObjectTypes type, string path)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [AdgConnection](/reference/datagate/datagate-client/adg-connection.html) | cn | The  to use for the operation.
| [AdgObjectTypes](/reference/datagate/datagate-common/adg-object-types.html) | type | The type of the object to create.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | path | The path of the object to create.

#### Returns

| Type | Description
| --- | ---
| [IAdgObject](/reference/datagate/datagate-client/i-adg-object.html) | A new instance of the  interface.

### ISystemValue NewSystemValue([AdgConnection cn](/reference/datagate/datagate-client/adg-connection.html), [bool withNewTransaction](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Creates a new instance of the  interface.


#### Remarks
This method uses the  method to create a new instance of the  interface.The  method is a generic method that takes a function delegate as a parameter.The function delegate is responsible for creating the new instance.If the  parameter is null, an  is thrown.

```cs
ISystemValue NewSystemValue(AdgConnection cn, bool withNewTransaction)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [AdgConnection](/reference/datagate/datagate-client/adg-connection.html) | cn | The  to use for the operation.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | withNewTransaction | A boolean value indicating whether to create a new transaction.

#### Returns

| Type | Description
| --- | ---
| [ISystemValue](/reference/datagate/datagate-client/i-system-value.html) | A new instance of the  interface.

### IAdgObject ReadXml([AdgConnection cn](/reference/datagate/datagate-client/adg-connection.html), [string containerPath](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [AdgObjectTypes docObjectType](/reference/datagate/datagate-common/adg-object-types.html), [string docObjectNewName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [XmlReader reader](https://learn.microsoft.com/en-us/dotnet/api/system.xml.xmlreader?view=net-8.0), [XmlOptions options](/reference/datagate/datagate-client/xml-options.html), [XmlCancelEventHandler observer](/reference/datagate/datagate-client/xml-cancel-event-handler.html))

Reads an XML document and creates a new instance of the  interface.


#### Remarks
This method uses the  method to read an XML document and create a new instance of the  interface.The  method takes several parameters, including an , a container path, an object type, a new object name, an , an , and an .If the  parameter is null, an  is thrown.

```cs
IAdgObject ReadXml(AdgConnection cn, string containerPath, AdgObjectTypes docObjectType, string docObjectNewName, XmlReader reader, XmlOptions options, XmlCancelEventHandler observer)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [AdgConnection](/reference/datagate/datagate-client/adg-connection.html) | cn | The  to use for the operation.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | containerPath | The path of the container for the object.
| [AdgObjectTypes](/reference/datagate/datagate-common/adg-object-types.html) | docObjectType | The type of the object to create.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | docObjectNewName | The new name for the object, or null to use the existing name.
| [XmlReader](https://learn.microsoft.com/en-us/dotnet/api/system.xml.xmlreader?view=net-8.0) | reader | The  to use to read the XML document.
| [XmlOptions](/reference/datagate/datagate-client/xml-options.html) | options | The  to use when reading the XML document.
| [XmlCancelEventHandler](/reference/datagate/datagate-client/xml-cancel-event-handler.html) | observer | An optional  to observe the reading process.

#### Returns

| Type | Description
| --- | ---
| [IAdgObject](/reference/datagate/datagate-client/i-adg-object.html) | A new instance of the  interface.

### IAdgObject ReadXml([AdgConnection cn](/reference/datagate/datagate-client/adg-connection.html), [string containerPath](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [AdgObjectTypes docObjectType](/reference/datagate/datagate-common/adg-object-types.html), [string docObjectNewName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [XmlReader reader](https://learn.microsoft.com/en-us/dotnet/api/system.xml.xmlreader?view=net-8.0), [XmlOptions options](/reference/datagate/datagate-client/xml-options.html))

Reads an XML document and creates a new instance of the  interface.


#### Remarks
This method is a convenience overload of the ReadXml method that does not require an  parameter.It calls the ReadXml method with the provided parameters and a null .If the  parameter is null, an  is thrown.

```cs
IAdgObject ReadXml(AdgConnection cn, string containerPath, AdgObjectTypes docObjectType, string docObjectNewName, XmlReader reader, XmlOptions options)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [AdgConnection](/reference/datagate/datagate-client/adg-connection.html) | cn | The  to use for the operation.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | containerPath | The path of the container for the object.
| [AdgObjectTypes](/reference/datagate/datagate-common/adg-object-types.html) | docObjectType | The type of the object to create.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | docObjectNewName | The new name for the object.
| [XmlReader](https://learn.microsoft.com/en-us/dotnet/api/system.xml.xmlreader?view=net-8.0) | reader | The  to use to read the XML document.
| [XmlOptions](/reference/datagate/datagate-client/xml-options.html) | options | The  to use when reading the XML document.

#### Returns

| Type | Description
| --- | ---
| [IAdgObject](/reference/datagate/datagate-client/i-adg-object.html) | A new instance of the  interface.

### IAdgObject ReadXml([AdgConnection cn](/reference/datagate/datagate-client/adg-connection.html), [string containerPath](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [AdgObjectTypes docObjectType](/reference/datagate/datagate-common/adg-object-types.html), [XmlReader reader](https://learn.microsoft.com/en-us/dotnet/api/system.xml.xmlreader?view=net-8.0), [XmlOptions options](/reference/datagate/datagate-client/xml-options.html), [XmlCancelEventHandler observer](/reference/datagate/datagate-client/xml-cancel-event-handler.html))

Reads an XML document and creates a new instance of the  interface.


#### Remarks
This method is a convenience overload of the ReadXml method that does not require a new object name parameter.It calls the ReadXml method with the provided parameters and a null new object name.If the  parameter is null, an  is thrown.

```cs
IAdgObject ReadXml(AdgConnection cn, string containerPath, AdgObjectTypes docObjectType, XmlReader reader, XmlOptions options, XmlCancelEventHandler observer)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [AdgConnection](/reference/datagate/datagate-client/adg-connection.html) | cn | The  to use for the operation.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | containerPath | The path of the container for the object.
| [AdgObjectTypes](/reference/datagate/datagate-common/adg-object-types.html) | docObjectType | The type of the object to create.
| [XmlReader](https://learn.microsoft.com/en-us/dotnet/api/system.xml.xmlreader?view=net-8.0) | reader | The  to use to read the XML document.
| [XmlOptions](/reference/datagate/datagate-client/xml-options.html) | options | The  to use when reading the XML document.
| [XmlCancelEventHandler](/reference/datagate/datagate-client/xml-cancel-event-handler.html) | observer | An optional  to observe the reading process.

#### Returns

| Type | Description
| --- | ---
| [IAdgObject](/reference/datagate/datagate-client/i-adg-object.html) | A new instance of the  interface.

### IAdgObject ReadXml([AdgConnection cn](/reference/datagate/datagate-client/adg-connection.html), [string containerPath](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [AdgObjectTypes docObjectType](/reference/datagate/datagate-common/adg-object-types.html), [XmlReader reader](https://learn.microsoft.com/en-us/dotnet/api/system.xml.xmlreader?view=net-8.0), [XmlOptions options](/reference/datagate/datagate-client/xml-options.html))

Reads an XML document and creates a new instance of the  interface.


#### Remarks
This method is a convenience overload of the ReadXml method that does not require a new object name or an  parameter.It calls the ReadXml method with the provided parameters, a null new object name, and a null .If the  parameter is null, an  is thrown.

```cs
IAdgObject ReadXml(AdgConnection cn, string containerPath, AdgObjectTypes docObjectType, XmlReader reader, XmlOptions options)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [AdgConnection](/reference/datagate/datagate-client/adg-connection.html) | cn | The  to use for the operation.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | containerPath | The path of the container for the object.
| [AdgObjectTypes](/reference/datagate/datagate-common/adg-object-types.html) | docObjectType | The type of the object to create.
| [XmlReader](https://learn.microsoft.com/en-us/dotnet/api/system.xml.xmlreader?view=net-8.0) | reader | The  to use to read the XML document.
| [XmlOptions](/reference/datagate/datagate-client/xml-options.html) | options | The  to use when reading the XML document.

#### Returns

| Type | Description
| --- | ---
| [IAdgObject](/reference/datagate/datagate-client/i-adg-object.html) | A new instance of the  interface.

### IAdgObject Synchronized([IAdgObject adgObj](/reference/datagate/datagate-client/i-adg-object.html))

Wraps an  in a synchronized (thread-safe) wrapper.


#### Remarks
This method checks the type of the  parameter and wraps it in a corresponding synchronized (thread-safe) wrapper.If the object is already a synchronized object, it is returned as is.If the object is an , it is wrapped in a .If the object is an , it is wrapped in a .If the object is an , it is wrapped in a .If the object is an , it is wrapped in a .If the object is none of the above types, it is wrapped in a .

```cs
IAdgObject Synchronized(IAdgObject adgObj)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [IAdgObject](/reference/datagate/datagate-client/i-adg-object.html) | adgObj | The  to wrap.

#### Returns

| Type | Description
| --- | ---
| [IAdgObject](/reference/datagate/datagate-client/i-adg-object.html) | A thread-safe wrapper around the .

### ILibraryList Synchronized([ILibraryList llObj](/reference/datagate/datagate-client/i-library-list.html))

Wraps an  in a synchronized (thread-safe) wrapper.


#### Remarks
This method checks if the  parameter is already a synchronized object. If it is, the method returns the object as is. If it's not, the method wraps it in a  to ensure thread safety.

```cs
ILibraryList Synchronized(ILibraryList llObj)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [ILibraryList](/reference/datagate/datagate-client/i-library-list.html) | llObj | The  to wrap.

#### Returns

| Type | Description
| --- | ---
| [ILibraryList](/reference/datagate/datagate-client/i-library-list.html) | A thread-safe wrapper around the .
