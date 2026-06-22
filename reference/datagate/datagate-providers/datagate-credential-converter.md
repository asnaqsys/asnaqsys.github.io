---
title: "DataGateCredentialConverter class"
description: "Provides a converter for DataGate credentials. "
last_modified_at: 2024-08-09T17:25:07Z
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
| [Read](datagate-credential-converter-read.html#idatagatecredential-read-utf8jsonreader-reader-type-typetoconvert-jsonserializeroptions-options)([Utf8JsonReader&](https://learn.microsoft.com/en-us/dotnet/api/system.text.json.utf8jsonreader?view=net-8.0), [Type](https://docs.microsoft.com/en-us/dotnet/api/system.type), [JsonSerializerOptions](https://learn.microsoft.com/en-us/dotnet/api/system.text.json.jsonserializeroptions?view=net-8.0)) | Reads the DataGate credentials from a Utf8JsonReader.
| [Write](datagate-credential-converter-write.html#void-write-utf8jsonwriter-writer-idatagatecredential-value-jsonserializeroptions-options)([Utf8JsonWriter](https://learn.microsoft.com/en-us/dotnet/api/system.text.json.utf8jsonwriter?view=net-8.0), [IDataGateCredential](/reference/datagate/datagate-providers/i-datagate-credential.html), [JsonSerializerOptions](https://learn.microsoft.com/en-us/dotnet/api/system.text.json.jsonserializeroptions?view=net-8.0)) | Writes the DataGate credentials to a secure string.

