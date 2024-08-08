---
title: "BaseRecordAttribute class     | QSYS API Reference Guide"
description: "Defines Base Record Attributes on a type "
last_modified_at: 2024-08-08T21:42:10Z
---

Defines Base Record Attributes on a type

**Namespace:** ASNA.QSys.Expo.Model
**Assembly:** ASNA.QSys.Expo.Model.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [Attribute](https://docs.microsoft.com/en-us/dotnet/api/system.attribute)
<br>
<br>

## Remarks

Model record classes may be declared with attributes to indicate runtime behavior. For example, `ChangeIndicator = 44` declares that when this record is changed by user interaction, the [Indicator](/reference/runtime/qsys-runtime/indicator.html) 44 should be set, such that logic can test this value and react to the change.

As any [C# Attributes](https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/concepts/attributes/), the syntax uses brackets right before the declaration of the class, for example:

```cs
[
    Record( ChangeIndicator = 44 )
]
public class MyRecord_Model : RecordModel
{
```

Defines the attribute `ChangeIndicator` for `MyRecord_Model` class.

The `BaseRecordAttribute` provides common attributes to all `RecordModel`s. Specialized (derived) Record classes, provide more attributes valid only to that class.

## Properties

| Type | Name | Description
| --- | --- | --- 
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | ChangeIndicator | Gets or sets the value that represents the Change indicator |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | FormatLevel | Gets or sets the Record Format Level Check hash code as a string |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | SetOffIndicators | Gets or sets a collection of Indicators to Set Off. The collection is a comma separated string |

## Methods

| Signature | Description |
| --- | --- |
| [GetFrom](#baserecordattribute-getfromtype-type)([Type](https://docs.microsoft.com/en-us/dotnet/api/system.type)) | Gets a BaseRecordAttribute from the Custom attributes associated with a type.

### BaseRecordAttribute GetFrom([Type type](https://docs.microsoft.com/en-us/dotnet/api/system.type))

Gets a BaseRecordAttribute from the Custom attributes associated with a type.

```cs
BaseRecordAttribute GetFrom(Type type)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Type](https://docs.microsoft.com/en-us/dotnet/api/system.type) | type | input type

#### Returns

| Type | Description
| --- | ---
| [BaseRecordAttribute](/reference/expo/qsys-expo-model/base-record-attribute.html) | the attribute
