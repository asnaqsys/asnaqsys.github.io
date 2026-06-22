---
title: "AltEncoding class"
description: "Represents a custom encoding that extends the base Encoding class, providing additional functionality for transforming data. "
last_modified_at: 2024-08-09T17:25:07Z
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
| [AltEncoding()](alt-encoding-ctor.html#altencoding) | Initializes a new instance of the  class with default encoder and decoder properties.

## Properties

| Type | Name | Description
| --- | --- | --- 
| [IEnumerable\<AltEncodingInfo\>](https://learn.microsoft.com/en-us/dotnet/api/system.collections.generic.ienumerable-1?view=net-8.0) | AvailableEncodings | Gets a list of all available AltEncoding objects. |
| [ITransformProperties](/reference/datagate/datagate-providers/i-transform-properties.html) | DecoderDefaultProps | Gets or sets the default properties for the decoder. |
| [ITransformProperties](/reference/datagate/datagate-providers/i-transform-properties.html) | EncoderDefaultProps | Gets or sets the default properties for the encoder. |

## Methods

| Signature | Description |
| --- | --- |
| [DictionaryFromITransformProps](alt-encoding-dictionaryfromitransformprops.html#dictionary-string-object-dictionaryfromitransformprops-itransformproperties-props)([ITransformProperties](/reference/datagate/datagate-providers/i-transform-properties.html)) | Converts the given ITransformProperties object into a dictionary.
| [Equal](alt-encoding-equal.html#bool-equal-itransformproperties-lhs-itransformproperties-rhs)([ITransformProperties](/reference/datagate/datagate-providers/i-transform-properties.html), [ITransformProperties](/reference/datagate/datagate-providers/i-transform-properties.html)) | Compares two ITransformProperties objects for equality.
| [GetAltDecoder](alt-encoding-getaltdecoder.html#altdecoder-getaltdecoder-itransformproperties-decprops)([ITransformProperties](/reference/datagate/datagate-providers/i-transform-properties.html)) | Returns an AltDecoder object for this AltEncoding, using the specified properties.
| [GetAltEncoder](alt-encoding-getaltencoder.html#altencoder-getaltencoder-itransformproperties-encprops)([ITransformProperties](/reference/datagate/datagate-providers/i-transform-properties.html)) | Returns an AltEncoder object for this AltEncoding, using the specified properties.
| [GetAltEncoding](alt-encoding-getaltencoding.html#altencoding-getaltencoding-string-name)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Returns an AltEncoding object for the specified name.
| [GetAltEncodingInfo()](alt-encoding-getaltencodinginfo.html#altencodinginfo-getaltencodinginfo) | Gets information about the current AltEncoding instance.
| [GetDecoder()](alt-encoding-getdecoder.html#decoder-getdecoder) | Returns an AltDecoder object for this AltEncoding, using the default properties.
| [GetDecoderImpl()](alt-encoding-getdecoderimpl.html#altdecoder-getdecoderimpl) | When overridden in a derived class, returns an AltDecoder object for this AltEncoding.
| [GetEncoder()](alt-encoding-getencoder.html#encoder-getencoder) | Returns an AltEncoder object for this AltEncoding, using the default properties.
| [GetEncoderImpl()](alt-encoding-getencoderimpl.html#altencoder-getencoderimpl) | When overridden in a derived class, returns an AltEncoder object for this AltEncoding.
| [TransformPropertiesFromDictionary](alt-encoding-transformpropertiesfromdictionary.html#itransformproperties-transformpropertiesfromdictionary-dictionary-string-object-dict)([Dictionary\<String, Object\>](https://learn.microsoft.com/en-us/dotnet/api/system.collections.generic.dictionary-2?view=net-8.0)) | Converts the given dictionary into an ITransformProperties object.
| [TransformPropertiesFromStream](alt-encoding-transformpropertiesfromstream.html#itransformproperties-transformpropertiesfromstream-binaryreader-br)([BinaryReader](https://learn.microsoft.com/en-us/dotnet/api/system.io.binaryreader?view=net-8.0)) | When overridden in a derived class, reads the given BinaryReader stream and converts it into an ITransformProperties object.
| [TransformPropertiesToStream](alt-encoding-transformpropertiestostream.html#void-transformpropertiestostream-itransformproperties-t-binarywriter-bw)([ITransformProperties](/reference/datagate/datagate-providers/i-transform-properties.html), [BinaryWriter](https://learn.microsoft.com/en-us/dotnet/api/system.io.binarywriter?view=net-8.0)) | When overridden in a derived class, writes the given ITransformProperties object to the specified BinaryWriter stream.

