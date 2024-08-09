---
title: "DdsRecordTagHelper class      | QSYS API Reference Guide"
description: "Defines a Display record where fields or constants are contained to display application data. "
last_modified_at: 2024-08-09T16:19:09Z
---

Defines a Display record where fields or constants are contained to display application data.

**Namespace:** ASNA.QSys.Expo.Tags
**Assembly:** ASNA.QSys.Expo.Tags.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [TagHelper](https://learn.microsoft.com/en-us/dotnet/api/microsoft.aspnetcore.razor.taghelpers.taghelper?view=aspnetcore-8.0) --> [RecordBaseTagHelper](/reference/expo/qsys-expo-tags/record-base-tag-helper.html)
<br>
<br>


## Remarks

A `Display Record Format` defines an horizontal Page segment. A Display Page may contain several `Display Record Formats`, but frequently only a few are made `Active` at a time, according to Application Logic.

Application Logic makes Display Records Formats `Active` by `Writing` to that Record. It is also possible to make Records `In-Active` by **Erasing** them, that is, by including their names in the comma-separated name list used as the value of the property [EraseFormats](/reference/expo/qsys-expo-model/base-record-attribute.html#properties). (When the Display Records Format with `EraseFormats` is written, it first **Erases* the other records. This feature was called Display Overlaying).

Each Record is made up by horizontal `Rows` taking the full width of the `main` HTML element. Each Row has a predetermined height (based on the Font size).

There are two Tag Helpers associated with Display Record Formats:

1. `DdsRecord` Tag Helper.
2. [DdsSubfileControl](/reference/expo/qsys-expo-tags/dds-subfile-control-tag-helper.html) Tag Helper.

The first defines an horizontal Page segment where Rows can contain only `DdsField`(s) - nested Records are not allowed-. The second, defines an horizontal Page segment where Rows can contain `DdsField`(s) as well as possibly one nested Record - spanning more than one row defining a segment that can scroll up or down -. The nested Record format that may be contained in a [DdsSubfileControl](/reference/expo/qsys-expo-tags/dds-subfile-control-tag-helper.html) is called the [DdsSubfileRecord](/reference/expo/qsys-expo-tags/dds-record-tag-helper.html). 

>If more than one [DdsSubfileRecord](/reference/expo/qsys-expo-tags/dds-record-tag-helper.html) is desired, each needs to define its own [DdsSubfileControl](/reference/expo/qsys-expo-tags/dds-subfile-control-tag-helper.html) Tag Helper.

The following is a sample specification of a `Display Record Format` named `CUSTREC` as Markup:

```html
<DdsRecord For="CUSTREC" KeyNames="ENTER 'Enter'; F4 'Prompt'; F6 'New'; F11 'Delete'; F12 'Cancel';">
    <div Row="1">
        <DdsConstant Col="2" Text=@System.Environment.UserName />
        <DdsConstant Col="29+5" Text="M5 Customer Maintenance" Color="DarkBlue" />
        <DdsConstant Col="64+5" Text=@DateTime.Today.ToString(@"MM\/ dd\/ yy") />
        <DdsConstant Col="73+5" Text=@DateTime.Now.ToString("HH: mm: ss") />
    </div>
    <div Row="2">
        <DdsCharField Col="2" For="CUSTREC.SCPGM" Upper=true />
    </div>
    <div Row="5">
        <DdsDecField Col="27" For="CUSTREC.SFCUSTNO" Color="DarkBlue" EditCode="Z" Comment="CUSTOMER NUMBER" />
        <DdsCharField Col="35+5" For="CUSTREC.SFOLDNAME" Upper=true Color="DarkBlue" />
    </div>
    <div Row="7">
        <DdsConstant Col="20" Text="Name:" />
        <DdsCharField Col="27" For="CUSTREC.SFNAME" VirtualRowCol="7,27" PositionCursor="40" />
    </div>
    <div Row="8">
        <DdsConstant Col="17" Text="Address:" />
        <DdsCharField Col="27" For="CUSTREC.SFADDR1" VirtualRowCol="8,27" PositionCursor="41" />
    </div>
    <div Row="9">
        <DdsCharField Col="27" For="CUSTREC.SFADDR2" VirtualRowCol="9,27" />
    </div>
    <div Row="10">
        <DdsConstant Col="20" Text="City:" />
        <DdsCharField Col="27" For="CUSTREC.SFCITY" VirtualRowCol="10,27" PositionCursor="42" />
    </div>
    <div Row="11">
        <DdsConstant Col="15" Text="State/Zip:" />
        <DdsCharField Col="27" For="CUSTREC.SFSTATE" Upper=true VirtualRowCol="11,27" PositionCursor="43" />
        <DdsConstant Col="30+5" Text="(F4)" Color="Blue" />
        <DdsCharField Col="37+5" For="CUSTREC.SFPOSTCODE" Upper=true VirtualRowCol="11,37" />
    </div>
    <div Row="13">
        <DdsConstant Col="21" Text="Fax:" />
        <DdsDecField Col="27" For="CUSTREC.SFFAX" VirtualRowCol="13,27" EditWord="(   )   -    " />
    </div>
    <div Row="14">
        <DdsConstant Col="19" Text="Phone:" />
        <DdsCharField Col="27" For="CUSTREC.SFPHONE" Upper=true VirtualRowCol="14,27" />
    </div>
    <div Row="15">
        <DdsConstant Col="18" Text="Status:" />
        <DdsCharField Col="27" For="CUSTREC.SFSTATUS" Upper=true VirtualRowCol="15,27" PositionCursor="44" />
        <DdsConstant Col="30+5" Text="(F4)" Color="Blue" />
    </div>
    <div Row="16">
        <DdsConstant Col="12" Text="Contact Name:" />
        <DdsCharField Col="27" For="CUSTREC.SFCONTACT" Upper=true VirtualRowCol="16,27" />
    </div>
    <div Row="17">
        <DdsConstant Col="11" Text="Contact eMail:" />
        <DdsCharField Col="27" For="CUSTREC.SFCONEMAL" Upper=true VirtualRowCol="17,27" />
    </div>
    <div Row="18">
        <DdsConstant Col="7" Text="Send Confirmation:" />
        <DdsCharField Col="27" For="CUSTREC.SFYN01" Upper=true VirtualRowCol="18,27" />
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

>Note how Rows `3, 4, 6, 12, 19, 24 ... 27` are skipped. Those are `Empty Rows` that still show as `White Empty Space` each with the height of a `Regular Row`.

Just for completeness, its corresponding Record Model, would look like:

```cs
[
    Record(FunctionKeys = "F4 04;F6 06:!30;F11 11:!30;F12 12",
        EraseFormats = "SFLC KEYS SALESREC"
    )
]
public class CUSTREC_Model : RecordModel
{
    [Char(10)]
    private string CSRREC  { get => CursorLocationFormatName; set { } }

    [Char(10)]
    private string CSRFLD  { get => CursorLocationFieldName; set { } }

    [Char(10)]
    public string SCPGM { get; private set; }

    [Dec(6, 0)]
    public decimal SFCUSTNO { get; private set; } // CUSTOMER NUMBER

    [Char(40)]
    public string SFOLDNAME { get; private set; }

    [Char(40)]
    public string SFNAME { get; set; }

    [Char(35)]
    public string SFADDR1 { get; set; }

    [Char(35)]
    public string SFADDR2 { get; set; }

    [Char(30)]
    public string SFCITY { get; set; }

    [Char(2)]
    public string SFSTATE { get; set; }

    [Char(10)]
    public string SFPOSTCODE { get; set; }

    [Dec(10, 0)]
    public decimal SFFAX { get; set; }

    [Char(20)]
    public string SFPHONE { get; set; }

    [Char(1)]
    public string SFSTATUS { get; set; }

    [Char(40)]
    public string SFCONTACT { get; set; }

    [Char(40)]
    public string SFCONEMAL { get; set; }

    [Char(1)]
    public string SFYN01 { get; set; }
}
```

>Note that when writing `Display Record Format` **CUSTREC** the following *other* `Display Record Formats`: `SFLC, KEYS and SALESREC` will be made `Inactive` (i.e. Removed from the Display Page).

## Properties

| Type | Name | Description
| --- | --- | --- 
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | CursorLocation | Gets or sets a conditional expression indicating where the Cursor should be located when presenting the Page. Format is 'Row,Col' or 'Row,Col:Indicator Expression'. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | ExcludeEmptyRows | Gets or sets a comma separated list of unused Row numbers that should be excluded from those DIV that get created to fill empty vertical space. Entries may also be ranges using - separator. |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | IsWindowRecord | Get whether the record format is a Window record. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | KeyNames | Gets or sets the display key name collection for the Record. Key names are separated by semicolon. |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | StretchConstantText | Gets or sets a value indicating if text for constants in the record are to be stretched-out to fill column positions |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | WindowHeightRows | Gets or sets the window height. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | WindowLeftCol | Gets or sets the left horizontal position of the window. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | WindowTitle | Gets or sets the label for the Window record's Title  |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | WindowTopRow | Gets or sets the top vertical position of the window. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | WindowWidthCols | Gets or sets the window width. |
