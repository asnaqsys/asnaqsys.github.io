---
title: "DataGateCredentialConverter.Write Method"
description: "Writes the DataGate credentials to a secure string."
---

## Definition

**Namespace:** ASNA.DataGate.Providers.Serialization  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Writes the DataGate credentials to a secure string.

<a id="void-write-utf8jsonwriter-writer-idatagatecredential-value-jsonserializeroptions-options"></a>
## void Write(Utf8JsonWriter writer, IDataGateCredential value, JsonSerializerOptions options)

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

## See Also
- [DataGateCredentialConverter class](datagate-credential-converter.html)
