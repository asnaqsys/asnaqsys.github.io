---
title: "ExportSourceAttribute class   | QSYS API Reference Guide"
description: "Defines Export Source Attribute on a type "
last_modified_at: 2024-08-09T17:26:04Z
---

Defines Export Source Attribute on a type

**Namespace:** ASNA.QSys.Expo.Model
**Assembly:** ASNA.QSys.Expo.Model.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [Attribute](https://docs.microsoft.com/en-us/dotnet/api/system.attribute)
<br>
<br>

## Properties

| Type | Name | Description
| --- | --- | --- 
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | CCSID | Gets or sets the Coded Character Set Identifier (CCSID). Defaults to 37 |

## Methods

| Signature | Description |
| --- | --- |
| [GetFrom](#exportsourceattribute-getfromtype-type)([Type](https://docs.microsoft.com/en-us/dotnet/api/system.type)) | Gets the ExportSourceAttribute from custom attributes in the indicated type

### ExportSourceAttribute GetFrom([Type type](https://docs.microsoft.com/en-us/dotnet/api/system.type))

Gets the ExportSourceAttribute from custom attributes in the indicated type

```cs
ExportSourceAttribute GetFrom(Type type)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Type](https://docs.microsoft.com/en-us/dotnet/api/system.type) | type | object type

#### Returns

| Type | Description
| --- | ---
| [ExportSourceAttribute](/reference/expo/qsys-expo-model/export-source-attribute.html) | The attribute
