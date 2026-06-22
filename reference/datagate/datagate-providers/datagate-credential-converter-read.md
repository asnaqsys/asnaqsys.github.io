---
title: "DataGateCredentialConverter.Read Method"
description: "Reads the DataGate credentials from a Utf8JsonReader."
---

## Definition

**Namespace:** ASNA.DataGate.Providers.Serialization  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Reads the DataGate credentials from a Utf8JsonReader.

<a id="idatagatecredential-read-utf8jsonreader-reader-type-typetoconvert-jsonserializeroptions-options"></a>
## IDataGateCredential Read(Utf8JsonReader& reader, Type typeToConvert, JsonSerializerOptions options)

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

## See Also
- [DataGateCredentialConverter class](datagate-credential-converter.html)
