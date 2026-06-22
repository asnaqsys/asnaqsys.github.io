---
title: "IStreamTransformerFactory interface.MakeDecoder Method"
description: "Creates a decoder for a given stream."
---

## Definition

**Namespace:** ASNA.DataGate.Providers  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Creates a decoder for a given stream.

<a id="stream-makedecoder-stream-istream"></a>
## Stream MakeDecoder(Stream istream)

Creates a decoder for a given stream.

```cs
Stream MakeDecoder(Stream istream)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Stream](https://learn.microsoft.com/en-us/dotnet/api/system.io.stream?view=net-8.0) | istream | The stream for which a decoder will be created.

#### Returns

| Type | Description
| --- | ---
| [Stream](https://learn.microsoft.com/en-us/dotnet/api/system.io.stream?view=net-8.0) | A stream that decodes the provided stream.

## See Also
- [IStreamTransformerFactory interface class](i-stream-transformer-factory.html)
