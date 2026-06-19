---
title: "IAdgObject interface.WriteXml Method"
description: "Writes the ADG object to an XML writer using the specified options."
---

## Definition

**Namespace:** ASNA.DataGate.Client  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Writes the ADG object to an XML writer using the specified options.

## Overloads

| Signature | Description |
| --- | --- |
| [WriteXml](#void-writexml-xmlwriter-writer-xmloptions-options)(void WriteXml(XmlWriter writer, XmlOptions options)) | Writes the ADG object to an XML writer using the specified options. |
| [WriteXml](#void-writexml-xmlwriter-writer-xmloptions-options-xmlcanceleventhandler-hndlr)(void WriteXml(XmlWriter writer, XmlOptions options, XmlCancelEventHandler hndlr)) | Writes the ADG object to an XML writer using the specified options and event handler. |
| [WriteXml](#void-writexml-xmlwriter-writer-xmloptions-options-xmlcanceleventhandler-hndlr-openfileadapterdelegate-fileopener)(void WriteXml(XmlWriter writer, XmlOptions options, XmlCancelEventHandler hndlr, OpenFileAdapterDelegate fileOpener)) | Writes the ADG object to an XML writer using the specified options, event handler, and file opener delegate. |

<a id="void-writexml-xmlwriter-writer-xmloptions-options"></a>
## void WriteXml(XmlWriter writer, XmlOptions options)

Writes the ADG object to an XML writer using the specified options.

#### Remarks
This method is used to write the ADG object to an XML writer using the specified options. The writer parameter specifies the XML writer to write to. The options parameter specifies the options to use when writing the XML, such as whether to include schema information or whether to indent the XML.This can be useful for serializing the object's state to XML.

```cs
void WriteXml(XmlWriter writer, XmlOptions options)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [XmlWriter](https://learn.microsoft.com/en-us/dotnet/api/system.xml.xmlwriter?view=net-8.0) | writer | The XML writer to write to.
| [XmlOptions](/reference/datagate/datagate-client/xml-options.html) | options | The options to use when writing the XML.

<a id="void-writexml-xmlwriter-writer-xmloptions-options-xmlcanceleventhandler-hndlr"></a>
## void WriteXml(XmlWriter writer, XmlOptions options, XmlCancelEventHandler hndlr)

Writes the ADG object to an XML writer using the specified options and event handler.

#### Remarks
This method is used to write the ADG object to an XML writer using the specified options and event handler. The writer parameter specifies the XML writer to write to. The options parameter specifies the options to use when writing the XML, such as whether to include schema information or whether to indent the XML.The hndlr parameter specifies the event handler for handling cancel events during the write operation. This can be useful for interrupting the write operation based on custom logic.

```cs
void WriteXml(XmlWriter writer, XmlOptions options, XmlCancelEventHandler hndlr)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [XmlWriter](https://learn.microsoft.com/en-us/dotnet/api/system.xml.xmlwriter?view=net-8.0) | writer | The XML writer to write to.
| [XmlOptions](/reference/datagate/datagate-client/xml-options.html) | options | The options to use when writing the XML.
| [XmlCancelEventHandler](/reference/datagate/datagate-client/xml-cancel-event-handler.html) | hndlr | The event handler for handling cancel events during the write operation.

<a id="void-writexml-xmlwriter-writer-xmloptions-options-xmlcanceleventhandler-hndlr-openfileadapterdelegate-fileopener"></a>
## void WriteXml(XmlWriter writer, XmlOptions options, XmlCancelEventHandler hndlr, OpenFileAdapterDelegate fileOpener)

Writes the ADG object to an XML writer using the specified options, event handler, and file opener delegate.

#### Remarks
This method is used to write the ADG object to an XML writer using the specified options, event handler, and file opener delegate. The writer parameter specifies the XML writer to write to. The options parameter specifies the options to use when writing the XML, such as whether to include schema information or whether to indent the XML.The hndlr parameter specifies the event handler for handling cancel events during the write operation. This can be useful for interrupting the write operation based on custom logic.The fileOpener parameter specifies the delegate for opening a file during the write operation. This can be useful for writing the XML to a specific file or stream.

```cs
void WriteXml(XmlWriter writer, XmlOptions options, XmlCancelEventHandler hndlr, OpenFileAdapterDelegate fileOpener)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [XmlWriter](https://learn.microsoft.com/en-us/dotnet/api/system.xml.xmlwriter?view=net-8.0) | writer | The XML writer to write to.
| [XmlOptions](/reference/datagate/datagate-client/xml-options.html) | options | The options to use when writing the XML.
| [XmlCancelEventHandler](/reference/datagate/datagate-client/xml-cancel-event-handler.html) | hndlr | The event handler for handling cancel events during the write operation.
| [OpenFileAdapterDelegate](/reference/datagate/datagate-client/open-file-adapter-delegate.html) | fileOpener | The delegate for opening a file during the write operation.

## See Also
- [IAdgObject interface class](i-adg-object.html)
