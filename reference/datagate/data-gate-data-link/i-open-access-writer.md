---
title: IOpenAccessWriter interface
---

Defines methods for writing to an open access data stream.

**Namespace:** ASNA.DataGate.DataLink
**Assembly:** ASNA.QSys.DataGate.Client.dll

**Inheritance:** 
<br>
<br>

## Methods

| Signature | Description |
| --- | --- |
| [Flush()](#flush-) | Flushes the data stream, ensuring all buffered data is written.
| [Prepare()](#prepare-) | Prepares the data stream for writing.
| [WriteByte](#writebyte-byte-)([Byte](https://docs.microsoft.com/en-us/dotnet/api/system.byte)) | Writes a single byte to the data stream.
| [Write](#write-byte-int32-int32-)([Byte](https://docs.microsoft.com/en-us/dotnet/api/system.byte), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Writes a sequence of bytes to the data stream.

### void Flush()

Flushes the data stream, ensuring all buffered data is written.

```cs
void Flush()
```

### void Prepare()

Prepares the data stream for writing.

```cs
void Prepare()
```

### void WriteByte([byte b](https://docs.microsoft.com/en-us/dotnet/api/system.byte))

Writes a single byte to the data stream.

```cs
void WriteByte(byte b)
```

#### Parameters
| Type | Parameter name | Description
| --- | --- | ---
| [Byte](https://docs.microsoft.com/en-us/dotnet/api/system.byte) | b | 

### void Write([Byte[] inBuf](https://docs.microsoft.com/en-us/dotnet/api/system.byte), [int iBegin](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int cBytes](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Writes a sequence of bytes to the data stream.

```cs
void Write(Byte[] inBuf, int iBegin, int cBytes)
```

#### Parameters
| Type | Parameter name | Description
| --- | --- | ---
| [Byte[]](https://docs.microsoft.com/en-us/dotnet/api/system.byte) | inBuf | 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | iBegin | 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | cBytes | 