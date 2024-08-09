---
title: "DdsSubfileControlTagHelper class"
description: "Defines a Subfile Controller element "
last_modified_at: 2024-08-09T17:26:17Z
---

Defines a Subfile Controller element

**Namespace:** ASNA.QSys.Expo.Tags
**Assembly:** ASNA.QSys.Expo.Tags.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [TagHelper](https://learn.microsoft.com/en-us/dotnet/api/microsoft.aspnetcore.razor.taghelpers.taghelper?view=aspnetcore-8.0) --> [RecordBaseTagHelper](/reference/expo/qsys-expo-tags/record-base-tag-helper.html) --> [DdsRecordTagHelper](/reference/expo/qsys-expo-tags/dds-record-tag-helper.html)
<br>
<br>


## Remarks

A `DdsSubfileControl` Tag Helper is a specialized [DdsRecord](/reference/expo/qsys-expo-tags/dds-record-tag-helper.html) that may contain a [Subfile Record](/reference/expo/qsys-expo-model/subfile-record-model.html). A `Subfile Record` is defined as a collection of [DdsSubfileRecord](/reference/expo/qsys-expo-tags/dds-subfile-record-tag-helper.html) Tag Helpers, nested `DdsSubfileControl` using a specified range of `DIV` rows, in as shown in the example code bellow).

The following markup shows the specification of DdsSubfileControl named "SFLC". As any other [DdsRecord](/reference/expo/qsys-expo-tags/dds-record-tag-helper.html) Tag Helper, `DdsSubfileControl` Tag Helper may contain [DdsConstants](/reference/expo/qsys-expo-tags/dds-constant-tag-helper.html) and [DdsFields](/reference/expo/qsys-expo-tags/dds-field-base.html) and up to one Subfile (collection of [DdsSubfileRecords](/reference/expo/qsys-expo-tags/dds-subfile-record-tag-helper.html)).

```html
@{
    int SFLC_SubfilePage = 10;
}
<DdsSubfileControl For="SFLC" KeyNames="ENTER 'Enter'; F6 'Add'; PageUp; PageDown;" SubfilePage="@SFLC_SubfilePage" CueCurrentRecord=true ClickSetsCurrentRecord=true>
    <div Row="1">
        <DdsConstant Col="2" Text=@System.Environment.UserName />
        <DdsConstant Col="33+1" Text="M5 Order Inquiry" Color="DarkBlue" />
        <DdsConstant Col="64+1" Text=@DateTime.Today.ToString(@"MM\/ dd\/ yy") />
        <DdsConstant Col="73+1" Text=@DateTime.Now.ToString("HH: mm: ss") />
    </div>
    <div Row="3">
        <DdsConstant Col="2" Text="Customer:" />
        <DdsCharField Col="12+1" For="SFLC.SCRCUST" Upper=true Comment="CUSTOMER NBR AND NAME" />
    </div>
    <div Row="4">
        <DdsConstant Col="2" Text="Phone...:" />
        <DdsCharField Col="12+1" For="SFLC.SCRPHONE" Upper=true />
        <DdsConstant Col="36+1" Text="Address:" />
        <DdsCharField Col="45+1" For="SFLC.CMADDR1" Upper=true />
    </div>
    <div Row="5">
        <DdsConstant Col="2" Text="Fax.....:" />
        <DdsCharField Col="12+1" For="SFLC.SCRFAX" Upper=true Comment="FAX NUMBER" />
        <DdsCharField Col="45+1" For="SFLC.CMADDR2" Upper=true />
    </div>
    <div Row="6">
        <DdsConstant Col="2" Text="Status..:" />
        <DdsCharField Col="12+1" For="SFLC.CMACTIVE" Upper=true />
        <DdsCharField Col="45+1" For="SFLC.CMCITY" Upper=true />
    </div>
    <div Row="7">
        <DdsCharField Col="45+1" For="SFLC.CMSTATE" Upper=true />
        <DdsCharField Col="48+1" For="SFLC.CMPOSTCODE" Upper=true />
    </div>
    <div Row="8">
        <DdsConstant Col="2" Text="Options:" Color="Blue" />
    </div>
    <div Row="9">
        <DdsConstant Col="3+1" Text="2=Update hdr  3=Update line items  6=Print" Color="Blue" />
        <DdsConstant Col="50+1" Text="Position to order:" />
        <DdsDecField Col="69+1" For="SFLC.SETORDNUM" VirtualRowCol="9,69" EditCode="Z" tabIndex=5 />
    </div>
    <div Row="11">
        <DdsConstant Col="2" Text="Sel" Color="DarkBlue"  />
        <DdsConstant Col="7+1" Text="Order Nbr" Color="DarkBlue"  />
        <DdsConstant Col="19+1" Text="Order Date" Color="DarkBlue"  />
        <DdsConstant Col="30+1" Text="Ship Date" Color="DarkBlue"  />
        <DdsConstant Col="41+1" Text="Delv. Date" Color="DarkBlue"  />
        <DdsConstant Col="52+1" Text="Order Total" Color="DarkBlue"  />
        <DdsConstant Col="71+1" Text="Stat" Color="DarkBlue"  />
        <DdsConstant Col="76+1" Text="Via" Color="DarkBlue"  />
    </div>
    <div Row="12" RowSpan="@SFLC_SubfilePage">
        @for (int rrn=0; rrn < Model.SFLC.SFL1.Count; rrn++)
        {
            int row = 12 + rrn;
            <DdsSubfileRecord RecordNumber="rrn" For="SFLC.SFL1">
                .
                .
                .
            </DdsSubfileRecord>
        }
    </div>
</DdsSubfileControl>
```

