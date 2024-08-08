---
title: "DdsConstantTagHelper class    | QSYS API Reference Guide"
description: "Defines an constant label. "
last_modified_at: 2024-08-08T21:42:22Z
---

Defines an constant label.

**Namespace:** ASNA.QSys.Expo.Tags
**Assembly:** ASNA.QSys.Expo.Tags.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [TagHelper](https://learn.microsoft.com/en-us/dotnet/api/microsoft.aspnetcore.razor.taghelpers.taghelper?view=aspnetcore-8.0) --> [FieldBase](/reference/expo/qsys-expo-tags/field-base.html)
<br>
<br>

## Remarks

A constant Label is one of the simplest elements on a Display Page. There is however one aspect that may be overlooked with noticeable consequences that is worth discussing.

Legacy applications typically use constant labels to:

1. Display Page titles (including user-name, system date and time). 
2. Name input fields.
3. Show valid `Option` codes (legacy way to show menus in a label).
4. Add headings to Tables (subfiles).

The following `DdsConstants` are used in a `DdsSubfileControl` record in a Sample Application:

```html
<div Row="1">
    <DdsConstant Col="2" Text=@System.Environment.UserName />
    <DdsConstant Col="31+1" Text="M5 Customer Inquiry" Color="DarkBlue" />
    <DdsConstant Col="64+1" Text=@DateTime.Today.ToString(@"MM\/ dd\/ yy") />
    <DdsConstant Col="73+1" Text=@DateTime.Now.ToString("HH: mm: ss") />
</div>
<div Row="2">
    <DdsConstant Col="52+1" Text="Position to name:" />
    <DdsCharField Col="70+1" For="SFLC.SETNAME" VirtualRowCol="2,70" tabIndex=1 />
</div>
<div Row="4">
    <DdsConstant Col="3" Text="2=Update   3=Display sales    5=Delivery Addresses    7=Create sales record     9=Print" Color="Blue" />
</div>
<div Row="5">
    <DdsConstant Col="3" Text="sales (Online)  10=Print sales (Batch)    11=Orders" Color="Blue" />
</div>
<div Row="7">
    <DdsConstant Col="3" Text="Sel" Color="DarkBlue" Underline="*True" />
    <DdsConstant Col="7+1" Text="Custno" Color="DarkBlue" Underline="*True" />
    <DdsConstant Col="14+1" Text="Customer Name" Color="DarkBlue" Underline="*True" />
    <DdsConstant Col="55+1" Text="City / State / Zip" Color="DarkBlue" Underline="*True" />
</div>
```

* Row "1" shows the Display Page Title along with Username, Date and Time of the server. Notice how the column position on each element, is laying ot the line while attempting to *center* the title `M5 Customer Inquiry` title. 

The Legacy calculations to center the title were: 
Col = (80 - 19) / 2
Col = 31 (*rounded to the next whole number*)

*Where*, 80 was the Terminal width, 19 is the length of `M5 Customer Inquiry` (assuming [Monospaced fonts](https://en.wikipedia.org/wiki/Monospaced_font))

This calculation **does not work well** on a Browser with *open* page width and [Proportional spaced fonts](https://en.wikipedia.org/wiki/Monospaced_font)

* Row "2" shows input-field `SETNAME` labeled to the left as `"Position to name:`, starting at Column 52. The Legacy intention was to *right-justify* the label, to have the colon (`:`) close to the input field. Same assumptions as before, regarding width of Page and [Monospaced fonts](https://en.wikipedia.org/wiki/Monospaced_font)

* Rows "4" and "5" show a *"menu"* of available valid *Options*: 2, 3, 5, 7, 9, 10 and 11. Notice option `9 = Print sales (Online)`, a label wrapping text from Row "4" to Row "5" ([See a screenshot here](https://asna.github.io/SunFarm/avoid-constant-stretching/)). The additional blanks between options in the label, for example 
`2=Update   3=Display sales` has a special purpose, that is lost with the obsolete assumptions.

* Finally, Row "7" is the column headings for the subfile (table), which present several challenges to appeared aligned, starting with the fact that the input element for `Sel` (selection) was transformed into a wider drop-down list. ([See a screenshot here](https://asna.github.io/SunFarm/avoid-constant-stretching/)).

>Forcing ALL fonts to [Monospaced fonts](https://en.wikipedia.org/wiki/Monospaced_font) attempting to solve the mis-alignment challenge, quickly proves to be a *oversimplification* with unwanted detriment in the Application look (old Legacy) which most consider **unacceptable**.

A better solution (enabled by default) is implemented by means of the property `StretchConstantText` below.

> `StretchConstantText` is a technique using a [Proportionally space font](https://en.wikipedia.org/wiki/Monospaced_font) - *normal* Web font - with a CSS style that adds [letter-spacing](https://developer.mozilla.org/en-US/docs/Web/CSS/letter-spacing). The runtime calculation for the amount of `letter-spacing` added, is carefully selected with the *best approximation* considering Legacy measurement assumptions.


## Properties

| Type | Name | Description
| --- | --- | --- 
| [Nullable\<Boolean\>](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/nullable-value-types) | StretchConstantText | Gets or sets a value that indicates if letter-spacing should be computed to make text rendering use the full width of the field definition. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | Text | Gets or sets the text of the constant.  |
