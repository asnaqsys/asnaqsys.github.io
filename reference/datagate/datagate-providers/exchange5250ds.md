---
title: "Exchange5250DS Delegate"
description: "Represents a method that exchanges 5250 data streams."
---

## Definition

**Namespace:** ASNA.DataGate.Providers  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Represents a method that exchanges 5250 data streams.

```csharp
public delegate void Exchange5250DS(
    int iBegin,
    ref byte[] aInDs,
    int InDsLength,
    out byte[] aOutDs,
    out int OutDsLength,
    out byte TelnetFlags)
```

#### Parameters

| Type | Parameter name | Description |
| --- | --- | --- |
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | iBegin | The starting point for the exchange. |
| [Byte](https://docs.microsoft.com/en-us/dotnet/api/system.byte)[] | aInDs | The input data stream. |
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | InDsLength | The length of the input data stream. |
| [Byte](https://docs.microsoft.com/en-us/dotnet/api/system.byte)[] | aOutDs | The output data stream. |
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | OutDsLength | The length of the output data stream. |
| [Byte](https://docs.microsoft.com/en-us/dotnet/api/system.byte) | TelnetFlags | The telnet flags for the exchange. |

## Remarks
Use this delegate to encapsulate the exchange of 5250 data streams, including both inbound and outbound buffers and associated telnet flags.

## See Also
- [ASNA.DataGate.Providers Namespace](/reference/datagate/datagate-providers/landing-page-namespace.html)
