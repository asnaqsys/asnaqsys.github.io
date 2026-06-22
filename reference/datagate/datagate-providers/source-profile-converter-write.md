---
title: "SourceProfileConverter.Write Method"
description: "Writes a SourceProfile to a Utf8JsonWriter."
---

## Definition

**Namespace:** ASNA.DataGate.Providers.Serialization  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Writes a SourceProfile to a Utf8JsonWriter.

<a id="void-write-utf8jsonwriter-writer-sourceprofile-value-jsonserializeroptions-options"></a>
## void Write(Utf8JsonWriter writer, SourceProfile value, JsonSerializerOptions options)

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

## See Also
- [SourceProfileConverter class](source-profile-converter.html)
