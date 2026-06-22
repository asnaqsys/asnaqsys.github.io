---
title: "XmlElementConverter.GetChildCount Method"
description: "Gets the number of child elements of the current XmlElement with the specified name and namespace."
---

## Definition

**Namespace:** ASNA.DataGate.Common  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Gets the number of child elements of the current XmlElement with the specified name and namespace.

<a id="int-getchildcount-string-childelementname-string-childelementnamespace"></a>
## int GetChildCount(string childElementName, string childElementNamespace)

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

## See Also
- [XmlElementConverter class](xml-element-converter.html)
