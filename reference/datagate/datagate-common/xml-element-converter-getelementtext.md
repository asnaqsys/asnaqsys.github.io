---
title: "XmlElementConverter.GetElementText Method"
description: "Gets the text of the current XmlElement."
---

## Definition

**Namespace:** ASNA.DataGate.Common  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Gets the text of the current XmlElement.

## Overloads

| Signature | Description |
| --- | --- |
| [GetElementText](#string-getelementtext)(string GetElementText()) | Gets the text of the current XmlElement. |
| [GetElementText](#string-getelementtext-xmlelement-element)(string GetElementText(XmlElement element)) | Gets the text of the specified XmlElement. |

<a id="string-getelementtext"></a>
## string GetElementText()

Gets the text of the current XmlElement.

```cs
string GetElementText()
```

<a id="string-getelementtext-xmlelement-element"></a>
## string GetElementText(XmlElement element)

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

## See Also
- [XmlElementConverter class](xml-element-converter.html)
