---
title: "SourceProfileConverter.Read Method"
description: "Reads a SourceProfile from a Utf8JsonReader."
---

## Definition

**Namespace:** ASNA.DataGate.Providers.Serialization  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Reads a SourceProfile from a Utf8JsonReader.

<a id="sourceprofile-read-utf8jsonreader-reader-type-typetoconvert-jsonserializeroptions-options"></a>
## SourceProfile Read(Utf8JsonReader& reader, Type typeToConvert, JsonSerializerOptions options)

Reads a SourceProfile from a Utf8JsonReader.

```cs
SourceProfile Read(Utf8JsonReader& reader, Type typeToConvert, JsonSerializerOptions options)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Utf8JsonReader&](https://learn.microsoft.com/en-us/dotnet/api/system.text.json.utf8jsonreader?view=net-8.0) | reader | The Utf8JsonReader to read from.
| [Type](https://docs.microsoft.com/en-us/dotnet/api/system.type) | typeToConvert | The type of object to convert.
| [JsonSerializerOptions](https://learn.microsoft.com/en-us/dotnet/api/system.text.json.jsonserializeroptions?view=net-8.0) | options | Options for the serializer.

#### Returns

| Type | Description
| --- | ---
| [SourceProfile](/reference/datagate/datagate-providers/source-profile.html) | A SourceProfile that was read from the Utf8JsonReader.

## See Also
- [SourceProfileConverter class](source-profile-converter.html)
