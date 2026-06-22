---
title: "IOpenAccessReader interface.Read Method"
description: "Reads a sequence of bytes from the channel into the specified buffer."
---

## Definition

**Namespace:** ASNA.DataGate.DataLink  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Reads a sequence of bytes from the channel into the specified buffer.

<a id="int-read-byte-inbuf-https-docs-microsoft-com-en-us-dotnet-api-system-byte-int-ibegin-int-cbytes"></a>
## int Read([Byte\[\] inBuf](https://docs.microsoft.com/en-us/dotnet/api/system.byte), int iBegin, int cBytes)

Reads a sequence of bytes from the channel into the specified buffer.

```cs
int Read(Byte[] inBuf, int iBegin, int cBytes)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Byte\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.byte) | inBuf | The buffer to store the data read from the channel.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | iBegin | The zero-based byte offset in inBuf at which to begin storing the data read from the channel.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | cBytes | The maximum number of bytes to read.

#### Returns

| Type | Description
| --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | The total number of bytes read into the buffer.

## See Also
- [IOpenAccessReader interface class](i-open-access-reader.html)
