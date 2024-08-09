---
title: "ColTagHelper class            | QSYS API Reference Guide"
description: "Provides a Col tag helper to Razor elements.  "
last_modified_at: 2024-08-09T16:19:09Z
---

Provides a Col tag helper to Razor elements. 

**Namespace:** ASNA.QSys.Expo.Tags
**Assembly:** ASNA.QSys.Expo.Tags.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [TagHelper](https://learn.microsoft.com/en-us/dotnet/api/microsoft.aspnetcore.razor.taghelpers.taghelper?view=aspnetcore-8.0)
<br>
<br>

## Remarks

Legacy [DDS for display files](https://www.ibm.com/docs/en/i/7.1?topic=dds-display-files) described field and constant Display positions using a grid-like row and column coordinate system. Typically a field was described with a `start-position` within the row.

Such `start-position` is indicated with *string expression that evaluates* to an integer value `>= 1`. This value is indicated as the `Col` position.

> Legacy [DDS for display files](https://www.ibm.com/docs/en/i/7.1?topic=dds-display-files) had a limitation of column positions according to the Terminal Device capabilities, typically 80 and 132. This limitation no longer applies, since a Web Page can scroll horizontally.

The following markup, describes the layout of several [DdsConstants](/reference/expo/qsys-expo-tags/dds-constant-tag-helper.html) and [DdsFields](/reference/expo/qsys-expo-tags/dds-field-base.html) within a [DdsRecord](/reference/expo/qsys-expo-tags/dds-record-tag-helper.html):

```html
<DdsRecord For="CUSTREC" KeyNames="ENTER 'Enter'; F4 'Prompt'; F6 'New'; F11 'Delete'; F12 'Cancel';">
    <div Row="1">
        <DdsConstant Col="2" Text=@System.Environment.UserName />
        <DdsConstant Col="29+5" Text="M5 Customer Maintenance" Color="DarkBlue" />
        <DdsConstant Col="64+5" Text=@DateTime.Today.ToString(@"MM\/ dd\/ yy") />
        <DdsConstant Col="73+5" Text=@DateTime.Now.ToString("HH: mm: ss") />
    </div>
    <div Row="2">
        <DdsCharField Col="2" For="CUSTREC.SCPGM" Upper=true VirtualRowCol="2,2" />
    </div>
    <div Row="5">
        <DdsDecField Col="27" For="CUSTREC.SFCUSTNO" VirtualRowCol="5,27" Color="DarkBlue" EditCode="Z" Comment="CUSTOMER NUMBER" />
        <DdsCharField Col="35+5" For="CUSTREC.SFOLDNAME" Upper=true VirtualRowCol="5,35" Color="DarkBlue" />
    </div>
    <div Row="7">
        <DdsConstant Col="20" Text="Name:" />
        <DdsCharField Col="27" For="CUSTREC.SFNAME" VirtualRowCol="7,27" PositionCursor="40" tabIndex=2 />
    </div>
    <div Row="8">
        <DdsConstant Col="17" Text="Address:" />
        <DdsCharField Col="27" For="CUSTREC.SFADDR1" VirtualRowCol="8,27" PositionCursor="41" tabIndex=3 />
    </div>
    <div Row="9">
        <DdsCharField Col="27" For="CUSTREC.SFADDR2" VirtualRowCol="9,27" tabIndex=4 />
    </div>
    <div Row="10">
        <DdsConstant Col="20" Text="City:" />
        <DdsCharField Col="27" For="CUSTREC.SFCITY" VirtualRowCol="10,27" PositionCursor="42" tabIndex=5 />
    </div>
    <div Row="11">
        <DdsConstant Col="15" Text="State/Zip:" />
        <DdsCharField Col="27" For="CUSTREC.SFSTATE" Upper=true VirtualRowCol="11,27" PositionCursor="43" tabIndex=6 />
        <DdsConstant Col="30+5" Text="(F4)" Color="Blue" />
        <DdsCharField Col="37+5" For="CUSTREC.SFPOSTCODE" Upper=true VirtualRowCol="11,37" tabIndex=7 />
    </div>
    <div Row="13">
        <DdsConstant Col="21" Text="Fax:" />
        <DdsDecField Col="27" For="CUSTREC.SFFAX" VirtualRowCol="13,27" EditWord="(   )   -    " tabIndex=8 />
    </div>
    <div Row="14">
        <DdsConstant Col="19" Text="Phone:" />
        <DdsCharField Col="27" For="CUSTREC.SFPHONE" Upper=true VirtualRowCol="14,27" tabIndex=9 />
    </div>
    <div Row="15">
        <DdsConstant Col="18" Text="Status:" />
        <DdsCharField Col="27" For="CUSTREC.SFSTATUS" Upper=true VirtualRowCol="15,27" PositionCursor="44" tabIndex=10 />
        <DdsConstant Col="30+5" Text="(F4)" Color="Blue" />
    </div>
    <div Row="16">
        <DdsConstant Col="12" Text="Contact Name:" />
        <DdsCharField Col="27" For="CUSTREC.SFCONTACT" Upper=true VirtualRowCol="16,27" tabIndex=11 />
    </div>
    <div Row="17">
        <DdsConstant Col="11" Text="Contact eMail:" />
        <DdsCharField Col="27" For="CUSTREC.SFCONEMAL" Upper=true VirtualRowCol="17,27" tabIndex=12 />
    </div>
    <div Row="18">
        <DdsConstant Col="7" Text="Send Confirmation:" />
        <DdsCharField Col="27" For="CUSTREC.SFYN01" Upper=true VirtualRowCol="18,27" tabIndex=13 />
        <DdsConstant Col="29+5" Text="(Y/N)" />
    </div>
    <div Row="23">
        <DdsConstant Col="3" Text="F4=Prompt" Color="Blue" />
        <DdsConstant Col="15" Text="F6=New customer" VisibleCondition="!30" Color="Blue" />
        <DdsConstant Col="33+5" Text="F11=Remove customer" VisibleCondition="!30" Color="Blue" />
        <DdsConstant Col="55+5" Text="F12=Cancel" Color="Blue" />
    </div>
</DdsRecord>
```

Notes:

1. The `Col` is a [TagHelper](https://docs.microsoft.com/en-us/dotnet/api/microsoft.aspnetcore.razor.taghelpers.taghelper) derived class, but it is used as a **property** for different Tag Helpers (including HTML elements). This is possible thanks to [Microsoft Tag Helper technology](https://docs.microsoft.com/en-US/aspnet/core/mvc/views/tag-helpers/intro). For the purpose of laying out elements on a Expo Display Page, it is safe to treat `Col` as a *string* property.

2. The type of value `Col` is a  [String](https://docs.microsoft.com/en-us/dotnet/api/system.globalization.stringinfo) that contains a `simple arithmetic` expression, that allows addition and subtraction. The expression should evaluate to an integer value `>= 1`.

3. Migrated Display Pages (directly from Legacy [DDS for display files](https://www.ibm.com/docs/en/i/7.1?topic=dds-display-files)), typically show the `Col` expression as a *binary* addition, where the first operand is the *original* column position and the second is the incremental adjustment required to accommodate HTML intrinsic graphical elements, for example, [HTML Dropdown lists](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/select) have a clickable *down* button to the right. This added button forces the width of the field to grow, and elements to the right will need to be offset accordingly.  To make it easier to locate the elements when searching for them, using the original start-position, the *original* value is preserved in the expression, during migration.  There are other scenarios where keeping the legacy start-position is also convenient. 

## Properties

| Type | Name | Description
| --- | --- | --- 
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | Col | Gets or sets a value that indicates the horizontal position within a Row. |
