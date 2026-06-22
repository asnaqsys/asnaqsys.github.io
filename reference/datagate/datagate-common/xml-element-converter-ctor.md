---
title: "XmlElementConverter Constructors"
description: "Initializes a new instance of the class with the specified XML container and element name."
---

## Definition

**Namespace:** ASNA.DataGate.Common  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Initializes a new instance of the class with the specified XML container and element name.

## Overloads

| Name | Description |
| --- | --- |
| [XmlElementConverter](#xmlelementconverter-xmlnode-ischemaelementname)([XmlNode](https://learn.microsoft.com/en-us/dotnet/api/system.xml.xmlnode?view=net-8.0), [ISchemaElementName](/reference/datagate/datagate-common/i-schema-element-name.html)) | Initializes a new instance of the class with the specified XML container and element name. |
| [XmlElementConverter](#xmlelementconverter-xmlnode-xmlelement-ischemaelementname)([XmlNode](https://learn.microsoft.com/en-us/dotnet/api/system.xml.xmlnode?view=net-8.0), [XmlElement](https://learn.microsoft.com/en-us/dotnet/api/system.xml.xmlelement?view=net-8.0), [ISchemaElementName](/reference/datagate/datagate-common/i-schema-element-name.html)) | Initializes a new instance of the class with the specified XML container, XML element, and element name. |

<a id="xmlelementconverter-xmlnode-ischemaelementname"></a>
### XmlElementConverter([XmlNode](https://learn.microsoft.com/en-us/dotnet/api/system.xml.xmlnode?view=net-8.0), [ISchemaElementName](/reference/datagate/datagate-common/i-schema-element-name.html))

Initializes a new instance of the  class with the specified XML container and element name.

```cs
XmlElementConverter(XmlNode, ISchemaElementName)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [XmlNode](https://learn.microsoft.com/en-us/dotnet/api/system.xml.xmlnode?view=net-8.0) | container | The XML container.
| [ISchemaElementName](/reference/datagate/datagate-common/i-schema-element-name.html) | elementName | The name of the element.

<a id="xmlelementconverter-xmlnode-xmlelement-ischemaelementname"></a>
### XmlElementConverter([XmlNode](https://learn.microsoft.com/en-us/dotnet/api/system.xml.xmlnode?view=net-8.0), [XmlElement](https://learn.microsoft.com/en-us/dotnet/api/system.xml.xmlelement?view=net-8.0), [ISchemaElementName](/reference/datagate/datagate-common/i-schema-element-name.html))

Initializes a new instance of the  class with the specified XML container, XML element, and element name.

```cs
XmlElementConverter(XmlNode, XmlElement, ISchemaElementName)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [XmlNode](https://learn.microsoft.com/en-us/dotnet/api/system.xml.xmlnode?view=net-8.0) | container | The XML container.
| [XmlElement](https://learn.microsoft.com/en-us/dotnet/api/system.xml.xmlelement?view=net-8.0) | element | The XML element to convert.
| [ISchemaElementName](/reference/datagate/datagate-common/i-schema-element-name.html) | elementName | The name of the element.

## See Also
- [XmlElementConverter class](xml-element-converter.html)
