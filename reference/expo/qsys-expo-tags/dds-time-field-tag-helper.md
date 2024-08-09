---
title: "DdsTimeFieldTagHelper class   | QSYS API Reference Guide"
description: "Defines an input element to capture Times. "
last_modified_at: 2024-08-09T17:26:18Z
---

Defines an input element to capture Times.

**Namespace:** ASNA.QSys.Expo.Tags
**Assembly:** ASNA.QSys.Expo.Tags.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [TagHelper](https://learn.microsoft.com/en-us/dotnet/api/microsoft.aspnetcore.razor.taghelpers.taghelper?view=aspnetcore-8.0) --> [FieldBase](/reference/expo/qsys-expo-tags/field-base.html) --> [DdsFieldBase](/reference/expo/qsys-expo-tags/dds-field-base.html)
<br>
<br>

## Remarks

To define a field to capture or display time of day values, use the [DdsTimeField](/reference/expo/qsys-expo-tags/dds-time-field-tag-helper.html) Tag Helper.

For example, the following markup defines a span text element for the field `ARRIVEAT` in the `PACKAGE` record (defined in the Model).

```html
<div Row="7">
    .
    .
    .
    <DdsTimeField Col="27" For="PACKAGE.ARRIVEAT" />
</div>
```

The field `ARRIVEAT` is defined in the Model file, like so:

```cs
public class PACKAGE_Model : RecordModel
{
    .
    .
    [Time(USA)]
    public DateTime ARRIVEAT { get; private set; }


```

Note how the `Time` attribute defines the [format of the Time field](/reference/expo/qsys-expo-model/dds-time-format.html) to be USA. The property accessors define the field `Usage`. In this example, the field is public get and private set, defining it as `OUTPUT Only`.

## Properties

| Type | Name | Description
| --- | --- | --- 
| [FieldAttribute](/reference/expo/qsys-expo-model/field-attribute.html) | FieldAttribute | Gets the Time FieldAttribute from the Model. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | MapValues | Gets or sets a value that indicates a list of semicolon-separated output value mappings. Format of each mapping is 'program-value,display-value'. |
| [TimeAttribute](/reference/expo/qsys-expo-model/time-attribute.html) | TimeFieldAttribute | Gets the Time Attribute from the Model. |

## Methods

| Signature | Description |
| --- | --- |
| [GetTimeFormat()](#ddstimeformat-gettimeformat) | Gets the DateFormat from the Model.

### DdsTimeFormat GetTimeFormat()

Gets the DateFormat from the Model.

```cs
DdsTimeFormat GetTimeFormat()
```
