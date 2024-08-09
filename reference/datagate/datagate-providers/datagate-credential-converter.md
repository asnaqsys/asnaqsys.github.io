---
title: "DataGateCredentialConverter class"
description: "Provides a converter for DataGate credentials. "
last_modified_at: 2024-08-09T16:18:40Z
---

Provides a converter for DataGate credentials.

**Namespace:** ASNA.DataGate.Providers.Serialization
**Assembly:** ASNA.QSys.DataGate.Client.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [JsonConverter](https://learn.microsoft.com/en-us/dotnet/api/system.text.json.serialization.jsonconverter-1?view=net-8.0) --> [JsonConverter\<IDataGateCredential\>](https://learn.microsoft.com/en-us/dotnet/api/system.text.json.serialization.jsonconverter-1?view=net-8.0)
<br>
<br>

## Methods

| Signature | Description |
| --- | --- |
| [Read](#idatagatecredential-readutf8jsonreader-reader-type-typetoconvert-jsonserializeroptions-options)([Utf8JsonReader&](https://learn.microsoft.com/en-us/dotnet/api/system.text.json.utf8jsonreader?view=net-8.0), [Type](https://docs.microsoft.com/en-us/dotnet/api/system.type), [JsonSerializerOptions](https://learn.microsoft.com/en-us/dotnet/api/system.text.json.jsonserializeroptions?view=net-8.0)) | Reads the DataGate credentials from a Utf8JsonReader.
| [Write](#void-writeutf8jsonwriter-writer-idatagatecredential-value-jsonserializeroptions-options)([Utf8JsonWriter](https://learn.microsoft.com/en-us/dotnet/api/system.text.json.utf8jsonwriter?view=net-8.0), [IDataGateCredential](/reference/datagate/datagate-providers/i-datagate-credential.html), [JsonSerializerOptions](https://learn.microsoft.com/en-us/dotnet/api/system.text.json.jsonserializeroptions?view=net-8.0)) | Writes the DataGate credentials to a secure string.

### IDataGateCredential Read([Utf8JsonReader& reader](https://learn.microsoft.com/en-us/dotnet/api/system.text.json.utf8jsonreader?view=net-8.0), [Type typeToConvert](https://docs.microsoft.com/en-us/dotnet/api/system.type), [JsonSerializerOptions options](https://learn.microsoft.com/en-us/dotnet/api/system.text.json.jsonserializeroptions?view=net-8.0))

Reads the DataGate credentials from a Utf8JsonReader.

```cs
IDataGateCredential Read(Utf8JsonReader& reader, Type typeToConvert, JsonSerializerOptions options)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Utf8JsonReader&](https://learn.microsoft.com/en-us/dotnet/api/system.text.json.utf8jsonreader?view=net-8.0) | reader | The Utf8JsonReader from which the credentials are deserialized.
| [Type](https://docs.microsoft.com/en-us/dotnet/api/system.type) | typeToConvert | The type of the object to convert.
| [JsonSerializerOptions](https://learn.microsoft.com/en-us/dotnet/api/system.text.json.jsonserializeroptions?view=net-8.0) | options | The options for reading the credentials.

#### Returns

| Type | Description
| --- | ---
| [IDataGateCredential](/reference/datagate/datagate-providers/i-datagate-credential.html) | The deserialized DataGate credentials.

### void Write([Utf8JsonWriter writer](https://learn.microsoft.com/en-us/dotnet/api/system.text.json.utf8jsonwriter?view=net-8.0), [IDataGateCredential value](/reference/datagate/datagate-providers/i-datagate-credential.html), [JsonSerializerOptions options](https://learn.microsoft.com/en-us/dotnet/api/system.text.json.jsonserializeroptions?view=net-8.0))

Writes the DataGate credentials to a secure string.

```cs
void Write(Utf8JsonWriter writer, IDataGateCredential value, JsonSerializerOptions options)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Utf8JsonWriter](https://learn.microsoft.com/en-us/dotnet/api/system.text.json.utf8jsonwriter?view=net-8.0) | writer | The XmlWriter stream to which the credentials are serialized.
| [IDataGateCredential](/reference/datagate/datagate-providers/i-datagate-credential.html) | value | The DataGate credentials to write.
| [JsonSerializerOptions](https://learn.microsoft.com/en-us/dotnet/api/system.text.json.jsonserializeroptions?view=net-8.0) | options | The options for writing the credentials.
