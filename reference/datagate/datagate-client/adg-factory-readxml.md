---
title: "AdgFactory.ReadXml Method"
description: "Reads an XML document and creates a new instance of the interface."
---

## Definition

**Namespace:** ASNA.DataGate.Client  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Reads an XML document and creates a new instance of the interface.

## Overloads

| Signature | Description |
| --- | --- |
| [ReadXml](#iadgobject-readxml-adgconnection-cn-string-containerpath-adgobjecttypes-docobjecttype-string-docobjectnewname-xmlreader-reader-xmloptions-options-xmlcanceleventhandler-observer)(IAdgObject ReadXml(AdgConnection cn, string containerPath, AdgObjectTypes docObjectType, string docObjectNewName, XmlReader reader, XmlOptions options, XmlCancelEventHandler observer)) | Reads an XML document and creates a new instance of the interface. |
| [ReadXml](#iadgobject-readxml-adgconnection-cn-string-containerpath-adgobjecttypes-docobjecttype-string-docobjectnewname-xmlreader-reader-xmloptions-options)(IAdgObject ReadXml(AdgConnection cn, string containerPath, AdgObjectTypes docObjectType, string docObjectNewName, XmlReader reader, XmlOptions options)) | Reads an XML document and creates a new instance of the interface. |
| [ReadXml](#iadgobject-readxml-adgconnection-cn-string-containerpath-adgobjecttypes-docobjecttype-xmlreader-reader-xmloptions-options-xmlcanceleventhandler-observer)(IAdgObject ReadXml(AdgConnection cn, string containerPath, AdgObjectTypes docObjectType, XmlReader reader, XmlOptions options, XmlCancelEventHandler observer)) | Reads an XML document and creates a new instance of the interface. |
| [ReadXml](#iadgobject-readxml-adgconnection-cn-string-containerpath-adgobjecttypes-docobjecttype-xmlreader-reader-xmloptions-options)(IAdgObject ReadXml(AdgConnection cn, string containerPath, AdgObjectTypes docObjectType, XmlReader reader, XmlOptions options)) | Reads an XML document and creates a new instance of the interface. |

<a id="iadgobject-readxml-adgconnection-cn-string-containerpath-adgobjecttypes-docobjecttype-string-docobjectnewname-xmlreader-reader-xmloptions-options-xmlcanceleventhandler-observer"></a>
## IAdgObject ReadXml(AdgConnection cn, string containerPath, AdgObjectTypes docObjectType, string docObjectNewName, XmlReader reader, XmlOptions options, XmlCancelEventHandler observer)

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

<a id="iadgobject-readxml-adgconnection-cn-string-containerpath-adgobjecttypes-docobjecttype-string-docobjectnewname-xmlreader-reader-xmloptions-options"></a>
## IAdgObject ReadXml(AdgConnection cn, string containerPath, AdgObjectTypes docObjectType, string docObjectNewName, XmlReader reader, XmlOptions options)

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

<a id="iadgobject-readxml-adgconnection-cn-string-containerpath-adgobjecttypes-docobjecttype-xmlreader-reader-xmloptions-options-xmlcanceleventhandler-observer"></a>
## IAdgObject ReadXml(AdgConnection cn, string containerPath, AdgObjectTypes docObjectType, XmlReader reader, XmlOptions options, XmlCancelEventHandler observer)

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

<a id="iadgobject-readxml-adgconnection-cn-string-containerpath-adgobjecttypes-docobjecttype-xmlreader-reader-xmloptions-options"></a>
## IAdgObject ReadXml(AdgConnection cn, string containerPath, AdgObjectTypes docObjectType, XmlReader reader, XmlOptions options)

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

## See Also
- [AdgFactory class](adg-factory.html)
