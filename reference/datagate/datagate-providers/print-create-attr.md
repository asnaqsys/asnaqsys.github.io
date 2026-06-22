---
title: "PrintCreateAttr class"
description: "Represents the attributes for creating a print file. "
last_modified_at: 2024-08-09T17:25:07Z
---

Represents the attributes for creating a print file.

**Namespace:** ASNA.DataGate.Providers
**Assembly:** ASNA.QSys.DataGate.Client.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [Hashtable](https://learn.microsoft.com/en-us/dotnet/api/system.collections.hashtable?view=net-8.0)
<br>
<br>

## Remarks
This class encapsulates the properties and methods required to create a print file.
It includes properties such as the file name, the user data, and the device attributes.

<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [PrintCreateAttr()](print-create-attr-ctor.html#printcreateattr) | Initializes a new instance of the  class.

## Properties

| Type | Name | Description
| --- | --- | --- 
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | CheckFormatLevels | Gets or sets a value indicating whether format levels should be checked. |
| [PrintDevAttr](/reference/datagate/datagate-providers/print-dev-attr.html) | DevAttr | Gets or sets the device attributes. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | DocumentName | Gets or sets the name of the document. |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | ProcessMacros | Gets or sets a value indicating whether macros should be processed. |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | Prompt | Gets or sets a value indicating whether a prompt should be displayed. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | WaitForFile | Gets or sets the time to wait for the file to be created, in milliseconds. |

## Methods

| Signature | Description |
| --- | --- |
| [ReadXml](print-create-attr-readxml.html#void-readxml-xmlreader-reader)([XmlReader](https://learn.microsoft.com/en-us/dotnet/api/system.xml.xmlreader?view=net-8.0)) | Generates an object from its XML representation.
| [TryGetValue](print-create-attr-trygetvalue.html#bool-trygetvalue-string-key-object-value)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Object&](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | Gets the value associated with the specified key.
| [WriteXml](print-create-attr-writexml.html#void-writexml-xmlwriter-writer)([XmlWriter](https://learn.microsoft.com/en-us/dotnet/api/system.xml.xmlwriter?view=net-8.0)) | Converts the current instance into an XML string.

