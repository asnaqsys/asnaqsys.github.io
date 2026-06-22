---
title: "AltEncoding.GetAltEncoder Method"
description: "Returns an AltEncoder object for this AltEncoding, using the specified properties."
---

## Definition

**Namespace:** ASNA.DataGate.DataLink.Text  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Returns an AltEncoder object for this AltEncoding, using the specified properties.

<a id="altencoder-getaltencoder-itransformproperties-encprops"></a>
## AltEncoder GetAltEncoder(ITransformProperties encProps)

Returns an AltEncoder object for this AltEncoding, using the specified properties.

```cs
AltEncoder GetAltEncoder(ITransformProperties encProps)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [ITransformProperties](/reference/datagate/datagate-providers/i-transform-properties.html) | encProps | The properties to use for the AltEncoder. If null, the default properties are used.

#### Returns

| Type | Description
| --- | ---
| [AltEncoder](/reference/datagate/datagate-data-link/alt-encoder.html) | An AltEncoder object for this AltEncoding, using the specified properties.

## See Also
- [AltEncoding class](alt-encoding.html)
