---
title: "UserPasswordCredentialInlineConverter.Read Method"
description: "Reads a UserPasswordCredential from a Utf8JsonReader."
---

## Definition

**Namespace:** ASNA.DataGate.Providers.Serialization  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Reads a UserPasswordCredential from a Utf8JsonReader.

<a id="userpasswordcredential-read-utf8jsonreader-reader-type-typetoconvert-jsonserializeroptions-options"></a>
## UserPasswordCredential Read(Utf8JsonReader& reader, Type typeToConvert, JsonSerializerOptions options)

Reads a UserPasswordCredential from a Utf8JsonReader.

```cs
UserPasswordCredential Read(Utf8JsonReader& reader, Type typeToConvert, JsonSerializerOptions options)
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
| [UserPasswordCredential](/reference/datagate/datagate-providers/user-password-credential.html) | A UserPasswordCredential that was read from the Utf8JsonReader.

## See Also
- [UserPasswordCredentialInlineConverter class](user-password-credential-inline-converter.html)
