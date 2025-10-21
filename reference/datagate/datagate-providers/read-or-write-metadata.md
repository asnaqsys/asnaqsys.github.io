---
title: "ReadOrWriteMetadata Delegate"
description: "Offers DataGate a stream with which to read (or write) opaque metadata from (or to)."
---

## Definition

**Namespace:** ASNA.DataGate.Providers  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Used by a metadata cache service to provide DataGate with a stream to read or write opaque metadata.

```csharp
public delegate void ReadOrWriteMetadata(Stream metadataStream, bool forRead)
```

#### Parameters

| Type | Parameter name | Description |
| --- | --- | --- |
| [Stream](https://docs.microsoft.com/en-us/dotnet/api/system.io.stream) | metadataStream | A read- or write-only stream, depending on the value of forRead. |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | forRead | True if the stream contains metadata previously cached; false if DataGate should write database metadata to the stream for caching. |

## Remarks
This delegate is typically consumed by an IMetadataCacheService implementation that coordinates reading and writing provider-specific metadata blobs to and from a storage medium.

## See Also
- [ASNA.DataGate.Providers Namespace](/reference/datagate/datagate-providers/landing-page-namespace.html)
