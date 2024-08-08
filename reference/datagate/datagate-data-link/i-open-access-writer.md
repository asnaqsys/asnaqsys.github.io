---
title: "IOpenAccessWriter interface   | QSYS API Reference Guide"
description: "Defines methods for writing data to an open access channel. "
last_modified_at: 2024-08-08T21:41:32Z
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
| [Flush()](#void-flush) | Flushes the writer, sending any buffered data to the channel.
| [Prepare()](#void-prepare) | Prepares the writer for a new write operation.
| [Write](#void-writebyte--inbuf-int-ibegin-int-cbytes)([Byte\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.byte), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Writes a sequence of bytes to the channel from the specified buffer.
| [WriteByte](#void-writebytebyte-b)([Byte](https://docs.microsoft.com/en-us/dotnet/api/system.byte)) | Writes a single byte to the channel.

### void Flush()

Flushes the writer, sending any buffered data to the channel.

```cs
void Flush()
```

### void Prepare()

Prepares the writer for a new write operation.

```cs
void Prepare()
```

### void Write([Byte\[\] inBuf](https://docs.microsoft.com/en-us/dotnet/api/system.byte), [int iBegin](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int cBytes](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

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

### void WriteByte([byte b](https://docs.microsoft.com/en-us/dotnet/api/system.byte))

Writes a single byte to the channel.

```cs
void WriteByte(byte b)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Byte](https://docs.microsoft.com/en-us/dotnet/api/system.byte) | b | The byte to write.
