---
title: "ISimpleSerializer interface   | QSYS API Reference Guide"
description: "Provides an interface for simple serialization and deserialization operations. "
last_modified_at: 2024-08-09T17:25:07Z
---

Provides an interface for simple serialization and deserialization operations.

**Namespace:** ASNA.DataGate.Providers
**Assembly:** ASNA.QSys.DataGate.Client.dll

**Extends:** doesn't extend any other interfaces.
<br>
<br>

## Methods

| Signature | Description |
| --- | --- |
| [Deserialize](#void-deserializestream-istream)([Stream](https://learn.microsoft.com/en-us/dotnet/api/system.io.stream?view=net-8.0)) | De-serializes data from a stream.
| [Serialize](#void-serializestream-ostream)([Stream](https://learn.microsoft.com/en-us/dotnet/api/system.io.stream?view=net-8.0)) | Serializes data and writes it to a stream.

### void Deserialize([Stream istream](https://learn.microsoft.com/en-us/dotnet/api/system.io.stream?view=net-8.0))

De-serializes data from a stream.

```cs
void Deserialize(Stream istream)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Stream](https://learn.microsoft.com/en-us/dotnet/api/system.io.stream?view=net-8.0) | istream | The stream from which the data will be deserialized.

### void Serialize([Stream ostream](https://learn.microsoft.com/en-us/dotnet/api/system.io.stream?view=net-8.0))

Serializes data and writes it to a stream.

```cs
void Serialize(Stream ostream)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Stream](https://learn.microsoft.com/en-us/dotnet/api/system.io.stream?view=net-8.0) | ostream | The stream where the serialized data will be written.
