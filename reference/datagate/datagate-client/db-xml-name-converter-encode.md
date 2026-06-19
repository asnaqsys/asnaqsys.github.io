---
title: "DbXmlNameConverter.Encode Method"
description: "Encodes the provided name into an XML-compliant string."
---

## Definition

**Namespace:** ASNA.DataGate.Client.CopyData  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Encodes the provided name into an XML-compliant string.

<a id="string-encode-xpathnavigator-context-string-name"></a>
## string Encode(XPathNavigator context, string name)

Encodes the provided name into an XML-compliant string.

#### Remarks
This method uses the  method to perform the actual encoding.Before the encoding, it checks if the provided context is null. If it is, an  is thrown.The  method uses the  method to encode the name, and handles any exceptions that might be thrown during the encoding.

```cs
string Encode(XPathNavigator context, string name)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [XPathNavigator](https://learn.microsoft.com/en-us/dotnet/api/system.xml.xpath.xpathnavigator?view=net-8.0) | context | The  context in which the encoding is performed.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | name | The name to be encoded.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | An XML-compliant string representation of the provided name.

## See Also
- [DbXmlNameConverter class](db-xml-name-converter.html)
