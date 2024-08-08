---
title: "DdsDateFieldTagHelper class   | QSYS API Reference Guide"
description: "Defines an input element to capture Dates. "
last_modified_at: 2024-08-08T21:42:22Z
---

Defines an input element to capture Dates.

**Namespace:** ASNA.QSys.Expo.Tags
**Assembly:** ASNA.QSys.Expo.Tags.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [TagHelper](https://learn.microsoft.com/en-us/dotnet/api/microsoft.aspnetcore.razor.taghelpers.taghelper?view=aspnetcore-8.0) --> [FieldBase](/reference/expo/qsys-expo-tags/field-base.html) --> [DdsFieldBase](/reference/expo/qsys-expo-tags/dds-field-base.html)
<br>
<br>

## Remarks

Date is a complex data type. It presents several presentation challenges (particularly with respect to [Localization](https://en.wikipedia.org/wiki/Internationalization_and_localization)). IBM i defined [Date Formats](https://www.ibm.com/docs/en/i/7.3?topic=design-date-formats) in a way that is not common for Web Development.

The use of Selectable Calendar (native on a Web Browser, or Customized by QSys Expo) is very desirable and presents an immediate level of Modernization on a Legacy Application.

The `DdsDateField` Tag Helper along with the Model definition of the field, provide a very convenient way preserve Application Logic with the IBM i defined [Date Formats](https://www.ibm.com/docs/en/i/7.3?topic=design-date-formats) specification.

The following is an excerpt of a Display Page, with the markup needed to define the layout of a Date:

```html
<div Row="4">
    <DdsConstant Col="23+2" Text="Date:" />
    <DdsDateField Col="29+2" For="SFLC.SORDDATE"  Comment="ORDER DATE" />
</div>
```

The following is the corresponding Model field definition:

```cs
public class SFLC_Model : SubfileControlModel
{
    public List<SFL1_Model> SFL1 { get; set; } = new List<SFL1_Model>();
    .
    .
    .
    [Date(DateFormat = DateAttribute.DdsDateFormat.USA)]
    public DateTime SORDDATE { get; private set; } // ORDER DATE

}
```

Notice how the [DateFormat attribute](/reference/expo/qsys-expo-model/date-attribute.html) is defined using the IBM i definition. (The default date-separator is `-`, it can be changed using `DateSeparator` attribute).

## Properties

| Type | Name | Description
| --- | --- | --- 
| [DateAttribute](/reference/expo/qsys-expo-model/date-attribute.html) | DateFieldAttribute | Gets the DateAttribute from the Model. |
| [FieldAttribute](/reference/expo/qsys-expo-model/field-attribute.html) | FieldAttribute | Gets the Date FieldAttribute from the Model. |
| [DdsDayNames](/reference/expo/qsys-expo-tags/dds-day-names.html) | FirstDayOfWeek | Gets or sets the countries first day of the week. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | MapValues | Gets or sets a value that indicates a list of semicolon-separated output value mappings. Format of each mapping is 'program-value,display-value'. |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | UseNativePicker | Gets or sets a value that indicates if the Browser's date picker should be used when capturing a date. |

## Methods

| Signature | Description |
| --- | --- |
| [GetDateFormat()](#ddsdateformat-getdateformat) | Gets the DateFormat from the Model.
| [GetDateSeparator()](#string-getdateseparator) | Gets the Date Separator from the Model.

### DdsDateFormat GetDateFormat()

Gets the DateFormat from the Model.

```cs
DdsDateFormat GetDateFormat()
```

### string GetDateSeparator()

Gets the Date Separator from the Model.

```cs
string GetDateSeparator()
```
