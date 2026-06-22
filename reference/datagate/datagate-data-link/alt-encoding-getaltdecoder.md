---
title: "AltEncoding.GetAltDecoder Method"
description: "Returns an AltDecoder object for this AltEncoding, using the specified properties."
---

## Definition

**Namespace:** ASNA.DataGate.DataLink.Text  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Returns an AltDecoder object for this AltEncoding, using the specified properties.

<a id="altdecoder-getaltdecoder-itransformproperties-decprops"></a>
## AltDecoder GetAltDecoder(ITransformProperties decProps)

Returns an AltDecoder object for this AltEncoding, using the specified properties.

```cs
AltDecoder GetAltDecoder(ITransformProperties decProps)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [ITransformProperties](/reference/datagate/datagate-providers/i-transform-properties.html) | decProps | The properties to use for the AltDecoder. If null, the default properties are used.

#### Returns

| Type | Description
| --- | ---
| [AltDecoder](/reference/datagate/datagate-data-link/alt-decoder.html) | An AltDecoder object for this AltEncoding, using the specified properties.

## See Also
- [AltEncoding class](alt-encoding.html)
