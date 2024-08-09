---
title: "DateAttribute class           | QSYS API Reference Guide"
description: "Provides Date Attribute (for Properties) "
last_modified_at: 2024-08-09T16:18:58Z
---

Provides Date Attribute (for Properties)

**Namespace:** ASNA.QSys.Expo.Model
**Assembly:** ASNA.QSys.Expo.Model.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [Attribute](https://docs.microsoft.com/en-us/dotnet/api/system.attribute) --> [FieldAttribute](/reference/expo/qsys-expo-model/field-attribute.html)
<br>
<br>

## Remarks

Model Fields are declared as Record Properties. To annotate the [Fixed Type](/concepts/program-structure/qsys-fixedtypes.html) as `Date`, Model properties can use this attribute.

For example,

```cs
[Date(DateFormat = DateAttribute.DdsDateFormat.USA)]
public DateTime SORDDATE { get; private set; } // ORDER DATE
```

Declares a read-only field of [Fixed Type](/concepts/program-structure/qsys-fixedtypes.html) `Date`, with `"USA"` presentation `Date Format`, named `SORDDATE` on a particular Model Record.

## Properties

| Type | Name | Description
| --- | --- | --- 
| [DdsDateFormat](/reference/expo/qsys-expo-model/dds-date-format.html) | DateFormat | Gets or sets DDS Date Format (Defaults to ISO) |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | DateSeparator | Gets or sets Date separator as a string (Defaults to "-") |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | STD_FORMAT | Standard Date Format |

## Methods

| Signature | Description |
| --- | --- |
| [GetFrom](#dateattribute-getfrommemberinfo-fieldmember)([MemberInfo](https://learn.microsoft.com/en-us/dotnet/api/system.reflection.memberinfo?view=net-8.0)) | Gets a DateAttribute from a field member

### DateAttribute GetFrom([MemberInfo fieldMember](https://learn.microsoft.com/en-us/dotnet/api/system.reflection.memberinfo?view=net-8.0))

Gets a DateAttribute from a field member

```cs
DateAttribute GetFrom(MemberInfo fieldMember)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [MemberInfo](https://learn.microsoft.com/en-us/dotnet/api/system.reflection.memberinfo?view=net-8.0) | fieldMember | field member information

#### Returns

| Type | Description
| --- | ---
| [DateAttribute](/reference/expo/qsys-expo-model/date-attribute.html) | the data attribute
