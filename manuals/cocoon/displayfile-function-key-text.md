---
title: "Displayfile Function Key Text Migration"
description: "Master display file function key text migration. Our guide simplifies the process, ensuring smooth transitions and system compatibility."
---

## Overview

[DDS for Displayfiles](https://www.ibm.com/docs/en/i/7.4?topic=dds-display-files) provides the following keywords to specify the Command Keys available to a Displayfile.

- [CAnn Command Attention](https://www.ibm.com/docs/en/i/7.4?topic=80-cann-command-attention-keyword-display-files)


```
Syntax: CAnn[(response-indicator ['text'])]
```

- [CFnn Command Function](https://www.ibm.com/docs/en/i/7.4?topic=80-cann-command-attention-keyword-display-files)


```
Syntax: CFnn[(response-indicator ['text'])]
```

CAnn and CFnn can be specified at the **File** level or at the **Record** Level.

>The difference between `CAnn` and `CFnn` is that the later transmits *changed data* as part of the response to the server request, while the former does not.

<br>

## Migration of Displayfile Available Command Keys.

Each Displayfile gets migrated as a pair of files:
1. The **View**: Razor Page (or Markup).
2. The **ViewModel**: C# class derived from `ASNA.QSys.Expo.Model.DisplayPageModel` class.

>The file extensions used are: `*.cshtml` and `*.cshtml.cs` respectively.

The **View** defines the User Interface *Presentation* while the **ViewModel** controls the communication of the changed data to the Application Logic.

Following these two different *roles*, the DDS keyword specification is broken down into the two files. The text is migrated as [KeyNames]() properties in the **View** file and the response-indicator (if any) associated to the Command Key is specified as attributes to the DisplayPage Model's `File` or `Record` depending on where it is defined in DDS.

## A simple DDS Migration example.

Assuming the example member-name is called `View`,

```
     A                                      CF03(03 'Exit')                   
 .
 .
 .
     A          R SFLC                      SFLCTL(SFL1)                        
     A                                      CF09(09 'Spooled Files')            

```

### Simple Migration:

`View.cshtml`:

```html
<form id="MonarchForm" method="post">
    <DdsFile DisplayPageModel="Model" KeyNames="F3 'Exit';" >

        <DdsFunctionKeys />

 .
 .
 .

        <DdsSubfileControl For="SFLC" KeyNames="F9 'Spooled Files';" ... >

```

`View.cshtml.cs`

```cs

    [
        BindProperties,
        DisplayPage(FunctionKeys = "F3 03"),
        ExportSource(CCSID = 37)
    ]
    public class View : DisplayPageModel
    {
         public SFLC_Model SFLC { get; set; }

        [
            SubfileControl(ClearRecords : ... ,
                FunctionKeys = "F9 09;",
                .
                .
                .
            )
        ]
        public class SFLC_Model : SubfileControlModel
        {

```

<br>

>The `ENTER` key is assumed to be *always* available and its KeyName is assumed to be 'Enter'. (For language localization, `ENTER` KeyName may be given its text translation, i.e. `'Intro'` in Spanish).

## Conditional indicators for CAnn and CFnn keywords.

Let's assume we have a DDS record which defines the following available function keys:

```
     A          R MYRECORD                                                       
     A                                      CF04(04 'Prompt')                   
     A N30                                  CF06(06 'New')                      
     A N30                                  CF11(11 'Delete')                   
     A                                      CF12(12 'Cancel')                   
```

### Migration with Conditional CAnn and CFnn keywords.

View Markup:

```html
    <DdsRecord For="MYRECORD" KeyNames="F4 'Prompt'; F6 'New'; F11 'Delete'; F12 'Cancel';">
```
>Note: `KeyNames` text for conditional Keys, is not affected in the Markup definition. 

ViewModel C# code:

```cs
        [
            Record(FunctionKeys = "F4 04;F6 06:!30;F11 11:!30;F12 12",
                .
                .
                .
            )
        ]
        public class MYRECORD_Model : RecordModel
        {

```
Notice that in the `FuntionKeys` (or `AttentionKeys`) record attribute, the value contains the following specifications:

1. F4 04
2. F6 06:!30
3. F11 11:!30
4. F12 12


> `FunctionKeys` and `AttentionKeys` collections are specified as a semi-colon separated string list.

Each specification uses the following syntax:

```
KEY response-indicator [: conditions]
```
>*conditions* is optional and specifies an expression that may contain AND, OR and NOT operands. 
To make expression syntax more *compact*, the following symbols are used instead of operands:

**AND** : `&`

**OR**  &nbsp; &nbsp;: `:`

**NOT** : `!`

When the *condition* evaluates to *false* the *clickable-button* with the corresponding `KeyName` will not be present on the Function key panel (ignoring the Markup specification).

As any other *response-indicator*, the indicator-number will be set or reset when used, i.e. `_IN[nn]` will be set to `1` (or `*INnn` to `*On` in RPG syntax).

The specification `F6 06:!30` can be read as follows:

*"Command key F6 is available to the Record (and the text visible) if indicator 30 is OFF. If the user presses F6 to submit page, the indicator 06 will be turned `ON` (ready for application Logic to check its value in conditional Logic code).*

>`Function` and `Attention` keys use the same format. The name of the Record class attribute `FunctionKeys` or `AttentionKeys` differentiates its purpose.



## Display Page Layout and Function key Panel corresponding location. 

Display pages as HTML use a two-panel [Flex Layout](https://developer.mozilla.org/en-US/docs/Web/CSS/flex), where one of the panels is used to contain the function-key-clickable elements and the other to contain the `DdsFile` and its active record format display elements.

By default, the [Flex Layout](https://developer.mozilla.org/en-US/docs/Web/CSS/flex) uses CSS to position the panels as two vertical columns where the Function keys are shown on the left and the **Main** Display file elements (file and active records) to the right.

There is a placeholder [tagHelper](https://www.learnrazorpages.com/razor-pages/tag-helpers/) element called `DdsFunctionKeys` which is frequently generated during Migration, right after `DdsFile` tagHelper, like so:

```html
<form id="MonarchForm" method="post">
    <DdsFile DisplayPageModel="Model" ... >

        <DdsFunctionKeys />

 .
 .
 .

        @* The rest of the Records go here  *@

    </DdsFile>
```

`DdsFunctionKeys` is not rendered in the place where it is defined, rather, the properties of this placeholder tagHelper are used to construct the two-panel [Flex Layout](https://developer.mozilla.org/en-US/docs/Web/CSS/flex). This `DdsFunctionKeys` tagHelper has only one property, namely `Location`.

The `Location` property may have one of these values:

1. `VerticalLeft`  - Keys are rendered in a vertical direction on the left of the page.
2. `VerticalRight` - Keys are rendered in a vertical direction on the right of the page.
3. `HorizontalTop` - Keys are rendered in a horizontal direction on the top of the page.
4. `HorizontalBottom` - Keys are rendered in a horizontal direction on the bottom of the page.
5. `Hidden` - Keys are not rendered.

>If not provided, the default location of the FunctionKey panel is `VerticalLeft`.

![Location values](images/function-key-location.svg)

<br>

Being a two-panel [Flex Layout](https://developer.mozilla.org/en-US/docs/Web/CSS/flex), the position of the **Main** Display panel follows the layout. That is, if `VerticalLeft` is used (default), the **Main** Display panel is rendered as the right panel, if `HorizontalBottom` is used, the **Main** Display panel is rendered as the top panel, etc. 

<br>

### One more DDS Keyword that may define the Indicator Text

There is one more DDS Keyword relevant to this discussion, [INDTXT Indicator Text](https://www.ibm.com/docs/en/i/7.4?topic=80-indtxt-indicator-text-keyword-display-files) which is also used to determine the text used during migration.

```
Syntax: INDTXT(indicator 'indicator-text')
```

The [INDTXT](https://www.ibm.com/docs/en/i/7.4?topic=80-indtxt-indicator-text-keyword-display-files) keyword is only used to document the *usage* of an indicator - it has no effect on the behavior of the display file -.

However, some Display Files use a combination of Command Key keywords (CAnn or CFnn) and `INDTXT` placed *in the same source line*.  

For example, 

```
      A                                     CF03 INDTXT(03 'Exit') 
```

The indicator `_IN03` (or `*IN03` using RPG syntax) will **not** be set, since it is not used as an *option-indicator* by the `CFnn` keyword, but the Application Logic code may still check for the associated [Function Key Indicator](https://www.ibm.com/docs/en/i/7.4?topic=indicators-function-key) or `INK` indicator (as opposed to the numbered option indicator) to condition Logic code execution.

This unique usage serves as source-member documentation, indicating in this case that *"The function key F3 is available, and - when hit - it will turn indicator KC on. In addition, it documents to be associated to the process of Exiting the Application."*
 
The Migration of this style of DDS Command Key specification will yield,

```html
    <DdsRecord For="MYRECORD" KeyNames="F3 'Exit';">
```

```cs
        [
            Record(FunctionKeys = "F3 *None",
                .
                .
                .
            )
        ]
        public class MYRECORD_Model : RecordModel
        {
```
 
> The DDS line may be conditioned by indicators as usual, producing the File or Record attribute with something like `FunctionKeys = "F3 *None : 88"` assuming the conditional indicator is `88`.
