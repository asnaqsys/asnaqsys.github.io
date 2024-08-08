---
title: "DdsCheckboxFieldTagHelper class"
description: "Defines a toggle two-state input element. "
last_modified_at: 2024-08-08T21:42:22Z
---

Defines a toggle two-state input element.

**Namespace:** ASNA.QSys.Expo.Tags
**Assembly:** ASNA.QSys.Expo.Tags.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [TagHelper](https://learn.microsoft.com/en-us/dotnet/api/microsoft.aspnetcore.razor.taghelpers.taghelper?view=aspnetcore-8.0) --> [FieldBase](/reference/expo/qsys-expo-tags/field-base.html) --> [DdsFieldBase](/reference/expo/qsys-expo-tags/dds-field-base.html)
<br>
<br>

## Remarks

A [Checkbox](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/Input/checkbox) is a good candidate to replace the typical Legacy `Yes/No` - constant and field - combination, with a [User-Friendly](https://www.merriam-webster.com/dictionary/user-friendly) element.

For example, the following Legacy Markup:

```html
<DdsConstant Col="47" Text="Send Confirmation" />
<DdsCharField Col="58" ColSpan="2" For="CUSTREC.SFYN01" VirtualRowCol="18,27" />
<DdsConstant Col="61" Text="(Y/N)" />
```

Is a good candidate to be replaced by:

```html
<DdsCheckboxField Col="47" Text="Send Confirmation" For="CUSTREC.SFYN01" VirtualRowCol="18,27" />
```

On the Model source file, you would have to `decorate` the field, providing meta-information for the value we want to designate as the *checked* (or true) value, and which for *unchecked* (or false) value.

The Values attribute for `DdsCheckboxField` expects the first value to be the *checked* and the second the *unchecked*.

```cs
[Char(1)]
[Values(typeof(string), "Y", "N")]
public string SFYN01 { get; set; }
```

>Note: The Business Logic (program using the Display Page), does not need to change - or be recompiled -.

## Properties

| Type | Name | Description
| --- | --- | --- 
| [CharAttribute](/reference/expo/qsys-expo-model/char-attribute.html) | CharAttribute | Gets a CharAttribute defined by the field, from the Model. |
| [DecAttribute](/reference/expo/qsys-expo-model/dec-attribute.html) | DecAttribute | Gets a DecAttribute defined by the field, from the Model. |
| [FieldAttribute](/reference/expo/qsys-expo-model/field-attribute.html) | FieldAttribute | Gets a FieldAttribute defined by the field, from the Model. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | Text | Gets or sets a value to provide a description for the checkbox. |
