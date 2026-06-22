---
title: "IOpenAccessWriter interface"
description: "Defines methods for writing data to an open access channel. "
last_modified_at: 2024-08-09T17:25:07Z
---

Defines methods for writing data to an open access channel.

**Namespace:** ASNA.DataGate.DataLink
**Assembly:** ASNA.QSys.DataGate.Client.dll

**Extends:** doesn't extend any other interfaces.
<br>
<br>

## Methods

| Signature | Description |
| --- | --- |
| [Flush()](i-open-access-writer-flush.html#void-flush) | Flushes the writer, sending any buffered data to the channel.
| [Prepare()](i-open-access-writer-prepare.html#void-prepare) | Prepares the writer for a new write operation.
| [Write](i-open-access-writer-write.html#void-write-byte-inbuf-https-docs-microsoft-com-en-us-dotnet-api-system-byte-int-ibegin-int-cbytes)([Byte\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.byte), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Writes a sequence of bytes to the channel from the specified buffer.
| [WriteByte](i-open-access-writer-writebyte.html#void-writebyte-byte-b)([Byte](https://docs.microsoft.com/en-us/dotnet/api/system.byte)) | Writes a single byte to the channel.

