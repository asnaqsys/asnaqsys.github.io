---
title: "DbXmlNameConverter class"
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
| [Decode](db-xml-name-converter-decode.html#string-decode-xpathnavigator-context-string-name)([XPathNavigator](https://learn.microsoft.com/en-us/dotnet/api/system.xml.xpath.xpathnavigator?view=net-8.0), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Decodes the provided XML-compliant string back into its original name.
| [Encode](db-xml-name-converter-encode.html#string-encode-xpathnavigator-context-string-name)([XPathNavigator](https://learn.microsoft.com/en-us/dotnet/api/system.xml.xpath.xpathnavigator?view=net-8.0), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Encodes the provided name into an XML-compliant string.

