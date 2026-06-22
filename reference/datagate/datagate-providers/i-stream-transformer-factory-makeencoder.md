---
title: "IStreamTransformerFactory interface.MakeEncoder Method"
description: "Creates an encoder for a given stream."
---

## Definition

**Namespace:** ASNA.DataGate.Providers  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Creates an encoder for a given stream.

<a id="stream-makeencoder-stream-ostream"></a>
## Stream MakeEncoder(Stream ostream)

Creates an encoder for a given stream.

```cs
Stream MakeEncoder(Stream ostream)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Stream](https://learn.microsoft.com/en-us/dotnet/api/system.io.stream?view=net-8.0) | ostream | The stream for which an encoder will be created.

#### Returns

| Type | Description
| --- | ---
| [Stream](https://learn.microsoft.com/en-us/dotnet/api/system.io.stream?view=net-8.0) | A stream that encodes the provided stream.

## See Also
- [IStreamTransformerFactory interface class](i-stream-transformer-factory.html)
