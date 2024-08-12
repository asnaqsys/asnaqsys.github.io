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