## Properties

| Type | Name | Description
| --- | --- | --- 
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | ClickSetsCurrentRecord | Gets or sets a value that indicates if the current record should be set by a mouse click (or finger tap) |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | CueCurrentRecord | Gets or sets a value that indicates if the current record in the Subfile should be highlighted as the pointer hovers over the subfile. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | DblClickKey | Gets or sets a value that indicates the name of the Aid Key to be "pressed" prior to submitting the page, if user double-clicks at the record. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | DblClickTargetField | Gets or sets a value that indicates the name of a record field where the cursor will be positioned prior to submitting the page, if user double-clicks at the record. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | DblClickTargetValue | Gets or sets a value that indicates the value to be set to of a record field prior to submitting the page, if user double-clicks at the record. |
| [ConditionalProperty](/reference/expo/qsys-expo-model/conditional-property.html) | ErrorMessage | Gets or sets a value of a ConditionalProperty associated with an error message. |
| [ConditionalProperty](/reference/expo/qsys-expo-model/conditional-property.html) | ErrorMessageId | Gets or sets a value of a ConditionalProperty associated with an error message ID. |
| [AidKey](/reference/expo/qsys-expo-model/aid-key.html) | SflDropKey | Gets or sets a value of the Aid Key that will trigger the subfile to drop fields on display records (only the. |
| [AidKey](/reference/expo/qsys-expo-model/aid-key.html) | SflFoldKey | Gets or sets a value of the Aid Key that will trigger the subfile to fold fields on display records. |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | ShowRecordAtTop | Gets or sets a value that indicates that record with indicated "rrn" should be displayed as the first record on the subfile . |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | ShowRecordNumber | Gets or sets a value that indicates the page that should be visible to guarantee that the "rrn" indicated is displayed (when the subfile has more than one page's worth of records). |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | ShowRecordWithCursor | Gets or sets a value that indicates the page that should be visible to guarantee that record with the cursor is displayed (when the subfile has more than one page's worth of records). |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | SubfileDrop | Gets or sets the Conditional Indicator Expression that determines when subfile-drop display mode is active. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | SubfileEnd | Gets or sets a value of the conditional expression that determines if the subfile contains the records of the last page.  |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | SubfileEndTextOff | Gets or sets a value of the label displayed by subfile when there are more ore records (not in last page) |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | SubfileEndTextOn | Gets or sets a value of the label displayed by subfile when there are no records (last page) |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | SubfileFold | Gets or sets the Conditional Indicator Expression that determines when subfile-fold display mode is active. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | SubfilePage | Gets or sets the Page value |

## Methods

| Signature | Description |
| --- | --- |
| [IsSubfileFolded](#bool-issubfilefoldedtaghelperexecutioncontext-executioncontext)([TagHelperExecutionContext](https://learn.microsoft.com/en-us/dotnet/api/microsoft.aspnetcore.razor.runtime.taghelpers.taghelperexecutioncontext?view=aspnetcore-8.0)) | Determines if records in the subfile are folded, as opposed to truncated.

### bool IsSubfileFolded([TagHelperExecutionContext executionContext](https://learn.microsoft.com/en-us/dotnet/api/microsoft.aspnetcore.razor.runtime.taghelpers.taghelperexecutioncontext?view=aspnetcore-8.0))

Determines if records in the subfile are folded, as opposed to truncated.

```cs
bool IsSubfileFolded(TagHelperExecutionContext executionContext)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [TagHelperExecutionContext](https://learn.microsoft.com/en-us/dotnet/api/microsoft.aspnetcore.razor.runtime.taghelpers.taghelperexecutioncontext?view=aspnetcore-8.0) | executionContext | 

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | true if the records in the subfile are folded.
