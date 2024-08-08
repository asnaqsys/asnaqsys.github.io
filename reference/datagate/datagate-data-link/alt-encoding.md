---
title: "AltEncoding class             | QSYS API Reference Guide"
description: "Represents a custom encoding that extends the base Encoding class, providing additional functionality for transforming data. "
last_modified_at: 2024-08-08T21:41:32Z
---

Represents a custom encoding that extends the base Encoding class, providing additional functionality for transforming data.

**Namespace:** ASNA.DataGate.DataLink.Text
**Assembly:** ASNA.QSys.DataGate.Client.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [Encoding](https://learn.microsoft.com/en-us/dotnet/api/system.text.encoding?view=net-8.0)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [AltEncoding()](#altencoding) | Initializes a new instance of the  class with default encoder and decoder properties.

### AltEncoding()

Initializes a new instance of the  class with default encoder and decoder properties.

```cs
AltEncoding()
```

## Properties

| Type | Name | Description
| --- | --- | --- 
| [IEnumerable\<AltEncodingInfo\>](https://learn.microsoft.com/en-us/dotnet/api/system.collections.generic.ienumerable-1?view=net-8.0) | AvailableEncodings | Gets a list of all available AltEncoding objects. |
| [ITransformProperties](/reference/datagate/datagate-providers/i-transform-properties.html) | DecoderDefaultProps | Gets or sets the default properties for the decoder. |
| [ITransformProperties](/reference/datagate/datagate-providers/i-transform-properties.html) | EncoderDefaultProps | Gets or sets the default properties for the encoder. |

## Methods

| Signature | Description |
| --- | --- |
| [DictionaryFromITransformProps](#dictionary-string-object-dictionaryfromitransformpropsitransformproperties-props)([ITransformProperties](/reference/datagate/datagate-providers/i-transform-properties.html)) | Converts the given ITransformProperties object into a dictionary.
| [Equal](#bool-equalitransformproperties-lhs-itransformproperties-rhs)([ITransformProperties](/reference/datagate/datagate-providers/i-transform-properties.html), [ITransformProperties](/reference/datagate/datagate-providers/i-transform-properties.html)) | Compares two ITransformProperties objects for equality.
| [GetAltDecoder](#altdecoder-getaltdecoderitransformproperties-decprops)([ITransformProperties](/reference/datagate/datagate-providers/i-transform-properties.html)) | Returns an AltDecoder object for this AltEncoding, using the specified properties.
| [GetAltEncoder](#altencoder-getaltencoderitransformproperties-encprops)([ITransformProperties](/reference/datagate/datagate-providers/i-transform-properties.html)) | Returns an AltEncoder object for this AltEncoding, using the specified properties.
| [GetAltEncoding](#altencoding-getaltencodingstring-name)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Returns an AltEncoding object for the specified name.
| [GetAltEncodingInfo()](#altencodinginfo-getaltencodinginfo) | Gets information about the current AltEncoding instance.
| [GetDecoder()](#decoder-getdecoder) | Returns an AltDecoder object for this AltEncoding, using the default properties.
| [GetDecoderImpl()](#altdecoder-getdecoderimpl) | When overridden in a derived class, returns an AltDecoder object for this AltEncoding.
| [GetEncoder()](#encoder-getencoder) | Returns an AltEncoder object for this AltEncoding, using the default properties.
| [GetEncoderImpl()](#altencoder-getencoderimpl) | When overridden in a derived class, returns an AltEncoder object for this AltEncoding.
| [TransformPropertiesFromStream](#itransformproperties-transformpropertiesfromstreambinaryreader-br)([BinaryReader](https://learn.microsoft.com/en-us/dotnet/api/system.io.binaryreader?view=net-8.0)) | When overridden in a derived class, reads the given BinaryReader stream and converts it into an ITransformProperties object.
| [TransformPropertiesToStream](#void-transformpropertiestostreamitransformproperties-t-binarywriter-bw)([ITransformProperties](/reference/datagate/datagate-providers/i-transform-properties.html), [BinaryWriter](https://learn.microsoft.com/en-us/dotnet/api/system.io.binarywriter?view=net-8.0)) | When overridden in a derived class, writes the given ITransformProperties object to the specified BinaryWriter stream.

### Dictionary\<string, object\> DictionaryFromITransformProps([ITransformProperties props](/reference/datagate/datagate-providers/i-transform-properties.html))

Converts the given ITransformProperties object into a dictionary.

```cs
Dictionary<string, object> DictionaryFromITransformProps(ITransformProperties props)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [ITransformProperties](/reference/datagate/datagate-providers/i-transform-properties.html) | props | The ITransformProperties object to convert.

#### Returns

| Type | Description
| --- | ---
| [Dictionary`2](https://learn.microsoft.com/en-us/dotnet/api/system.collections.generic.dictionary-2?view=net-8.0) | A dictionary representing the properties of the given ITransformProperties object.

### bool Equal([ITransformProperties lhs](/reference/datagate/datagate-providers/i-transform-properties.html), [ITransformProperties rhs](/reference/datagate/datagate-providers/i-transform-properties.html))

Compares two ITransformProperties objects for equality.

```cs
bool Equal(ITransformProperties lhs, ITransformProperties rhs)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [ITransformProperties](/reference/datagate/datagate-providers/i-transform-properties.html) | lhs | The first ITransformProperties object to compare.
| [ITransformProperties](/reference/datagate/datagate-providers/i-transform-properties.html) | rhs | The second ITransformProperties object to compare.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | True if the two ITransformProperties objects are equal; otherwise, false.

### AltDecoder GetAltDecoder([ITransformProperties decProps](/reference/datagate/datagate-providers/i-transform-properties.html))

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

### AltEncoder GetAltEncoder([ITransformProperties encProps](/reference/datagate/datagate-providers/i-transform-properties.html))

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

### AltEncoding GetAltEncoding([string name](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Returns an AltEncoding object for the specified name.

```cs
AltEncoding GetAltEncoding(string name)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | name | The name for which to get an AltEncoding.

#### Returns

| Type | Description
| --- | ---
| [AltEncoding](/reference/datagate/datagate-data-link/alt-encoding.html) | An AltEncoding object for the specified name.

### AltEncodingInfo GetAltEncodingInfo()

Gets information about the current AltEncoding instance.

```cs
AltEncodingInfo GetAltEncodingInfo()
```

### Decoder GetDecoder()

Returns an AltDecoder object for this AltEncoding, using the default properties.

```cs
Decoder GetDecoder()
```

### AltDecoder GetDecoderImpl()

When overridden in a derived class, returns an AltDecoder object for this AltEncoding.

```cs
AltDecoder GetDecoderImpl()
```

### Encoder GetEncoder()

Returns an AltEncoder object for this AltEncoding, using the default properties.

```cs
Encoder GetEncoder()
```

### AltEncoder GetEncoderImpl()

When overridden in a derived class, returns an AltEncoder object for this AltEncoding.

```cs
AltEncoder GetEncoderImpl()
```

### ITransformProperties TransformPropertiesFromStream([BinaryReader br](https://learn.microsoft.com/en-us/dotnet/api/system.io.binaryreader?view=net-8.0))

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

### void TransformPropertiesToStream([ITransformProperties t](/reference/datagate/datagate-providers/i-transform-properties.html), [BinaryWriter bw](https://learn.microsoft.com/en-us/dotnet/api/system.io.binarywriter?view=net-8.0))

When overridden in a derived class, writes the given ITransformProperties object to the specified BinaryWriter stream.

```cs
void TransformPropertiesToStream(ITransformProperties t, BinaryWriter bw)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [ITransformProperties](/reference/datagate/datagate-providers/i-transform-properties.html) | t | The ITransformProperties object to write to the stream.
| [BinaryWriter](https://learn.microsoft.com/en-us/dotnet/api/system.io.binarywriter?view=net-8.0) | bw | The BinaryWriter stream to write to.
