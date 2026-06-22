---
title: "InputStreamAggregator.Write Method"
description: "Writes a sequence of bytes to the current stream and advances the current position within this stream by the number of bytes written."
---

## Definition

**Namespace:** ASNA.DataGate.Common.Util  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Writes a sequence of bytes to the current stream and advances the current position within this stream by the number of bytes written.

<a id="void-write-byte-buffer-https-docs-microsoft-com-en-us-dotnet-api-system-byte-int-offset-int-count"></a>
## void Write([Byte\[\] buffer](https://docs.microsoft.com/en-us/dotnet/api/system.byte), int offset, int count)

Writes a sequence of bytes to the current stream and advances the current position within this stream by the number of bytes written. This method always throws a NotSupportedException.

```cs
void Write(Byte[] buffer, int offset, int count)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Byte\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.byte) | buffer | An array of bytes. This method copies count bytes from buffer to the current stream.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | offset | The zero-based byte offset in buffer at which to begin copying bytes to the current stream.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | count | The number of bytes to be written to the current stream.

## See Also
- [InputStreamAggregator class](input-stream-aggregator.html)
