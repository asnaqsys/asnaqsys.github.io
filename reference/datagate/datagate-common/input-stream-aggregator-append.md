---
title: "InputStreamAggregator.Append Method"
description: "Appends a new stream to the list of streams to be aggregated."
---

## Definition

**Namespace:** ASNA.DataGate.Common.Util  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Appends a new stream to the list of streams to be aggregated.

<a id="void-append-int-len-func-stream-cons"></a>
## void Append(int len, Func\<Stream\> cons)

Appends a new stream to the list of streams to be aggregated.

```cs
void Append(int len, Func<Stream> cons)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | len | The length of the stream to be appended.
| [Func\<Stream\>](https://learn.microsoft.com/en-us/dotnet/api/system.func-2?view=net-8.0) | cons | A function that constructs the stream to be appended.

## See Also
- [InputStreamAggregator class](input-stream-aggregator.html)
