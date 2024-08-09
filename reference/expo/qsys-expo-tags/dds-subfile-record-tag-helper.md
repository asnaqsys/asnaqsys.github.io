---
title: "DdsSubfileRecordTagHelper class"
description: "Defines a Subfile record element "
last_modified_at: 2024-08-09T17:26:17Z
---

Defines a Subfile record element

**Namespace:** ASNA.QSys.Expo.Tags
**Assembly:** ASNA.QSys.Expo.Tags.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [TagHelper](https://learn.microsoft.com/en-us/dotnet/api/microsoft.aspnetcore.razor.taghelpers.taghelper?view=aspnetcore-8.0) --> [RecordBaseTagHelper](/reference/expo/qsys-expo-tags/record-base-tag-helper.html)
<br>
<br>

## Remarks

The `DdsSubfileRecord` Tag Helper is a Display element that can be repeated inside a [DdsSubfileControl](/reference/expo/qsys-expo-tags/dds-subfile-control-tag-helper.html) to bind an element to a record collection in the Model. Subfile records have an associated [Relative Record Number](https://www.ibm.com/support/pages/ibm-rpg400-example-relative-record-number-file-processing).

[Razor Language](https://docs.microsoft.com/en-us/aspnet/core/mvc/views/razor) allows a [Razor Page](https://docs.microsoft.com/en-us/aspnet/core/razor-pages) to express a a variable number of Tag Helpers to appear on a Display Page, defining a headless Table starting at a particular `DIV` row, spanning a `Page` number of rows (down), binding collection elements defined in the Model, using an [RRN](https://www.ibm.com/support/pages/ibm-rpg400-example-relative-record-number-file-processing). 

The following examples shows the markup for a Subfile collection called "SFL1" in the Model.

```html
@{
    int SFLC_SubfilePage = 10;
}
<DdsSubfileControl For="SFLC" KeyNames="ENTER 'Enter'; F6 'Add'; PageUp; PageDown;" SubfilePage="@SFLC_SubfilePage" CueCurrentRecord=true ClickSetsCurrentRecord=true>
    .
    .
    .
    <div Row="12" RowSpan="@SFLC_SubfilePage">
        @for (int rrn=0; rrn < Model.SFLC.SFL1.Count; rrn++)
        {
            <DdsSubfileRecord RecordNumber="rrn" For="SFLC.SFL1">
                <DdsDecField Col="2" For="SFLC.SFL1[rrn].SFSEL" VisibleCondition="!( 60 )" VirtualRowCol="@row,2" EditCode="Z" ValuesText="'0','2','3','6'" tabIndex=1 />
                <DdsDecField Col="7+1" For="SFLC.SFL1[rrn].SFORDNUM" Color="Green : !61 , DarkBlue : 61"  EditCode="Z" />
                <DdsDateField Col="19+1" For="SFLC.SFL1[rrn].SFORDDATE"  Color="Green : !61 , DarkBlue : 61"  Comment="ORDER DATE" />
                <DdsDateField Col="30+1" For="SFLC.SFL1[rrn].SFSHPDATE"  Color="Green : !61 , DarkBlue : 61"  Comment="PRICE" />
                <DdsDecDateField Col="41+1" For="SFLC.SFL1[rrn].SFDELDATE" DateFormat="ISO" DateSeparator="-" SuppressLeadingZeroes=true Color="Green : !61 , DarkBlue : 61"  />
                <DdsDecField Col="52+1" For="SFLC.SFL1[rrn].SFORDAMT" Color="Green : !61 , DarkBlue : 61"  EditCode="A" />
                <DdsCharField Col="71+1" For="SFLC.SFL1[rrn].SFFILESTAT" Upper=true Color="Green : !61 , DarkBlue : 61"  />
                <DdsDecField Col="76+1" For="SFLC.SFL1[rrn].SFSHPVIA" Color="Green : !61 , DarkBlue : 61"  EditCode="Z" />
            </DdsSubfileRecord>
        }
    </div>
</DdsSubfileControl>
```

For reference, the Model on this example, is defined by:

```cs
[
    SubfileControl(ClearRecords : "90",
        FunctionKeys = "F6 06;PageUp 51:!76;PageDown 50:!77",
        DisplayFields = "!90",
        DisplayRecords = "!90",
        Size = 11
    )
]
public class SFLC_Model : SubfileControlModel
{
    public List<SFL1_Model> SFL1 { get; set; } = new List<SFL1_Model>();

    [Char(50)]
    public string SCRCUST { get; private set; } // CUSTOMER NBR AND NAME

    [Char(20)]
    public string SCRPHONE { get; private set; }

    [Char(35)]
    public string CMADDR1 { get; private set; }

    [Char(14)]
    public string SCRFAX { get; private set; } // FAX NUMBER

    [Char(35)]
    public string CMADDR2 { get; private set; }

    [Char(1)]
    public string CMACTIVE { get; private set; }

    [Char(30)]
    public string CMCITY { get; private set; }

    [Char(2)]
    public string CMSTATE { get; private set; }

    [Char(10)]
    public string CMPOSTCODE { get; private set; }

    [Dec(9, 0)]
    public decimal SETORDNUM { get; set; }

    public class SFL1_Model : SubfileRecordModel
    {
        [Values(typeof(Decimal),"00","02","03","06")]
        [Dec(2, 0, Protect = "60")]
        public decimal SFSEL { get; set; }

        [Char(1, Protect = "*True")]
        public string SFCOLOR { get; set; }

        [Dec(9, 0)]
        public decimal SFORDNUM { get; private set; }

        [Date]
        public DateTime SFORDDATE { get; private set; } // ORDER DATE

        [Date]
        public DateTime SFSHPDATE { get; private set; } // PRICE

        [Dec(8, 0)]
        public decimal SFDELDATE { get; private set; }

        [Dec(13, 4)]
        public decimal SFORDAMT { get; private set; }

        [Char(4)]
        public string SFFILESTAT { get; private set; }

        [Dec(3, 0)]
        public decimal SFSHPVIA { get; private set; }
    }
}
```

## Properties

| Type | Name | Description
| --- | --- | --- 
| [RecordModel](/reference/expo/qsys-expo-model/record-model.html) | RecordModel | Gets the RecordModel associated with DdsSubfileRecord tag helper |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | RecordNumber | Gets or sets a value indicating the subfile record number (starts at 1) |
