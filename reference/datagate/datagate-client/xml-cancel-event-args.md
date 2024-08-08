---
title: "XmlCancelEventArgs class      | QSYS API Reference Guide"
description: "Provides data for the XmlCancelEvent event. "
last_modified_at: 2024-08-08T21:41:32Z
---

Provides data for the XmlCancelEvent event.

**Namespace:** ASNA.DataGate.Client
**Assembly:** ASNA.QSys.DataGate.Client.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [EventArgs](https://learn.microsoft.com/en-us/dotnet/api/system.eventargs?view=net-8.0)
<br>
<br>

## Remarks
This class contains information about an event that is raised when an XML operation is cancelled. 
It includes properties for getting the message associated with the event, the type of the event, 
any exception that occurred, and whether the operation should be cancelled. 
This can be useful for handling errors or interruptions during XML operations.

<br>
<br>

## Properties

| Type | Name | Description
| --- | --- | --- 
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | Cancel | Gets or sets a value indicating whether the XML event should be cancelled. |
| [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception) | Exception | Gets or sets the exception associated with the XML event. |
| [IEnumerable\<Object\>](https://learn.microsoft.com/en-us/dotnet/api/system.collections.generic.ienumerable-1?view=net-8.0) | ExtendedInfo | Gets the extended information for the XML event. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | Message | Gets the formatted message for the XML event. |
| [XmlInfoMsgType](/reference/datagate/datagate-client/xml-info-msg-type.html) | MessageID | Gets or sets the message ID for the XML event. |
| [XmlInfoEventType](/reference/datagate/datagate-client/xml-info-event-type.html) | Type | Gets or sets the type of the XML event. |

## Methods

| Signature | Description |
| --- | --- |
| [ToString()](#string-tostring) | Returns a string that represents the current object.

### string ToString()

Returns a string that represents the current object.


#### Remarks
This method overrides the base ToString method and returns the Message property of the XmlCancelEventArgs object. The Message property contains a formatted string that represents the details of the event. This can be useful for logging or displaying detailed information about the event.

```cs
string ToString()
```
