---
title: "DbXmlNameConverter class      | QSYS API Reference Guide"
description: "This class is a filter used in the XML transforms ExportToXml.xslt and ImportToXml.xslt.  Encode() takes an arbitrary string and returns an XML-compli"
last_modified_at: 2024-08-09T17:25:07Z
---

This class is a filter used in the XML transforms ExportToXml.xslt and
ImportToXml.xslt.  Encode() takes an arbitrary string and returns an
XML-compliant Name string.  For example, "$ITEMTEST" is returned as
"_x0024_ITEMTEST".  Decode() performs the inverse function.

**Namespace:** ASNA.DataGate.Client.CopyData
**Assembly:** ASNA.QSys.DataGate.Client.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>

## Properties

| Type | Name | Description
| --- | --- | --- 
| [DbXmlNameConverter](/reference/datagate/datagate-client/db-xml-name-converter.html) | Default | Gets the default instance of the  class. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | Urn | Defines the Uniform Resource Name (URN) for the  class. |

## Methods

| Signature | Description |
| --- | --- |
| [Decode](#string-decodexpathnavigator-context-string-name)([XPathNavigator](https://learn.microsoft.com/en-us/dotnet/api/system.xml.xpath.xpathnavigator?view=net-8.0), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Decodes the provided XML-compliant string back into its original name.
| [Encode](#string-encodexpathnavigator-context-string-name)([XPathNavigator](https://learn.microsoft.com/en-us/dotnet/api/system.xml.xpath.xpathnavigator?view=net-8.0), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Encodes the provided name into an XML-compliant string.

### string Decode([XPathNavigator context](https://learn.microsoft.com/en-us/dotnet/api/system.xml.xpath.xpathnavigator?view=net-8.0), [string name](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

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

### string Encode([XPathNavigator context](https://learn.microsoft.com/en-us/dotnet/api/system.xml.xpath.xpathnavigator?view=net-8.0), [string name](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

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
