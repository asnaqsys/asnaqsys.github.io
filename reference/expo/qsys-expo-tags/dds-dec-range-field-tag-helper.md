---
title: "DdsDecRangeFieldTagHelper class"
description: "Defines an input element where numbers can be typed using a keyboard. The captured value will be posted as the value entered into a field.  "
last_modified_at: 2024-08-09T16:19:09Z
---

Defines an input element where numbers can be typed using a keyboard. The captured value will be posted as the value entered into a field. 

**Namespace:** ASNA.QSys.Expo.Tags
**Assembly:** ASNA.QSys.Expo.Tags.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [TagHelper](https://learn.microsoft.com/en-us/dotnet/api/microsoft.aspnetcore.razor.taghelpers.taghelper?view=aspnetcore-8.0) --> [FieldBase](/reference/expo/qsys-expo-tags/field-base.html) --> [DdsFieldBase](/reference/expo/qsys-expo-tags/dds-field-base.html) --> [DdsDecFieldTagHelper](/reference/expo/qsys-expo-tags/dds-dec-field-tag-helper.html)
<br>
<br>

## Remarks

It is recommended to specify the **Min** (minimum) and **Max** (maximum) values to properly define the valid range.

Whenever possible, it is also recommended to use a [pattern](https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes/pattern) attribute to validate the value, before the page can be submitted to the server. For example, for a field used as a four digit **PIN** (zero decimals), a pattern such as:

```html
pattern="\d{4,4}"
title="Valid PIN is four digits long."
```

sets the client-side validation to allow values that are only digits with a length of four. Notice also the use of attribute [title](https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes/pattern#usability) to assist the user when the Browser shows validation errors.

## Properties

| Type | Name | Description
| --- | --- | --- 
| [InteractionStyles](/reference/expo/qsys-expo-tags/interaction-styles.html) | InteractionStyle | Gets or sets how the user interacts with the visual component. |
| [Decimal](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types) | Max | Gets or sets the numeric range Maximum value. |
| [Decimal](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types) | Min | Gets or sets the numeric range Minimum value. |
| [NumericValueStyles](/reference/expo/qsys-expo-tags/numeric-value-styles.html) | NumericValueStyle | Gets or sets named style that determines the position of an optional numeric input box. |
| [Decimal](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types) | Step | Step by which the value is increased/decreased using Buttons or operating Slider. |
