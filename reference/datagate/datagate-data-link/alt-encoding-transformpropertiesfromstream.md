---
title: "AltEncoding.TransformPropertiesFromStream Method"
description: "When overridden in a derived class, reads the given BinaryReader stream and converts it into an ITransformProperties object."
---

## Definition

**Namespace:** ASNA.DataGate.DataLink.Text  
**Assembly:** ASNA.QSys.DataGate.Client.dll

When overridden in a derived class, reads the given BinaryReader stream and converts it into an ITransformProperties object.

<a id="itransformproperties-transformpropertiesfromstream-binaryreader-br"></a>
## ITransformProperties TransformPropertiesFromStream(BinaryReader br)

When overridden in a derived class, reads the given BinaryReader stream and converts it into an ITransformProperties object.

```cs
ITransformProperties TransformPropertiesFromStream(BinaryReader br)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [BinaryReader](https://learn.microsoft.com/en-us/dotnet/api/system.io.binaryreader?view=net-8.0) | br | The BinaryReader stream to read from.

#### Returns

| Type | Description
| --- | ---
| [ITransformProperties](/reference/datagate/datagate-providers/i-transform-properties.html) | An ITransformProperties object representing the properties read from the stream.

## See Also
- [AltEncoding class](alt-encoding.html)
