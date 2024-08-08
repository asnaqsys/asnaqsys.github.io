---
title: "SourceProfileConverter class  | QSYS API Reference Guide"
description: "The SourceProfileConverter class is responsible for converting source profiles. "
last_modified_at: 2024-08-08T21:41:32Z
---

The SourceProfileConverter class is responsible for converting source profiles.

**Namespace:** ASNA.DataGate.Providers.Serialization
**Assembly:** ASNA.QSys.DataGate.Client.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [JsonConverter](https://learn.microsoft.com/en-us/dotnet/api/system.text.json.serialization.jsonconverter-1?view=net-8.0) --> [JsonConverter\<SourceProfile\>](https://learn.microsoft.com/en-us/dotnet/api/system.text.json.serialization.jsonconverter-1?view=net-8.0)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [SourceProfileConverter](#sourceprofileconvertersourceprofileconverteroptions)([SourceProfileConverterOptions](/reference/datagate/datagate-providers/source-profile-converter-options.html)) | Initializes a new instance of the  class with the specified options.
| [SourceProfileConverter()](#sourceprofileconverter) | Initializes a new instance of the  class with default settings.

### SourceProfileConverter([SourceProfileConverterOptions](/reference/datagate/datagate-providers/source-profile-converter-options.html))

Initializes a new instance of the  class with the specified options.

```cs
SourceProfileConverter(SourceProfileConverterOptions)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [SourceProfileConverterOptions](/reference/datagate/datagate-providers/source-profile-converter-options.html) | opts | The options for the source profile converter.

### SourceProfileConverter()

Initializes a new instance of the  class with default settings.

```cs
SourceProfileConverter()
```

## Methods

| Signature | Description |
| --- | --- |
| [Write](#void-writeutf8jsonwriter-writer-sourceprofile-value-jsonserializeroptions-options)([Utf8JsonWriter](https://learn.microsoft.com/en-us/dotnet/api/system.text.json.utf8jsonwriter?view=net-8.0), [SourceProfile](/reference/datagate/datagate-providers/source-profile.html), [JsonSerializerOptions](https://learn.microsoft.com/en-us/dotnet/api/system.text.json.jsonserializeroptions?view=net-8.0)) | Writes a SourceProfile to a Utf8JsonWriter.

### void Write([Utf8JsonWriter writer](https://learn.microsoft.com/en-us/dotnet/api/system.text.json.utf8jsonwriter?view=net-8.0), [SourceProfile value](/reference/datagate/datagate-providers/source-profile.html), [JsonSerializerOptions options](https://learn.microsoft.com/en-us/dotnet/api/system.text.json.jsonserializeroptions?view=net-8.0))

Writes a SourceProfile to a Utf8JsonWriter.

```cs
void Write(Utf8JsonWriter writer, SourceProfile value, JsonSerializerOptions options)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Utf8JsonWriter](https://learn.microsoft.com/en-us/dotnet/api/system.text.json.utf8jsonwriter?view=net-8.0) | writer | The Utf8JsonWriter to write to.
| [SourceProfile](/reference/datagate/datagate-providers/source-profile.html) | value | The SourceProfile to write.
| [JsonSerializerOptions](https://learn.microsoft.com/en-us/dotnet/api/system.text.json.jsonserializeroptions?view=net-8.0) | options | Options for the serializer.
