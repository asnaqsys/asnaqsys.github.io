---
title: "UserPasswordCredentialInlineConverter.Write Method"
description: "Writes a UserPasswordCredential to a Utf8JsonWriter."
---

## Definition

**Namespace:** ASNA.DataGate.Providers.Serialization  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Writes a UserPasswordCredential to a Utf8JsonWriter.

<a id="void-write-utf8jsonwriter-writer-userpasswordcredential-value-jsonserializeroptions-options"></a>
## void Write(Utf8JsonWriter writer, UserPasswordCredential value, JsonSerializerOptions options)

Writes a UserPasswordCredential to a Utf8JsonWriter.

```cs
void Write(Utf8JsonWriter writer, UserPasswordCredential value, JsonSerializerOptions options)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Utf8JsonWriter](https://learn.microsoft.com/en-us/dotnet/api/system.text.json.utf8jsonwriter?view=net-8.0) | writer | The Utf8JsonWriter to write to.
| [UserPasswordCredential](/reference/datagate/datagate-providers/user-password-credential.html) | value | The UserPasswordCredential to write.
| [JsonSerializerOptions](https://learn.microsoft.com/en-us/dotnet/api/system.text.json.jsonserializeroptions?view=net-8.0) | options | Options for the serializer.

## See Also
- [UserPasswordCredentialInlineConverter class](user-password-credential-inline-converter.html)
