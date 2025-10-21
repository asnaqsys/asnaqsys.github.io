---
title: "AdgObserver Delegate"
description: "Represents a method that processes a string."
---

## Definition

**Namespace:** ASNA.DataGate.Client  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Represents a method that processes a string.

```csharp
public delegate void AdgObserver(string text)
```

#### Parameters

| Type | Parameter name | Description |
| --- | --- | --- |
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | text | The string to be processed. |

## Remarks
This delegate provides a reference to a method that takes a string as a parameter. The target method determines how the string is processed (for example, logging, parsing, or transforming).

## See Also
- [ASNA.DataGate.Client Namespace](/reference/datagate/datagate-client/landing-page-namespace.html)
