---
title: "IExchange5250 interface       | QSYS API Reference Guide"
description: "Provides an interface for exchanging 5250 data streams. "
last_modified_at: 2024-08-08T21:41:32Z
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

### void CompleteOpen([int peerAltCodePageID](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Completes the opening of a peer with a specific code page ID.

```cs
void CompleteOpen(int peerAltCodePageID)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | peerAltCodePageID | The alternative code page ID of the peer.
