---
title: "WrfHashAttribute class        | QSYS API Reference Guide"
description: "Holds the computed hash value for the Wrf corresponding to this class. "
last_modified_at: 2024-08-09T16:18:58Z
---

Holds the computed hash value for the Wrf corresponding to this class.

**Namespace:** ASNA.QSys.Expo.Model
**Assembly:** ASNA.QSys.Expo.Model.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [Attribute](https://docs.microsoft.com/en-us/dotnet/api/system.attribute)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [WrfHashAttribute](#wrfhashattributestring)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Initializes a WrfHashAttribute object.

### WrfHashAttribute([String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Initializes a WrfHashAttribute object.

```cs
WrfHashAttribute(String)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | wrfHashValue | Computed hash value for the Wrf that corresponds to this Model class.

## Properties

| Type | Name | Description
| --- | --- | --- 
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | WrfHashValue | Gets the computed hash value for the Wrf. Must match the hash value of the reconstituted Wrf file. |

## Methods

| Signature | Description |
| --- | --- |
| [GetFrom](#wrfhashattribute-getfromtype-type)([Type](https://docs.microsoft.com/en-us/dotnet/api/system.type)) | Gets the WrfHashAttribute from the Custom attributes on a type.

### WrfHashAttribute GetFrom([Type type](https://docs.microsoft.com/en-us/dotnet/api/system.type))

Gets the WrfHashAttribute from the Custom attributes on a type.

```cs
WrfHashAttribute GetFrom(Type type)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Type](https://docs.microsoft.com/en-us/dotnet/api/system.type) | type | The type from which to extract the attribute.

#### Returns

| Type | Description
| --- | ---
| [WrfHashAttribute](/reference/expo/qsys-expo-model/wrf-hash-attribute.html) | The WrfHashAttribute in the given type, or null if the attribute doesn't exist.
