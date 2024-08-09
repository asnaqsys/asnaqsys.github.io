---
title: "IExchange5250 interface       | QSYS API Reference Guide"
description: "Provides an interface for exchanging 5250 data streams. "
last_modified_at: 2024-08-09T17:25:07Z
---

Provides an interface for exchanging 5250 data streams.

**Namespace:** ASNA.DataGate.Providers
**Assembly:** ASNA.QSys.DataGate.Client.dll

**Extends:** doesn't extend any other interfaces.
<br>
<br>

## Methods

| Signature | Description |
| --- | --- |
| [CompleteOpen](#void-completeopenint-peeraltcodepageid)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Completes the opening of a peer with a specific code page ID.
| [Exchange5250DS](#void-exchange5250dsint-ibegin-byte--ainds-int-indslength-byte--aoutds-int32-outdslength-byte-telnetflags)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Byte\[\]&](https://docs.microsoft.com/en-us/dotnet/api/system.byte), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Byte\[\]&](https://docs.microsoft.com/en-us/dotnet/api/system.byte), [Int32&](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Byte&](https://docs.microsoft.com/en-us/dotnet/api/system.byte)) | Exchanges 5250 data streams.
| [GetDeviceInfo](#void-getdeviceinfostring-devicesn-string-deviceclient-string-deviceserver)([String&](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String&](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String&](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Gets the device information.

### void CompleteOpen([int peerAltCodePageID](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Completes the opening of a peer with a specific code page ID.

```cs
void CompleteOpen(int peerAltCodePageID)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | peerAltCodePageID | The alternative code page ID of the peer.

### void Exchange5250DS([int iBegin](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [Byte\[\]& aInDs](https://docs.microsoft.com/en-us/dotnet/api/system.byte), [int InDsLength](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [Byte\[\]& aOutDs](https://docs.microsoft.com/en-us/dotnet/api/system.byte), [Int32& OutDsLength](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Byte& TelnetFlags](https://docs.microsoft.com/en-us/dotnet/api/system.byte))

Exchanges 5250 data streams.

```cs
void Exchange5250DS(int iBegin, Byte[]& aInDs, int InDsLength, Byte[]& aOutDs, Int32& OutDsLength, Byte& TelnetFlags)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | iBegin | The starting point for the exchange.
| [Byte\[\]&](https://docs.microsoft.com/en-us/dotnet/api/system.byte) | aInDs | The input data stream.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | InDsLength | The length of the input data stream.
| [Byte\[\]&](https://docs.microsoft.com/en-us/dotnet/api/system.byte) | aOutDs | The output data stream.
| [Int32&](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | OutDsLength | The length of the output data stream.
| [Byte&](https://docs.microsoft.com/en-us/dotnet/api/system.byte) | TelnetFlags | The telnet flags for the exchange.

### void GetDeviceInfo([String& deviceSN](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String& deviceClient](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String& deviceServer](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Gets the device information.

```cs
void GetDeviceInfo(String& deviceSN, String& deviceClient, String& deviceServer)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String&](https://docs.microsoft.com/en-us/dotnet/api/system.string) | deviceSN | The device serial number.
| [String&](https://docs.microsoft.com/en-us/dotnet/api/system.string) | deviceClient | The device client.
| [String&](https://docs.microsoft.com/en-us/dotnet/api/system.string) | deviceServer | The device server.
