---
title: "DdsFileTagHelper class        | QSYS API Reference Guide"
description: "Renders the Monarch Base Application&#39;s Active records along with Active Aid Keys. "
last_modified_at: 2024-08-09T16:19:09Z
---

Renders the Monarch Base Application's Active records along with Active Aid Keys.

**Namespace:** ASNA.QSys.Expo.Tags
**Assembly:** ASNA.QSys.Expo.Tags.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [TagHelper](https://learn.microsoft.com/en-us/dotnet/api/microsoft.aspnetcore.razor.taghelpers.taghelper?view=aspnetcore-8.0)
<br>
<br>


## Remarks

There is one *- and only one -* `DdsFile` Tag Helper on a Display Page.

The `DdsFile` is the placeholder for the Display Page. It is the parent element for the rest of the `DdsXXX` Tag Helpers.

The following is the basic [Razor Page](https://docs.microsoft.com/en-us/aspnet/core/razor-pages/) element markup structure that defines a Display Page:

```html
<form method="post">>
    <DdsFile DisplayPageModel="Model">

        <DdsFunctionKeys />

        <main role="main" >
            <DdsSubfileControl For="Record_1">...</DdsSubfileControl>
            <DdsRecord For="Record_2">...</DdsRecord>
            <DdsRecord For="Record_3">...</DdsRecord>
            <DdsRecord For="Record_n">...</DdsRecord>
            <DdsMessagePanel />
        </main>
    </DdsFile>
</form>
```

>The Application controls which of the DdsRecords (including any DdsSubfileControl) are *active* at a time. The same can be said for the *active* Function keys.

Only the *active* DdsRecords are rendered when the Display Page is presented to the user inside the Browser's form.

Notice the Razor page meta-data at the top of the `.cshtml` file:

```html
@page
@model MYPAGENAME
```

Which indicates that file `MYPAGENAME.cshtml.cs` defines the instance of the class `MYPAGENAME` which derives from [DisplayPageModel](/reference/expo/qsys-expo-model/display-page-model.html)

By convention the model file has the name `MYPAGENAME.cshtml.cs` with content similar to this: 

```cs
namespace MyCompany.MyApplication.ApplicationViews
{
    [
        BindProperties,
        DisplayPage(FunctionKeys = "F3 03"),
        ExportSource(CCSID = 37)
    ]
    public class MYPAGENAME : DisplayPageModel
    {
```

Where all the `DdsRecords` are defined.

## Properties

| Type | Name | Description
| --- | --- | --- 
| [DisplayPageModel](/reference/expo/qsys-expo-model/display-page-model.html) | DisplayPageModel | Gets the Active Page Model. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | KeyNames | Gets or sets the display key name collection for the File. Key names are separated by semicolon. |
| [Decimal](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types) | LengthMonoFontAdjustmentFactor | Gets or sets factor value applied to the calculation of grid-field ending positions. Typically a reduction factor required to adjust widths due to the use of  Proportional fonts, replacing legacy Monospaced fonts. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | MinRows | Gets or sets the minimum Rows that will be rendered to define the minimum Page height. Corresponds to the legacy DDS DSPSIZ  |

## Methods

| Signature | Description |
| --- | --- |
| [Init](#void-inittaghelpercontext-context)([TagHelperContext](https://learn.microsoft.com/en-us/dotnet/api/microsoft.aspnetcore.razor.taghelpers.taghelpercontext?view=aspnetcore-8.0)) | Initializes the ITagHelper with the given context. 
| [ProcessAsync](#task-processasynctaghelpercontext-context-taghelperoutput-output)([TagHelperContext](https://learn.microsoft.com/en-us/dotnet/api/microsoft.aspnetcore.razor.taghelpers.taghelpercontext?view=aspnetcore-8.0), [TagHelperOutput](https://learn.microsoft.com/en-us/dotnet/api/microsoft.aspnetcore.razor.taghelpers.taghelperoutput?view=aspnetcore-8.0)) | Asynchronously executes the TagHelper with the given context and output.

### void Init([TagHelperContext context](https://learn.microsoft.com/en-us/dotnet/api/microsoft.aspnetcore.razor.taghelpers.taghelpercontext?view=aspnetcore-8.0))

Initializes the ITagHelper with the given context. 

```cs
void Init(TagHelperContext context)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [TagHelperContext](https://learn.microsoft.com/en-us/dotnet/api/microsoft.aspnetcore.razor.taghelpers.taghelpercontext?view=aspnetcore-8.0) | context | Contains information associated with the current HTML tag.

### Task ProcessAsync([TagHelperContext context](https://learn.microsoft.com/en-us/dotnet/api/microsoft.aspnetcore.razor.taghelpers.taghelpercontext?view=aspnetcore-8.0), [TagHelperOutput output](https://learn.microsoft.com/en-us/dotnet/api/microsoft.aspnetcore.razor.taghelpers.taghelperoutput?view=aspnetcore-8.0))

Asynchronously executes the TagHelper with the given context and output.

```cs
Task ProcessAsync(TagHelperContext context, TagHelperOutput output)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [TagHelperContext](https://learn.microsoft.com/en-us/dotnet/api/microsoft.aspnetcore.razor.taghelpers.taghelpercontext?view=aspnetcore-8.0) | context | Contains information associated with the current HTML tag.
| [TagHelperOutput](https://learn.microsoft.com/en-us/dotnet/api/microsoft.aspnetcore.razor.taghelpers.taghelperoutput?view=aspnetcore-8.0) | output | A stateful HTML element used to generate an HTML tag.

#### Returns

| Type | Description
| --- | ---
| [Task](https://docs.microsoft.com/en-us/dotnet/api/system.threading.tasks.taskscheduler) | A Task that on completion updates the output.
