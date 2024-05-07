---
title: IStreamTransformerFactory interface
---

Provides methods for creating encoder and decoder streams.

**Namespace:** ASNA.DataGate.Providers
**Assembly:** ASNA.QSys.DataGate.Client.dll

**Inheritance:** 
<br>
<br>

## Methods

| Signature | Description |
| --- | --- |
| [MakeEncoder](#makeencoder-stream-)([Stream](https://learn.microsoft.com/en-us/dotnet/api/system.io.stream?view=net-8.0)) | Creates an encoder stream using the provided output stream.
| [MakeDecoder](#makedecoder-stream-)([Stream](https://learn.microsoft.com/en-us/dotnet/api/system.io.stream?view=net-8.0)) | Creates a decoder stream using the provided input stream.

### Stream MakeEncoder([Stream ostream](https://learn.microsoft.com/en-us/dotnet/api/system.io.stream?view=net-8.0))

Creates an encoder stream using the provided output stream.

```cs
Stream MakeEncoder(Stream ostream)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Stream](https://learn.microsoft.com/en-us/dotnet/api/system.io.stream?view=net-8.0) | ostream | 

#### Returns

| Type | Description
| --- | ---
| [Stream](https://learn.microsoft.com/en-us/dotnet/api/system.io.stream?view=net-8.0) | A stream that encodes data.

### Stream MakeDecoder([Stream istream](https://learn.microsoft.com/en-us/dotnet/api/system.io.stream?view=net-8.0))

Creates a decoder stream using the provided input stream.

```cs
Stream MakeDecoder(Stream istream)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Stream](https://learn.microsoft.com/en-us/dotnet/api/system.io.stream?view=net-8.0) | istream | 

#### Returns

| Type | Description
| --- | ---
| [Stream](https://learn.microsoft.com/en-us/dotnet/api/system.io.stream?view=net-8.0) | A stream that decodes data.