---
title: "AdgEnumerator Delegate"
description: "Represents a method that handles an IAdgObject."
---

## Definition

**Namespace:** ASNA.DataGate.Client  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Represents a method that handles an IAdgObject.

```csharp
public delegate void AdgEnumerator(IAdgObject iAdgObject)
```

#### Parameters

| Type | Parameter name | Description |
| --- | --- | --- |
| [IAdgObject](/reference/datagate/datagate-client/i-adg-object.html) | iAdgObject | The IAdgObject to be handled. |

## Remarks
This delegate provides a reference to a method that takes an IAdgObject as a parameter. Use it to enumerate or perform operations on an IAdgObject instance; the specific work is determined by the target method implementation.

## See Also
- [IAdgObject](/reference/datagate/datagate-client/i-adg-object.html)
- [ASNA.DataGate.Client Namespace](/reference/datagate/datagate-client/landing-page-namespace.html)
