---
title: "InputStreamAggregator class"
description: "Queue multiple, fixed-length, read-only streams into one stream. "
last_modified_at: 2024-08-09T17:25:07Z
---

Queue multiple, fixed-length, read-only streams into one stream.

**Namespace:** ASNA.DataGate.Common.Util
**Assembly:** ASNA.QSys.DataGate.Client.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [MarshalByRefObject](https://learn.microsoft.com/en-us/dotnet/api/system.marshalbyrefobject?view=net-8.0) --> [Stream](https://learn.microsoft.com/en-us/dotnet/api/system.io.stream?view=net-8.0)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [InputStreamAggregator()](input-stream-aggregator-ctor.html#inputstreamaggregator) | Initializes a new instance of the  class.

## Properties

| Type | Name | Description
| --- | --- | --- 
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | CanRead | Gets a value indicating whether the current stream supports reading. |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | CanSeek | Gets a value indicating whether the current stream supports seeking. |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | CanWrite | Gets a value indicating whether the current stream supports writing. |
| [Int64](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | Length | Gets the length in bytes of the stream. |
| [Int64](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | Position | Gets or sets the position within the current stream. |

## Methods

| Signature | Description |
| --- | --- |
| [Append](input-stream-aggregator-append.html#void-append-int-len-func-stream-cons)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Func\<Stream\>](https://learn.microsoft.com/en-us/dotnet/api/system.func-2?view=net-8.0)) | Appends a new stream to the list of streams to be aggregated.
| [Dispose](input-stream-aggregator-dispose.html#void-dispose-bool-disposing)([Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Releases all resources used by the current instance of the  class.
| [Finalize()](input-stream-aggregator-finalize.html#void-finalize) | Finalizes an instance of the  class.
| [Flush()](input-stream-aggregator-flush.html#void-flush) | Overrides the Stream.Flush method so that no action is performed.
| [Read](input-stream-aggregator-read.html#int-read-byte-buffer-https-docs-microsoft-com-en-us-dotnet-api-system-byte-int-offset-int-count)([Byte\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.byte), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Reads a sequence of bytes from the current stream and advances the position within the stream by the number of bytes read.
| [ReadByte()](input-stream-aggregator-readbyte.html#int-readbyte) | Reads a byte from the stream and advances the position within the stream by one byte, or returns -1 if at the end of the stream.
| [Seek](input-stream-aggregator-seek.html#long-seek-long-offset-seekorigin-origin)([Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64), [SeekOrigin](https://learn.microsoft.com/en-us/dotnet/api/system.io.seekorigin?view=net-8.0)) | Sets the position within the current stream. Always throws a NotSupportedException.
| [SetLength](input-stream-aggregator-setlength.html#void-setlength-long-value)([Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64)) | Sets the length of the current stream. This method always throws a NotSupportedException.
| [Write](input-stream-aggregator-write.html#void-write-byte-buffer-https-docs-microsoft-com-en-us-dotnet-api-system-byte-int-offset-int-count)([Byte\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.byte), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Writes a sequence of bytes to the current stream and advances the current position within this stream by the number of bytes written. This method always throws a NotSupportedException.

