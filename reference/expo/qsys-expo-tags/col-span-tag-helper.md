---
title: "ColSpanTagHelper class        | QSYS API Reference Guide"
description: "Provides a ColSpan tag helper to Razor elements.  "
last_modified_at: 2024-08-08T21:42:22Z
---

Provides a ColSpan tag helper to Razor elements. 

**Namespace:** ASNA.QSys.Expo.Tags
**Assembly:** ASNA.QSys.Expo.Tags.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [TagHelper](https://learn.microsoft.com/en-us/dotnet/api/microsoft.aspnetcore.razor.taghelpers.taghelper?view=aspnetcore-8.0)
<br>
<br>

## Remarks

Legacy [DDS for display files](https://www.ibm.com/docs/en/i/7.1?topic=dds-display-files) described field and constant Display positions using a grid-like row and column coordinate system. Typically a field was described with a `start-position` spanning to an `end-position` according to its width (or field length).

Sometimes it is desirable the override the `end-position` by providing a `Column Span` value that extends the `bounding-box` of the field or constant beyond the *natural* calculation of the `end-position` (as in `start_position + length`).

For example, the constant "Selection" in the markup below, has a *character* length of `9`. Without the `ColSpan` property, the `end-position` would be calculated as: `4+4+9 = 17`. Instead we want the constant's bounding box to extend to position `23` (that is `4+4+15`).

>Extending a [DdsField's](/reference/model/qsys-expo-tags/dds-field-base.html) or [DdsConstant's](/reference/model/qsys-expo-tags/dds-constant-tag-helper.html) width may be desirable when a [CSS](https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes/class) style wants to be applied (such as [background-color](https://developer.mozilla.org/en-US/docs/Web/CSS/background-color)).  

```html
    <div Row="3">
        <DdsConstant Col="4+4" ColSpan="15" Text="Selection" Color="DarkBlue" />
        .
        .
        .
    </div>
```

## Properties

| Type | Name | Description
| --- | --- | --- 
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | ColSpan | Gets or sets a value that indicates the width positions within a Row, to calculate Column end. |
