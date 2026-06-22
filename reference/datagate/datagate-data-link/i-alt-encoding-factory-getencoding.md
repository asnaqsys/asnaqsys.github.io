---
title: "IAltEncodingFactory interface.GetEncoding Method"
description: "Generally, this method should only return an instance ofAltEncoding if the encoding is represented by one of theAltEncodingInfo objects returned by the Encodings property.This method should throw ArgumentException if the name given is notsupported by the factory."
---

## Definition

**Namespace:** ASNA.DataGate.DataLink.Text  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Generally, this method should only return an instance ofAltEncoding if the encoding is represented by one of theAltEncodingInfo objects returned by the Encodings property.This method should throw ArgumentException if the name given is notsupported by the factory.

<a id="altencoding-getencoding-string-name"></a>
## AltEncoding GetEncoding(string name)

Generally, this method should only return an instance ofAltEncoding if the encoding is represented by one of theAltEncodingInfo objects returned by the Encodings property.This method should throw ArgumentException if the name given is notsupported by the factory.

```cs
AltEncoding GetEncoding(string name)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | name | The name of the encoding, as returned by             AltEncoding.EncodingName.

#### Returns

| Type | Description
| --- | ---
| [AltEncoding](/reference/datagate/datagate-data-link/alt-encoding.html) | An instance of AltEncoding representing the desiredencoding translation facility.

## See Also
- [IAltEncodingFactory interface class](i-alt-encoding-factory.html)
