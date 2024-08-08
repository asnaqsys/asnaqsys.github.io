---
title: "DdsCharFieldTagHelper class   | QSYS API Reference Guide"
description: "Defines an input element where characters can be typed using a keyboard. The captured value will be posted as the value entered into a field.  "
last_modified_at: 2024-08-08T21:42:22Z
---

Defines an input element where characters can be typed using a keyboard. The captured value will be posted as the value entered into a field. 

**Namespace:** ASNA.QSys.Expo.Tags
**Assembly:** ASNA.QSys.Expo.Tags.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [TagHelper](https://learn.microsoft.com/en-us/dotnet/api/microsoft.aspnetcore.razor.taghelpers.taghelper?view=aspnetcore-8.0) --> [FieldBase](/reference/expo/qsys-expo-tags/field-base.html) --> [DdsFieldBase](/reference/expo/qsys-expo-tags/dds-field-base.html)
<br>
<br>

## Remarks

To define an input-capable [Fixed String](/reference/runtime/qsys-runtime/fixed-string-1.html), use the `DdsCharField` Tag Helper.

For example, the following markup defines an input text element for the field `SFNAME` in the `CUSTREC` record (defined in the Model).

```html
<div Row="4">
    .
    .
    .
    <DdsCharField Col="27" For="CUSTREC.SFNAME" PositionCursor="67"/>
</div>
```

The field `SFNAME` is defined in the Model file, like so:

```cs
public class CUSTREC_Model : RecordModel
{
    .
    .
    .
    [Char(40)]
    public string SFNAME { get; set; }

```

Note how the `Char` attribute defines the fixed length of 40 characters. The property accessors define the field `Usage`. In this example, the field is public get and public set, defining it as `BOTH` readable as well as writable.



## Properties

| Type | Name | Description
| --- | --- | --- 
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | LimitMaxLength | Gets or sets a value that indicates whether to set a limit on the maximum characters allowed to be typed on the field. Defaults to true. When true, the maximum allowed characters will be set to the Length of the field. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | MessageIdExpression | Gets or sets a conditionalal property string that indicates which message of a message file will be used to extract the text associated with the message. Format is comma-separated list of 'MessageID MessageFileName[:optional indicator expression]'. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | MultilineColWidth | Gets or sets a value that indicates the width of the multi-line text area expressed in legacy character count. When used in a Browser, more characters may be entered per line, but the box will have the legacy pixel width.   |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | SpellCheck | Gets or sets a value that indicates the HTML spellcheck attribute used during rendering. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | ValuesText | Gets or sets a value that describes valid display values. Each text description is single-quoted. List is comma separated. ValuesText can be used to display the field as a dropdown box. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | ValuesTextOptionSeparator | Gets or sets the string that will be used to separate Value and Text for ValuesText. Defaults to not prepend values to ValuesText. |

## Methods

| Signature | Description |
| --- | --- |
| [getFieldValue()](#string-getfieldvalue) | Gets the value of the field from the Model.

### string getFieldValue()

Gets the value of the field from the Model.

```cs
string getFieldValue()
```
