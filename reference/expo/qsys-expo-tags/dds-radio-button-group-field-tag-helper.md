---
title: "DdsRadioButtonGroupFieldTagHelper class"
description: "Defines a group of radio-button elements. "
last_modified_at: 2024-08-08T21:42:22Z
---

Defines a group of radio-button elements.

**Namespace:** ASNA.QSys.Expo.Tags
**Assembly:** ASNA.QSys.Expo.Tags.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [TagHelper](https://learn.microsoft.com/en-us/dotnet/api/microsoft.aspnetcore.razor.taghelpers.taghelper?view=aspnetcore-8.0) --> [FieldBase](/reference/expo/qsys-expo-tags/field-base.html) --> [DdsFieldBase](/reference/expo/qsys-expo-tags/dds-field-base.html)
<br>
<br>

## Remarks

Legacy `IBM i` Applications commonly used input fields designed to accept only `Y` or `N` values. The Display Page would include something like the following markup:

```html
<div Row="18">
    <DdsConstant Col="7" Text="Send Confirmation:" />
    <DdsCharField Col="27" For="CUSTREC.SFYN01" Upper=true />
    <DdsConstant Col="29+5" Text="(Y/N)" />
</div>
```

With the field definition in the Model, like:

```cs
[Char(1)]
public string SFYN01 { get; set; }
```

This would display a Text line with `Send Confirmation:` followed by an input text box (accepting one character) and the text `(Y/N)` at the end of same line (to hint user that the two values expected where: `Y` or `N`).

A better implementation (compatible with the Program Logic), is to replace the markup with:

```html
<div Row="18">
    <DdsRadioButtonGroupField Col="7" Text="Send Confirmation" ValuesText="'Yes','No'" For="CUSTREC.SFYN01" />
</div>

```

And the Model definition with:

```cs
[Char(1)]
[Values(typeof(string), "Y", "N")]
public string SFYN01 { get; set; }
```

Notice how the Markup is reduced in significant ways:

1. Three Tag Helpers are reduced to one.
2. There is only one `Col` property (the radio button group components will be layout out automatically with best alignment possible).
3. Instead of having the User type a `Y` or `N`, the active radio graphic representation can be selected with the mouse, finger or arrow keys.
4. There is no need to be concerned about input text casing (with legacy interface, the Program logic may need to allow `Y` or `y` as equivalent responses).


>There are more uses for `DdsRadioButtonGroupField` other than `Yes/No` fields.

<br>
<br>

## Properties

| Type | Name | Description
| --- | --- | --- 
| [FieldAttribute](/reference/expo/qsys-expo-model/field-attribute.html) | FieldAttribute | Gets the FieldAttribute from the Model |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | NumberOfColumns | Gets or sets the number of columns used to render the element group |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | NumberOfRows | Gets or sets the number of rows used to render the element group |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | Text | Gets or sets the label describing the element group |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | ValuesText | Gets or sets a value that describes each radio button text. Each text description is single-quoted. List is comma separated. |
