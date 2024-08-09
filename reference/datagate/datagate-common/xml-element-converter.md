---
title: "XmlElementConverter class     | QSYS API Reference Guide"
description: "Provides methods for converting between XmlElement objects and their string, boolean, and child element representations. "
last_modified_at: 2024-08-09T16:18:40Z
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
| [XmlElementConverter](#xmlelementconverterxmlnode-ischemaelementname)([XmlNode](https://learn.microsoft.com/en-us/dotnet/api/system.xml.xmlnode?view=net-8.0), [ISchemaElementName](/reference/datagate/datagate-common/i-schema-element-name.html)) | Initializes a new instance of the  class with the specified XML container and element name.
| [XmlElementConverter](#xmlelementconverterxmlnode-xmlelement-ischemaelementname)([XmlNode](https://learn.microsoft.com/en-us/dotnet/api/system.xml.xmlnode?view=net-8.0), [XmlElement](https://learn.microsoft.com/en-us/dotnet/api/system.xml.xmlelement?view=net-8.0), [ISchemaElementName](/reference/datagate/datagate-common/i-schema-element-name.html)) | Initializes a new instance of the  class with the specified XML container, XML element, and element name.

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
| [CreateElement](#xmlelement-createelementbool-addxmlnsattr)([Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Creates a new XmlElement with the specified name and appends it to the parent node.
| [GetAttribute](#string-getattributestring-name)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Gets the value of the attribute with the specified name from the current XmlElement.
| [GetAttribute](#string-getattributestring-name-object-defaultvalue)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | Gets the value of the attribute with the specified name from the current XmlElement. If the attribute does not exist, returns the specified default value.
| [GetChildCount](#int-getchildcountstring-childelementname-string-childelementnamespace)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Gets the number of child elements of the current XmlElement with the specified name and namespace.
| [GetChildren](#xmlnodelist-getchildrenstring-childelementname-string-childelementnamespace)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Gets all child elements of the current XmlElement with the specified name and namespace.
| [GetChildrenOrThrow](#ienumerable-xmlelement-getchildrenorthrowstring-childname-string-childnamespace)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Gets all child elements of the current XmlElement with the specified name and namespace. If the current element is null, throws an InvalidOperationException.
| [GetDocumentOrThrow()](#xmldocument-getdocumentorthrow) | Gets the XmlDocument that the current XmlElement belongs to. If the document is null, throws an InvalidOperationException.
| [GetElementOrThrow()](#xmlelement-getelementorthrow) | Gets the XmlElement that is being converted. If the element is null, throws an InvalidOperationException.
| [GetElementText()](#string-getelementtext) | Gets the text of the current XmlElement.
| [GetElementText](#string-getelementtextxmlelement-element)([XmlElement](https://learn.microsoft.com/en-us/dotnet/api/system.xml.xmlelement?view=net-8.0)) | Gets the text of the specified XmlElement.
| [GetFirstElement()](#void-getfirstelement) | Gets the first child element of the parent node that matches the specified element name and namespace. The element is stored in the Element property of this class.
| [GetParentOrThrow()](#xmlnode-getparentorthrow) | Gets the parent XmlNode of the current XmlElement. If the parent is null, throws an InvalidOperationException.
| [GetXsdBool](#string-getxsdboolbool-value)([Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Converts a boolean value to its equivalent string representation in XSD format.
| [GetXsdBooleanAttribute](#bool-getxsdbooleanattributestring-name-bool-defaultvalue)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Gets the value of the attribute with the specified name from the current XmlElement and converts it to a boolean. If the attribute does not exist, returns the specified default value.
| [HasAttribute](#bool-hasattributestring-name)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Determines whether the current XmlElement has an attribute with the specified name.
| [SetAttribute](#void-setattributestring-name-object-val)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | Sets the value of the attribute with the specified name in the current XmlElement.
| [SetElementName](#void-setelementnameischemaelementname-name)([ISchemaElementName](/reference/datagate/datagate-common/i-schema-element-name.html)) | Sets the name of the current XmlElement to the specified value.
| [SetElementText](#void-setelementtextstring-text)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Sets the text of the current XmlElement to the specified value.

### XmlElement CreateElement([bool addXmlnsAttr](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Creates a new XmlElement with the specified name and appends it to the parent node.

```cs
XmlElement CreateElement(bool addXmlnsAttr)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | addXmlnsAttr | If true, adds an xmlns attribute with the namespace of the element.

#### Returns

| Type | Description
| --- | ---
| [XmlElement](https://learn.microsoft.com/en-us/dotnet/api/system.xml.xmlelement?view=net-8.0) | The created XmlElement.

### string GetAttribute([string name](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Gets the value of the attribute with the specified name from the current XmlElement.

```cs
string GetAttribute(string name)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | name | The name of the attribute.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The value of the attribute.

### string GetAttribute([string name](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [object defaultValue](https://docs.microsoft.com/en-us/dotnet/api/system.object))

Gets the value of the attribute with the specified name from the current XmlElement. If the attribute does not exist, returns the specified default value.

```cs
string GetAttribute(string name, object defaultValue)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | name | The name of the attribute.
| [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) | defaultValue | The value to return if the attribute does not exist.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The value of the attribute, or the default value if the attribute does not exist.

### int GetChildCount([string childElementName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string childElementNamespace](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Gets the number of child elements of the current XmlElement with the specified name and namespace.

```cs
int GetChildCount(string childElementName, string childElementNamespace)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | childElementName | The name of the child elements to count.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | childElementNamespace | The namespace of the child elements to count.

#### Returns

| Type | Description
| --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | The number of child elements with the specified name and namespace.

### XmlNodeList GetChildren([string childElementName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string childElementNamespace](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Gets all child elements of the current XmlElement with the specified name and namespace.

```cs
XmlNodeList GetChildren(string childElementName, string childElementNamespace)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | childElementName | The name of the child elements to get.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | childElementNamespace | The namespace of the child elements to get.

#### Returns

| Type | Description
| --- | ---
| [XmlNodeList](https://learn.microsoft.com/en-us/dotnet/api/system.xml.xmlnodelist?view=net-8.0) | A collection of child elements with the specified name and namespace, or null if the current element is null.

### IEnumerable\<XmlElement\> GetChildrenOrThrow([string childName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string childNamespace](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Gets all child elements of the current XmlElement with the specified name and namespace. If the current element is null, throws an InvalidOperationException.


#### Remarks
Use this in cases where GetChildren() should never return null, i.e., when Element is not null.

```cs
IEnumerable<XmlElement> GetChildrenOrThrow(string childName, string childNamespace)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | childName | The name of the child elements to get.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | childNamespace | The namespace of the child elements to get.

#### Returns

| Type | Description
| --- | ---
| [IEnumerable`1](https://learn.microsoft.com/en-us/dotnet/api/system.collections.generic.ienumerable-1?view=net-8.0) | A collection of child elements with the specified name and namespace.

### XmlDocument GetDocumentOrThrow()

Gets the XmlDocument that the current XmlElement belongs to. If the document is null, throws an InvalidOperationException.

```cs
XmlDocument GetDocumentOrThrow()
```

### XmlElement GetElementOrThrow()

Gets the XmlElement that is being converted. If the element is null, throws an InvalidOperationException.

```cs
XmlElement GetElementOrThrow()
```

### string GetElementText()

Gets the text of the current XmlElement.

```cs
string GetElementText()
```

### string GetElementText([XmlElement element](https://learn.microsoft.com/en-us/dotnet/api/system.xml.xmlelement?view=net-8.0))

Gets the text of the specified XmlElement.

```cs
string GetElementText(XmlElement element)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [XmlElement](https://learn.microsoft.com/en-us/dotnet/api/system.xml.xmlelement?view=net-8.0) | element | The XmlElement to get the text from.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The text of the XmlElement, or an empty string if the element has no text.

### void GetFirstElement()

Gets the first child element of the parent node that matches the specified element name and namespace. The element is stored in the Element property of this class.

```cs
void GetFirstElement()
```

### XmlNode GetParentOrThrow()

Gets the parent XmlNode of the current XmlElement. If the parent is null, throws an InvalidOperationException.

```cs
XmlNode GetParentOrThrow()
```

### string GetXsdBool([bool value](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Converts a boolean value to its equivalent string representation in XSD format.

```cs
string GetXsdBool(bool value)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | value | The boolean value to convert.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The string representation of the boolean value in XSD format.

### bool GetXsdBooleanAttribute([string name](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [bool defaultValue](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Gets the value of the attribute with the specified name from the current XmlElement and converts it to a boolean. If the attribute does not exist, returns the specified default value.

```cs
bool GetXsdBooleanAttribute(string name, bool defaultValue)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | name | The name of the attribute.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | defaultValue | The value to return if the attribute does not exist.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | The boolean value of the attribute, or the default value if the attribute does not exist.

### bool HasAttribute([string name](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Determines whether the current XmlElement has an attribute with the specified name.

```cs
bool HasAttribute(string name)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | name | The name of the attribute.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | true if the current XmlElement has an attribute with the specified name; otherwise, false.

### void SetAttribute([string name](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [object val](https://docs.microsoft.com/en-us/dotnet/api/system.object))

Sets the value of the attribute with the specified name in the current XmlElement.

```cs
void SetAttribute(string name, object val)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | name | The name of the attribute.
| [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) | val | The value to set for the attribute.

### void SetElementName([ISchemaElementName name](/reference/datagate/datagate-common/i-schema-element-name.html))

Sets the name of the current XmlElement to the specified value.

```cs
void SetElementName(ISchemaElementName name)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [ISchemaElementName](/reference/datagate/datagate-common/i-schema-element-name.html) | name | The new name for the current XmlElement.

### void SetElementText([string text](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Sets the text of the current XmlElement to the specified value.

```cs
void SetElementText(string text)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | text | The value to set as the text of the current XmlElement.
