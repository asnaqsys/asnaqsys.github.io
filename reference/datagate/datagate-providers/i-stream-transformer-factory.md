---
title: "IStreamTransformerFactory interface"
description: "Provides an interface for creating encoders and decoders for streams. "
last_modified_at: 2024-08-09T16:18:40Z
---

Provides an interface for creating encoders and decoders for streams.

**Namespace:** ASNA.DataGate.Providers
**Assembly:** ASNA.QSys.DataGate.Client.dll

**Extends:** doesn't extend any other interfaces.
<br>
<br>

## Methods

| Signature | Description |
| --- | --- |
| [MakeDecoder](#stream-makedecoderstream-istream)([Stream](https://learn.microsoft.com/en-us/dotnet/api/system.io.stream?view=net-8.0)) | Creates a decoder for a given stream.
| [MakeEncoder](#stream-makeencoderstream-ostream)([Stream](https://learn.microsoft.com/en-us/dotnet/api/system.io.stream?view=net-8.0)) | Creates an encoder for a given stream.

### Stream MakeDecoder([Stream istream](https://learn.microsoft.com/en-us/dotnet/api/system.io.stream?view=net-8.0))

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

### Stream MakeEncoder([Stream ostream](https://learn.microsoft.com/en-us/dotnet/api/system.io.stream?view=net-8.0))

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
