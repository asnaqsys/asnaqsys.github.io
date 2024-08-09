---
title: "UserPasswordCredentialInlineConverter class"
description: "The UserPasswordCredentialInlineConverter class is responsible for converting UserPasswordCredential objects. "
last_modified_at: 2024-08-09T16:18:40Z
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
| [Read](#userpasswordcredential-readutf8jsonreader-reader-type-typetoconvert-jsonserializeroptions-options)([Utf8JsonReader&](https://learn.microsoft.com/en-us/dotnet/api/system.text.json.utf8jsonreader?view=net-8.0), [Type](https://docs.microsoft.com/en-us/dotnet/api/system.type), [JsonSerializerOptions](https://learn.microsoft.com/en-us/dotnet/api/system.text.json.jsonserializeroptions?view=net-8.0)) | Reads a UserPasswordCredential from a Utf8JsonReader.
| [Write](#void-writeutf8jsonwriter-writer-userpasswordcredential-value-jsonserializeroptions-options)([Utf8JsonWriter](https://learn.microsoft.com/en-us/dotnet/api/system.text.json.utf8jsonwriter?view=net-8.0), [UserPasswordCredential](/reference/datagate/datagate-providers/user-password-credential.html), [JsonSerializerOptions](https://learn.microsoft.com/en-us/dotnet/api/system.text.json.jsonserializeroptions?view=net-8.0)) | Writes a UserPasswordCredential to a Utf8JsonWriter.

### UserPasswordCredential Read([Utf8JsonReader& reader](https://learn.microsoft.com/en-us/dotnet/api/system.text.json.utf8jsonreader?view=net-8.0), [Type typeToConvert](https://docs.microsoft.com/en-us/dotnet/api/system.type), [JsonSerializerOptions options](https://learn.microsoft.com/en-us/dotnet/api/system.text.json.jsonserializeroptions?view=net-8.0))

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
