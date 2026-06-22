---
title: "IOpenAccessWriter interface.Write Method"
description: "Writes a sequence of bytes to the channel from the specified buffer."
---

## Definition

**Namespace:** ASNA.DataGate.DataLink  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Writes a sequence of bytes to the channel from the specified buffer.

<a id="void-write-byte-inbuf-https-docs-microsoft-com-en-us-dotnet-api-system-byte-int-ibegin-int-cbytes"></a>
## void Write([Byte\[\] inBuf](https://docs.microsoft.com/en-us/dotnet/api/system.byte), int iBegin, int cBytes)

Writes a sequence of bytes to the channel from the specified buffer.

```cs
void Write(Byte[] inBuf, int iBegin, int cBytes)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Byte\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.byte) | inBuf | The buffer containing the data to write to the channel.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | iBegin | The zero-based byte offset in inBuf at which to begin writing from.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | cBytes | The number of bytes to write.

## See Also
- [IOpenAccessWriter interface class](i-open-access-writer.html)
