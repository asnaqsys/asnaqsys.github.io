---
title: "XmlCancelEventHandler Delegate"
description: "Represents the method that will handle an event when an XML operation can be canceled."
---

## Definition

**Namespace:** ASNA.DataGate.Client  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Handles an event when an XML operation can be canceled.

```csharp
public delegate void XmlCancelEventHandler(object o, XmlCancelEventArgs args)
```

#### Parameters

| Type | Parameter name | Description |
| --- | --- | --- |
| [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) | o | The source of the event. |
| [XmlCancelEventArgs](/reference/datagate/datagate-client/xml-cancel-event-args.html) | args | The XmlCancelEventArgs instance containing the event data. |

## Remarks
Use this delegate for event handlers that can cancel an ongoing XML operation based on the information provided in the XmlCancelEventArgs.

## See Also
- [XmlCancelEventArgs](/reference/datagate/datagate-client/xml-cancel-event-args.html)
- [ASNA.DataGate.Client Namespace](/reference/datagate/datagate-client/landing-page-namespace.html)
