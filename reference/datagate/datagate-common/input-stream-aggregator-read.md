---
title: "InputStreamAggregator.Read Method"
description: "Reads a sequence of bytes from the current stream and advances the position within the stream by the number of bytes read."
---

## Definition

**Namespace:** ASNA.DataGate.Common.Util  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Reads a sequence of bytes from the current stream and advances the position within the stream by the number of bytes read.

<a id="int-read-byte-buffer-https-docs-microsoft-com-en-us-dotnet-api-system-byte-int-offset-int-count"></a>
## int Read([Byte\[\] buffer](https://docs.microsoft.com/en-us/dotnet/api/system.byte), int offset, int count)

Reads a sequence of bytes from the current stream and advances the position within the stream by the number of bytes read.

```cs
int Read(Byte[] buffer, int offset, int count)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Byte\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.byte) | buffer | An array of bytes. When this method returns, the buffer contains the specified byte array with the values between offset and (offset + count - 1) replaced by the bytes read from the current source.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | offset | The zero-based byte offset in buffer at which to begin storing the data read from the current stream.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | count | The maximum number of bytes to be read from the current stream.

#### Returns

| Type | Description
| --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | The total number of bytes read into the buffer. This can be less than the number of bytes requested if that many bytes are not currently available, or zero (0) if the end of the stream has been reached.

## See Also
- [InputStreamAggregator class](input-stream-aggregator.html)
