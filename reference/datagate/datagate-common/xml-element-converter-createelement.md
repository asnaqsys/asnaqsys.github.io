---
title: "XmlElementConverter.CreateElement Method"
description: "Creates a new XmlElement with the specified name and appends it to the parent node."
---

## Definition

**Namespace:** ASNA.DataGate.Common  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Creates a new XmlElement with the specified name and appends it to the parent node.

<a id="xmlelement-createelement-bool-addxmlnsattr"></a>
## XmlElement CreateElement(bool addXmlnsAttr)

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

## See Also
- [XmlElementConverter class](xml-element-converter.html)
