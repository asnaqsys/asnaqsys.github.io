---
title: "XmlElementConverter.GetChildrenOrThrow Method"
description: "Gets all child elements of the current XmlElement with the specified name and namespace."
---

## Definition

**Namespace:** ASNA.DataGate.Common  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Gets all child elements of the current XmlElement with the specified name and namespace.

<a id="ienumerable-xmlelement-getchildrenorthrow-string-childname-string-childnamespace"></a>
## IEnumerable\<XmlElement\> GetChildrenOrThrow(string childName, string childNamespace)

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

## See Also
- [XmlElementConverter class](xml-element-converter.html)
