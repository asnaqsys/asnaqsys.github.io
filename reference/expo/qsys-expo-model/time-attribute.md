---
title: "TimeAttribute class           | QSYS API Reference Guide"
description: "Provides Time Attribute (for Properties) "
last_modified_at: 2024-08-08T21:42:10Z
---

Provides Time Attribute (for Properties)

**Namespace:** ASNA.QSys.Expo.Model
**Assembly:** ASNA.QSys.Expo.Model.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [Attribute](https://docs.microsoft.com/en-us/dotnet/api/system.attribute) --> [FieldAttribute](/reference/expo/qsys-expo-model/field-attribute.html)
<br>
<br>

## Remarks

Model Fields are declared as Record Properties. To annotate the [Fixed Type](/concepts/program-structure/qsys-fixedtypes.html) as `Time`, Model properties can use this attribute.

For example,

```cs
[Time(TimeAttribute.DdsTimeFormat.USA)]
public DateTime OPENTIME { get; private set; } // Opening Time
```

Declares a read-only field of [Fixed Type](/concepts/program-structure/qsys-fixedtypes.html) `Time`, with `"USA"` presentation `Time Format`, named `OPENTIME` on a particular Model Record.

## Properties

| Type | Name | Description
| --- | --- | --- 
| [DdsTimeFormat](/reference/expo/qsys-expo-model/dds-time-format.html) | TimeFormat | Gets or sets DDS Date Format (Defaults to ISO) |
