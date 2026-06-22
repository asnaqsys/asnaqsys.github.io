---
title: "SourceProfileConverter class"
description: "The SourceProfileConverter class is responsible for converting source profiles. "
last_modified_at: 2024-08-09T17:25:07Z
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
| [SourceProfileConverter](source-profile-converter-ctor.html#sourceprofileconverter-sourceprofileconverteroptions)([SourceProfileConverterOptions](/reference/datagate/datagate-providers/source-profile-converter-options.html)) | Initializes a new instance of the  class with the specified options.
| [SourceProfileConverter()](source-profile-converter-ctor.html#sourceprofileconverter) | Initializes a new instance of the  class with default settings.

## Methods

| Signature | Description |
| --- | --- |
| [Read](source-profile-converter-read.html#sourceprofile-read-utf8jsonreader-reader-type-typetoconvert-jsonserializeroptions-options)([Utf8JsonReader&](https://learn.microsoft.com/en-us/dotnet/api/system.text.json.utf8jsonreader?view=net-8.0), [Type](https://docs.microsoft.com/en-us/dotnet/api/system.type), [JsonSerializerOptions](https://learn.microsoft.com/en-us/dotnet/api/system.text.json.jsonserializeroptions?view=net-8.0)) | Reads a SourceProfile from a Utf8JsonReader.
| [Write](source-profile-converter-write.html#void-write-utf8jsonwriter-writer-sourceprofile-value-jsonserializeroptions-options)([Utf8JsonWriter](https://learn.microsoft.com/en-us/dotnet/api/system.text.json.utf8jsonwriter?view=net-8.0), [SourceProfile](/reference/datagate/datagate-providers/source-profile.html), [JsonSerializerOptions](https://learn.microsoft.com/en-us/dotnet/api/system.text.json.jsonserializeroptions?view=net-8.0)) | Writes a SourceProfile to a Utf8JsonWriter.

