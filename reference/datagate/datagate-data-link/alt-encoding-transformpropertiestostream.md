---
title: "AltEncoding.TransformPropertiesToStream Method"
description: "When overridden in a derived class, writes the given ITransformProperties object to the specified BinaryWriter stream."
---

## Definition

**Namespace:** ASNA.DataGate.DataLink.Text  
**Assembly:** ASNA.QSys.DataGate.Client.dll

When overridden in a derived class, writes the given ITransformProperties object to the specified BinaryWriter stream.

<a id="void-transformpropertiestostream-itransformproperties-t-binarywriter-bw"></a>
## void TransformPropertiesToStream(ITransformProperties t, BinaryWriter bw)

When overridden in a derived class, writes the given ITransformProperties object to the specified BinaryWriter stream.

```cs
void TransformPropertiesToStream(ITransformProperties t, BinaryWriter bw)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [ITransformProperties](/reference/datagate/datagate-providers/i-transform-properties.html) | t | The ITransformProperties object to write to the stream.
| [BinaryWriter](https://learn.microsoft.com/en-us/dotnet/api/system.io.binarywriter?view=net-8.0) | bw | The BinaryWriter stream to write to.

## See Also
- [AltEncoding class](alt-encoding.html)
