---
title: "UserPasswordCredentialInlineConverter class"
description: "The UserPasswordCredentialInlineConverter class is responsible for converting UserPasswordCredential objects. "
last_modified_at: 2024-08-08T21:41:32Z
---

The UserPasswordCredentialInlineConverter class is responsible for converting UserPasswordCredential objects.

**Namespace:** ASNA.DataGate.Providers.Serialization
**Assembly:** ASNA.QSys.DataGate.Client.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [JsonConverter](https://learn.microsoft.com/en-us/dotnet/api/system.text.json.serialization.jsonconverter-1?view=net-8.0) --> [JsonConverter\<UserPasswordCredential\>](https://learn.microsoft.com/en-us/dotnet/api/system.text.json.serialization.jsonconverter-1?view=net-8.0)
<br>
<br>

## Methods

| Signature | Description |
| --- | --- |
| [Write](#void-writeutf8jsonwriter-writer-userpasswordcredential-value-jsonserializeroptions-options)([Utf8JsonWriter](https://learn.microsoft.com/en-us/dotnet/api/system.text.json.utf8jsonwriter?view=net-8.0), [UserPasswordCredential](/reference/datagate/datagate-providers/user-password-credential.html), [JsonSerializerOptions](https://learn.microsoft.com/en-us/dotnet/api/system.text.json.jsonserializeroptions?view=net-8.0)) | Writes a UserPasswordCredential to a Utf8JsonWriter.

### void Write([Utf8JsonWriter writer](https://learn.microsoft.com/en-us/dotnet/api/system.text.json.utf8jsonwriter?view=net-8.0), [UserPasswordCredential value](/reference/datagate/datagate-providers/user-password-credential.html), [JsonSerializerOptions options](https://learn.microsoft.com/en-us/dotnet/api/system.text.json.jsonserializeroptions?view=net-8.0))

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
