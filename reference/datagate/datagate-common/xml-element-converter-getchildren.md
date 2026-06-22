---
title: "XmlElementConverter.GetChildren Method"
description: "Gets all child elements of the current XmlElement with the specified name and namespace."
---

## Definition

**Namespace:** ASNA.DataGate.Common  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Gets all child elements of the current XmlElement with the specified name and namespace.

<a id="xmlnodelist-getchildren-string-childelementname-string-childelementnamespace"></a>
## XmlNodeList GetChildren(string childElementName, string childElementNamespace)

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

## See Also
- [XmlElementConverter class](xml-element-converter.html)
