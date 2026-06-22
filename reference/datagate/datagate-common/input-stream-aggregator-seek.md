---
title: "InputStreamAggregator.Seek Method"
description: "Sets the position within the current stream."
---

## Definition

**Namespace:** ASNA.DataGate.Common.Util  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Sets the position within the current stream.

<a id="long-seek-long-offset-seekorigin-origin"></a>
## long Seek(long offset, SeekOrigin origin)

Sets the position within the current stream. Always throws a NotSupportedException.

```cs
long Seek(long offset, SeekOrigin origin)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | offset | A byte offset relative to the origin parameter.
| [SeekOrigin](https://learn.microsoft.com/en-us/dotnet/api/system.io.seekorigin?view=net-8.0) | origin | A value of type SeekOrigin indicating the reference point used to obtain the new position.

#### Returns

| Type | Description
| --- | ---
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | Always throws a NotSupportedException.

## See Also
- [InputStreamAggregator class](input-stream-aggregator.html)
