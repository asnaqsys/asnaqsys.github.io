---
title: "DdsDecDateFieldTagHelper class"
description: "Defines an input element to capture Dates for fields defined as decimal values. "
last_modified_at: 2024-08-09T16:19:09Z
---

Defines an input element to capture Dates for fields defined as decimal values.

**Namespace:** ASNA.QSys.Expo.Tags
**Assembly:** ASNA.QSys.Expo.Tags.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [TagHelper](https://learn.microsoft.com/en-us/dotnet/api/microsoft.aspnetcore.razor.taghelpers.taghelper?view=aspnetcore-8.0) --> [FieldBase](/reference/expo/qsys-expo-tags/field-base.html) --> [DdsFieldBase](/reference/expo/qsys-expo-tags/dds-field-base.html) --> [DdsDateFieldTagHelper](/reference/expo/qsys-expo-tags/dds-date-field-tag-helper.html)
<br>
<br>

## Remarks

Legacy Applications more commonly used Dates as numeric values (with a particular [EditWord](/reference/expo/qsys-expo-model/edit-word.html), more than the proper [Date type](https://www.ibm.com/docs/en/i/7.3?topic=fields-example-date-time-timestamp-dds)).

During Migration patterns are observed to identify such dates and convert them to `DdsDecDateField` tag Helper to make the Calendar available on the Page (as if the proper [Date type](https://www.ibm.com/docs/en/i/7.3?topic=fields-example-date-time-timestamp-dds) was used).

This alone provides automated Modernization.

```html
<div Row="12" RowSpan="@SFLC_SubfilePage">
    @for (int rrn=0; rrn < Model.SFLC.SFL1.Count; rrn++)
    {
        int row = 12 + rrn;
        <DdsSubfileRecord RecordNumber="rrn" For="SFLC.SFL1">

            <DdsDecDateField Col="41+1" For="SFLC.SFL1[rrn].SFDELDATE" DateFormat="ISO" DateSeparator="-" SuppressLeadingZeroes=true Color="Green : !61 , DarkBlue : 61" />

        </DdsSubfileRecord>
    }
</div>
```

Note how the [DateFormat](/reference/expo/qsys-expo-model/dds-date-format.html) and `DateSeparator`are defined in the *Presentation* (markup) and not in the model (as it is done for [DdsDateField](/reference/expo/qsys-expo-tags/dds-date-field-tag-helper.html))

```cs
public class SFL1_Model : SubfileRecordModel
{
    .
    .
    .
    [Dec(8, 0)]
    public decimal SFDELDATE { get; private set; }
    .
    .
    .
}
```
The Model defines a [decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) type (which knows nothing about DateFormat or DateSeparators). The Application Logic will process the numeric value as usual.


## Properties

| Type | Name | Description
| --- | --- | --- 
| [DdsDateFormat](/reference/expo/qsys-expo-model/dds-date-format.html) | DateFormat | Gets the DateFormat from the Model. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | DateSeparator | Gets the Date Separator from the Model. |
| [DecAttribute](/reference/expo/qsys-expo-model/dec-attribute.html) | DecFieldAttribute | Gets the DecAttribute from the Model. |
| [FieldAttribute](/reference/expo/qsys-expo-model/field-attribute.html) | FieldAttribute | Gets the Decimal FieldAttribute from the Model. |

## Methods

| Signature | Description |
| --- | --- |
| [GetDateFormat()](#ddsdateformat-getdateformat) | Get the DdsDateFormat attribute from the Model.
| [GetDateSeparator()](#string-getdateseparator) | Gets the Data Separator from de Model.

### DdsDateFormat GetDateFormat()

Get the DdsDateFormat attribute from the Model.

```cs
DdsDateFormat GetDateFormat()
```

### string GetDateSeparator()

Gets the Data Separator from de Model.

```cs
string GetDateSeparator()
```
