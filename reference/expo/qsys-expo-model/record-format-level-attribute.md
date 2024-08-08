---
title: "RecordFormatLevelAttribute class"
description: "Defines the Record level value for a record in the class. "
last_modified_at: 2024-08-08T21:42:10Z
---

Defines the Record level value for a record in the class.

**Namespace:** ASNA.QSys.Expo.Model
**Assembly:** ASNA.QSys.Expo.Model.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [Attribute](https://docs.microsoft.com/en-us/dotnet/api/system.attribute)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [RecordFormatLevelAttribute](#recordformatlevelattributestring-string)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Initializes a RecordFormatLevelAttribute object.

### RecordFormatLevelAttribute([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Initializes a RecordFormatLevelAttribute object.

```cs
RecordFormatLevelAttribute(String, String)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | recordName | The name of the record format.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | levelValue | The string value of the record format level.

## Properties

| Type | Name | Description
| --- | --- | --- 
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | LevelValue | Gets the value of the record format level. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | RecordName | Gets the name of the record format. |

## Methods

| Signature | Description |
| --- | --- |
| [GetAllFrom](#ienumerable-recordformatlevelattribute-getallfromtype-type)([Type](https://docs.microsoft.com/en-us/dotnet/api/system.type)) | Extract all RecordFormatLevelAttribute definitions from the custom attributes on a type.

### IEnumerable\<RecordFormatLevelAttribute\> GetAllFrom([Type type](https://docs.microsoft.com/en-us/dotnet/api/system.type))

Extract all RecordFormatLevelAttribute definitions from the custom attributes on a type.

```cs
IEnumerable<RecordFormatLevelAttribute> GetAllFrom(Type type)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Type](https://docs.microsoft.com/en-us/dotnet/api/system.type) | type | The type from which to extract the attributes.

#### Returns

| Type | Description
| --- | ---
| [IEnumerable`1](https://learn.microsoft.com/en-us/dotnet/api/system.collections.generic.ienumerable-1?view=net-8.0) | An IEnumerable object that contains all the RecordFormatLevelAttribute objects of the type argument.
