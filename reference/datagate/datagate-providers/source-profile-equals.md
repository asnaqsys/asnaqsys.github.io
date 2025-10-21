---
title: "SourceProfile.Equals Method"
description: "Determines whether the current SourceProfile instance is equal to another object or instance."
---

## Definition

**Namespace:** ASNA.DataGate.Providers  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Determines whether the current instance is equal to the specified instance or object.

## Overloads

| Signature | Description |
| --- | --- |
| [Equals](#bool-equalssourceprofile)( [SourceProfile](/reference/datagate/datagate-providers/source-profile.html)) | Determines whether the current instance of SourceProfile is equal to the specified instance.
| [Equals](#bool-equalsobject)( [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | Determines whether the current instance is equal to the specified object.
| [Equals](#bool-equalsobject-bool)( [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Determines whether the current instance is equal to the specified object, with an option to ignore the database name.

## bool Equals(SourceProfile)

Determines whether the current instance of SourceProfile is equal to the specified instance.

```cs
bool Equals(SourceProfile other)
```

#### Parameters

| Type | Parameter name | Description |
| --- | --- | --- |
| [SourceProfile](/reference/datagate/datagate-providers/source-profile.html) | other | The instance to compare with the current instance. |

### Remarks
This method is used to compare the current instance with another instance of the SourceProfile class. The comparison is based on the properties of the instances.

## bool Equals(object)

Determines whether the current instance is equal to the specified object.

```cs
bool Equals(object other)
```

#### Parameters

| Type | Parameter name | Description |
| --- | --- | --- |
| [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) | other | The instance to compare with the current instance. |

## bool Equals(object, bool)

Determines whether the current instance is equal to the specified object.

```cs
bool Equals(object obj, bool bIgnoreDatabaseName)
```

#### Parameters

| Type | Parameter name | Description |
| --- | --- | --- |
| [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) | obj | The object to compare with the current instance. |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | bIgnoreDatabaseName | A boolean value that indicates whether to ignore the database name in the comparison. |

### Remarks
This method is used to compare the current instance with another object of the same type. If the `bIgnoreDatabaseName` parameter is set to true, the comparison will ignore the database name.

## See Also
- [SourceProfile class](source-profile.html)
