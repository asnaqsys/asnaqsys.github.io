---
title: "DbXmlNameConverter.Decode Method"
description: "Decodes the provided XML-compliant string back into its original name."
---

## Definition

**Namespace:** ASNA.DataGate.Client.CopyData  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Decodes the provided XML-compliant string back into its original name.

<a id="string-decode-xpathnavigator-context-string-name"></a>
## string Decode(XPathNavigator context, string name)

Decodes the provided XML-compliant string back into its original name.

#### Remarks
This method uses the  method to perform the actual decoding.Before the decoding, it checks if the provided context is null. If it is, an  is thrown.The  method uses the  method to decode the name, and handles any exceptions that might be thrown during the decoding.

```cs
string Decode(XPathNavigator context, string name)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [XPathNavigator](https://learn.microsoft.com/en-us/dotnet/api/system.xml.xpath.xpathnavigator?view=net-8.0) | context | The  context in which the decoding is performed.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | name | The XML-compliant string to be decoded.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The original name that was encoded into the provided XML-compliant string.

## See Also
- [DbXmlNameConverter class](db-xml-name-converter.html)
