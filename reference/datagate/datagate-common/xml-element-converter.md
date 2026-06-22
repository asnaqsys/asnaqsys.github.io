---
title: "XmlElementConverter class"
description: "Provides methods for converting between XmlElement objects and their string, boolean, and child element representations. "
last_modified_at: 2024-08-09T17:25:07Z
---

Provides methods for converting between XmlElement objects and their string, boolean, and child element representations.

**Namespace:** ASNA.DataGate.Common
**Assembly:** ASNA.QSys.DataGate.Client.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [XmlElementConverter](xml-element-converter-ctor.html#xmlelementconverter-xmlnode-ischemaelementname)([XmlNode](https://learn.microsoft.com/en-us/dotnet/api/system.xml.xmlnode?view=net-8.0), [ISchemaElementName](/reference/datagate/datagate-common/i-schema-element-name.html)) | Initializes a new instance of the  class with the specified XML container and element name.
| [XmlElementConverter](xml-element-converter-ctor.html#xmlelementconverter-xmlnode-xmlelement-ischemaelementname)([XmlNode](https://learn.microsoft.com/en-us/dotnet/api/system.xml.xmlnode?view=net-8.0), [XmlElement](https://learn.microsoft.com/en-us/dotnet/api/system.xml.xmlelement?view=net-8.0), [ISchemaElementName](/reference/datagate/datagate-common/i-schema-element-name.html)) | Initializes a new instance of the  class with the specified XML container, XML element, and element name.

## Properties

| Type | Name | Description
| --- | --- | --- 
| [XmlDocument](https://learn.microsoft.com/en-us/dotnet/api/system.xml.xmldocument?view=net-8.0) | Doc | Gets the XmlDocument that the current XmlElement belongs to. |
| [XmlElement](https://learn.microsoft.com/en-us/dotnet/api/system.xml.xmlelement?view=net-8.0) | Element | Gets or sets the XmlElement that is being converted. |
| [ISchemaElementName](/reference/datagate/datagate-common/i-schema-element-name.html) | ElementName | Gets the name of the current XmlElement. |
| [XmlNode](https://learn.microsoft.com/en-us/dotnet/api/system.xml.xmlnode?view=net-8.0) | Parent | Gets the parent XmlNode of the current XmlElement. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | XsdFalse | Represents the string "false" in XSD format. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | XsdTrue | Represents the string "true" in XSD format. |

## Methods

| Signature | Description |
| --- | --- |
| [CreateElement](xml-element-converter-createelement.html#xmlelement-createelement-bool-addxmlnsattr)([Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Creates a new XmlElement with the specified name and appends it to the parent node.
| [GetAttribute](xml-element-converter-getattribute.html#string-getattribute-string-name)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Gets the value of the attribute with the specified name from the current XmlElement.
| [GetAttribute](xml-element-converter-getattribute.html#string-getattribute-string-name-object-defaultvalue)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | Gets the value of the attribute with the specified name from the current XmlElement. If the attribute does not exist, returns the specified default value.
| [GetChildCount](xml-element-converter-getchildcount.html#int-getchildcount-string-childelementname-string-childelementnamespace)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Gets the number of child elements of the current XmlElement with the specified name and namespace.
| [GetChildren](xml-element-converter-getchildren.html#xmlnodelist-getchildren-string-childelementname-string-childelementnamespace)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Gets all child elements of the current XmlElement with the specified name and namespace.
| [GetChildrenOrThrow](xml-element-converter-getchildrenorthrow.html#ienumerable-xmlelement-getchildrenorthrow-string-childname-string-childnamespace)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Gets all child elements of the current XmlElement with the specified name and namespace. If the current element is null, throws an InvalidOperationException.
| [GetDocumentOrThrow()](xml-element-converter-getdocumentorthrow.html#xmldocument-getdocumentorthrow) | Gets the XmlDocument that the current XmlElement belongs to. If the document is null, throws an InvalidOperationException.
| [GetElementOrThrow()](xml-element-converter-getelementorthrow.html#xmlelement-getelementorthrow) | Gets the XmlElement that is being converted. If the element is null, throws an InvalidOperationException.
| [GetElementText()](xml-element-converter-getelementtext.html#string-getelementtext) | Gets the text of the current XmlElement.
| [GetElementText](xml-element-converter-getelementtext.html#string-getelementtext-xmlelement-element)([XmlElement](https://learn.microsoft.com/en-us/dotnet/api/system.xml.xmlelement?view=net-8.0)) | Gets the text of the specified XmlElement.
| [GetFirstElement()](xml-element-converter-getfirstelement.html#void-getfirstelement) | Gets the first child element of the parent node that matches the specified element name and namespace. The element is stored in the Element property of this class.
| [GetParentOrThrow()](xml-element-converter-getparentorthrow.html#xmlnode-getparentorthrow) | Gets the parent XmlNode of the current XmlElement. If the parent is null, throws an InvalidOperationException.
| [GetXsdBool](xml-element-converter-getxsdbool.html#string-getxsdbool-bool-value)([Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Converts a boolean value to its equivalent string representation in XSD format.
| [GetXsdBooleanAttribute](xml-element-converter-getxsdbooleanattribute.html#bool-getxsdbooleanattribute-string-name-bool-defaultvalue)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Gets the value of the attribute with the specified name from the current XmlElement and converts it to a boolean. If the attribute does not exist, returns the specified default value.
| [HasAttribute](xml-element-converter-hasattribute.html#bool-hasattribute-string-name)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Determines whether the current XmlElement has an attribute with the specified name.
| [SetAttribute](xml-element-converter-setattribute.html#void-setattribute-string-name-object-val)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | Sets the value of the attribute with the specified name in the current XmlElement.
| [SetElementName](xml-element-converter-setelementname.html#void-setelementname-ischemaelementname-name)([ISchemaElementName](/reference/datagate/datagate-common/i-schema-element-name.html)) | Sets the name of the current XmlElement to the specified value.
| [SetElementText](xml-element-converter-setelementtext.html#void-setelementtext-string-text)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Sets the text of the current XmlElement to the specified value.

