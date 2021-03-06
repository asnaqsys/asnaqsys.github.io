---
title: XmlInfoEventArgs.Message Field

Id: dcsXmlInfoEventArgsClassMessageField
TocParent: dcsXmlInfoEventArgsFields
TocOrder: 0

keywords: Message field
keywords: XmlInfoEventArgs.Message field
keywords: XML [DCS 16.0 events, feedback message
keywords: XML [DCS 16.0 event handler, feedback message
keywords: event handlers, feedback message

---

The **Message** field contains the text of a status report of an XML operation.
<pre class="prettyprint">        <span class="lang">[C#]</span>
 **public string Message** 
      </pre>
<pre class="prettyprint">        <span class="lang">[Visual Basic] </span>
 **public Shared Property Message As string** 
      </pre>
<pre class="prettyprint">        <span class="lang">[Visual RPG]</span>
 **BegProp Message Type(*string) Access(*Public) Shared(*Yes)<br />**    

         </pre>

## Field
Value

String. The message text of the event.
## Remarks

English-language text messages of **Message** provide feedback to users of [AdgFactory.ReadXml](adg-factory-class-read-xml-method2.html) and [IAdgObject.WriteXml](dcsIAdgObjectClassWriteXmlMethod2.html). See also [XmlInfoEventHandler](xml-info-event-handler-delegate.html).
## Requirements

**Namespace:** [ASNA.DataGate.Client](datagate-client-namespace.html) 

**Assembly:** ASNA DataGate Client

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
## See Also


[XmlInfoEventArgs Class](xml-info-event-args-class.html)
      <br />
[XmlInfoEventArgs Members](xml-info-event-args-members.html)
      <br />
[AdgFactory.ReadXml](adg-factory-class-read-xml-method2.html)
      <br />
[IAdgObject.WriteXml](dcsIAdgObjectClassWriteXmlMethod2.html)
      <br />
[XmlInfoEventHandler Delegate](xml-info-event-handler-delegate.html)
      <br />
[ASNA.DataGate.Client Namespace](datagate-client-namespace.html)

