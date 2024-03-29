---
title: DdsButtonTagHelper Class
---

Defines a clickable element that can be used to simulate pressing a function key.

**Namespace:** ASNA.QSys.Expo.Tags <br/>
**Assembly:** ASNA.QSys.Expo.Tags

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [TagHelper](https://docs.microsoft.com/en-us/dotnet/api/microsoft.aspnetcore.razor.taghelpers.taghelper) --> DdsButtonTagHelper

## Remarks

Interactive IBM i Legacy Applications present data to the user on the screen then allow the user to enter additional data and press Enter, or a Function Key, to continue the execution of the application. As part of the information sent from the screen to the application, the location of the cursor (row,column) and the Function Key pressed is included.

Expo applications function the same way, allowing users to use their keyboards to enter data and press function keys on their keyboards. The DdsButton provides an alternate way for the user to select the function key desired.  The DdsButton also allows the programmer to simulate the location of the cursor when the DdsButton is pressed along with the name of then input field and even provide some data on the field when the DdsButton is clicked.

An attention identifier (AID) is the way of specifying the function key used by a user. To set the name of the function key being impersonated by the DdsButton use the property `AidKey`. 

A programmer enables which function keys are available to the user by listing the keys in the Model at the File level, using the [DisplayPage](/reference/asna-qsys-expo/expo-model/display-page-attribute.html) attribute, or at the record level utilizing the [Record]((/reference/asna-qsys-expo/expo-model/record-attribute.html)) attribute, in both cases the attribute's `FunctionKeys` property is used.  If the key is to be enable only sometimes then an indicator expression can be provided.

In order for the DdsButton to be rendered and available on the screen, the corresponding function key which it impersonates should be enabled by the application.  For instance, if the programmer adds a DdsButton with its `AidKey` set to `F4`, then the function key `F4` should be enabled by the application at either the File or the Record level.

### Simulating Cursor Position

Some legacy applications used a technique where the user was able to position the `cursor` on an input-capable field and press one of the available `Function Keys` to submit the Page. Application logic would identify the pressed `Function Key` combined with the location of the cursor (next to a named field), and determine the action to take.

Modernized Applications may want to provide additional [HTML Button](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/button) elements in strategic places on the Page, to improve usability.

#### Reporting a Field Name
To maintain the Legacy Application logic intact, `DdsButton` Tag Helper can simulate the action of navigating to the desired input element and *pressing* a specified [AidKey](/reference/asna-qsys-expo/expo-model/aid-key.html).

For example, assuming that a Display Page has a *Prompt* feature, indicated with `F4` valid for fields `SFSTATE` and `SFSTATUS` (record `CUSTREC`), the following two `DdsButtons` may be added to improve usability:

```html
<DdsRecord For="CUSTREC" KeyNames="ENTER 'Submit'; F3 'Exit'; F4 'Prompt'; F6 'New Customer'; F11 'Remove Customer'; F12 'Back';">
    <div Row="2">
        . . .
        <DdsButton Col="91" ButtonStyle="Icon" IconId="search" AidKey="F4" FocusField="CUSTREC.SFSTATUS" IconTitle="Prompt for Status Codes" />
    </div>

    <div Row="7">
        . . .
        <DdsButton Col="40" ButtonStyle="Icon" IconId="search" AidKey="F4" FocusField="CUSTREC.SFSTATE" IconTitle="Prompt for State Codes" />
    </div>

<DdsRecord/>
```

The first `DdsButton` will appear on `Row 2`, `Col 91` and when user clicks (or Taps with finger) on this button, it simulates that the `cursor` was located on field "CUSTREC.SFSTATUS" and the press of the `F4`[AidKey](/reference/asna-qsys-expo/expo-model/aid-key.html)

The second `DdsButton` will appear on `Row 7`, `Col 40` and when user clicks (or Taps with finger) on this button, it simulates that the `cursor` was located on field "CUSTREC.SFSTATE" and the press of the `F4`[AidKey](/reference/asna-qsys-expo/expo-model/aid-key.html)

Both `DdsButton` appear as icons with the shape of a magnifying glass (typically used by *search*).

>Note: The Application Logic remains intact. 

#### Reporting a Row and Column Position
If the application is looking for the Row and Column where the cursor was positioned at the time the function key was pressed, then the programmer can use the `VirtualRowCol` property of DdsButton to simulate that position. 

```html
    <DdsButton Col="40" ButtonStyle="Icon" IconId="search" AidKey="F4" VirtualRowCol="7,27" IconTitle="Prompt for State Codes" />
```

### Setting a Value

In addition to having the DdsButton simulate the position of the cursor in a particular field, it is also possible to specify some value to be entered for the selected field. 

The following example shows an input capable field named VZCFCD used by the application to receive some confirmation.  The two DdsButtons allow the user to simply click them to express her intention. Clicking  the `Confirm` button will enter a 'Y' on the field `VZCFCD` of record format `RCONFIRM` and press \<Enter\>. Clicking on the `Cancel` button will simulate pressing the \<F12\> key.

```html
<DdsRecord For="RCONFIRM" KeyNames="ENTER 'Intro.'; F12 'Cancel';" WindowLeftCol="50" WindowTopRow="22" WindowHeightRows="1" WindowWidthCols="38">
    . . .
    <DdsCharField Col="12" For="RCONFIRM.VZCFCD"  VirtualRowCol="24,73" Color="Blue" />
    <DdsButton Col="24" AidKey="Enter" ButtonStyle="Button" Text="Confirm" FocusField="RCONFIRM.VZCFCD" FieldValue="Y" />
    <DdsButton Col="32" AidKey="F12"   ButtonStyle="Button" Text="Cancel" />
    . . . 
<DdsRecord/>
```
![](images/dds-button-button.jpg)

### Focusing on a Subfile's Field
To set a DdsButton's `FocusField` property to a subfile field use this syntax:

```html
<DdsSubfileRecord RecordNumber="rrn" For="SFLC.SFL1">
    . . .
    <DdsButton Col="7"  FocusField=@($"SFLC.SFL1[{rrn}].SFSEL") FieldValue="2" AidKey="Enter" Title="Update Customer" ButtonStyle="Link"   Text="Update" />
    <DdsButton Col="14" FocusField=@($"SFLC.SFL1[{rrn}].SFSEL") FieldValue="3" AidKey="Enter" Title="Display Sales"   ButtonStyle="Button" Text="Sales" />
</DdsSubfileRecord>
```


### Button Styles
The DdsButton can be rendered in one of four [styles](/reference/asna-qsys-expo/expo-tags/dds-button-tag-helper/button-styles.html):
 + Button
 + Icon
 + Image
 + Link

#### Button
To display the DdsButton as a link, set the `ButtonStyle="Button"` and the `Text` property to name the button.

```html
    <DdsButton Col="24" AidKey="Enter" ButtonStyle="Button" Text="Confirm" FocusField="RCONFIRM.VZCFCD" FieldValue="Y" />
    <DdsButton Col="32" AidKey="F12"   ButtonStyle="Button" Text="Cancel" />
```
![](images/dds-button-button.jpg)

#### Icon

When displaying a DdsButton as an Icon, use one of the shapes provided by the library. The [*Icon Shapes*](/reference/asna-qsys-expo/expo-tags/dds-button-icon-reference.html) are simple and clean, monochrome (color can be changed to any solid color), scaled without loss and respect the background (use *transparent* background).

To display the DdsButton as a link, set the `ButtonStyle="Button"` and set the name of the Icon to be used on the `IconID` property.

```html
    <DdsButton Col="24" AidKey="Enter" ButtonStyle="Icon" IconId="check"         Color="green" FocusField="RCONFIRM.VZCFCD" FieldValue="Y" />
    <DdsButton Col="32" AidKey="F12"   ButtonStyle="Icon" IconId="remove-circle" Color="red />
```
![](images/dds-button-icon.jpg)

#### Image

To display the DdsButton as an image, set the `ButtonStyle="Image"` and set the `Image` property to the URL of the desired image.

```html
    <DdsButton Col="24" AidKey="Enter" ButtonStyle="Image" Image="/images/confirm.jpg" FocusField="RCONFIRM.VZCFCD" FieldValue="Y" />
    <DdsButton Col="36" AidKey="F12"   ButtonStyle="Image" Image="/images/cancel.jpg" />
```
![](images/dds-button-image.jpg)


#### Link
To display the DdsButton as a link, set the `ButtonStyle="Link"` and the `Text` property to name the link.

```html
    <DdsButton Col="24" AidKey="Enter" ButtonStyle="Link" Text="Confirm" FocusField="RCONFIRM.VZCFCD" FieldValue="Y" />
    <DdsButton Col="32" AidKey="F12"   ButtonStyle="Link" Text="Cancel" />
```
![](images/dds-button-link.jpg)

<br>
<br>

## Properties

| Type | Name | Description | Indexer
| --- | --- | --- | --- 
| [AidKey](/reference/asna-qsys-expo/expo-model/aid-key.html) | AidKey | Attention or Function key to be posted when Button is clicked (as if the user had pressed than keyboard key). | 
| [ButtonStyles](/reference/asna-qsys-expo/expo-tags/dds-button-tag-helper/button-styles.html) | ButtonStyle | Gets or sets a ButtonStyle to define the rendering shape. | 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | Col | Gets or sets a value that indicates the horizontal position within a Row. | 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | Color | Gets or sets the name of a web color to be used to draw the element. | 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | FieldValue | When used along with FocusField, gets or sets the value to be copied to the field prior to submitting the page. This allows compatibility with logic expecting to detect a particular value of a field at a particular cursor position. | 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | FocusField | Gets or sets the name of the field where the cursor will be set prior to submitting the page. This allows compatibility with logic expecting to detect cursor position on a particular field. Use the special value \*PREVIOUS instead of a field name to indicate: "The name of the previous input-capable sibling field."  | 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | IconId | When used along with Icon ButtonStyle, gets or sets a value indicating the ID of the icon available in the [Icon Library](dds-button-icon-reference). | 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | Image | When used along with Image ButtonStyle, gets or sets a value indicating the URL to the path to the image. | 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | Order | When a set of ITagHelpers are executed, their Init(TagHelperContext)'s are first invoked in the specified Order; then their ProcessAsync(TagHelperContext, TagHelperOutput)'s are invoked in the specified Order. Lower values are executed first<br>(Inherited from [TagHelper](https://docs.microsoft.com/en-us/dotnet/api/microsoft.aspnetcore.razor.taghelpers.taghelper)) | 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | ProtectCondition | Gets or sets a conditional expression. When rendering, if the condition evaluates to true, the button will not be clickable. | 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | Text | When used along with Button or Link ButtonStyle, gets or sets a value that will be shown in the face of the button. The HTML element defines where the text will show (or ignore it). | 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | Title | Gets or sets the title element that is added to the button. Most Browsers display the title text as a tooltip (accessible name). | 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | VirtualRowCol | Gets or sets the value of the legacy row, col position that the Button will report as being the one where the cursor was 'positioned at' when the button was clicked. | 

<br>
<br>

## Methods

| Type | Name | Description | Return Description 
| --- | --- | --- | --- 
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | [Equals](https://docs.microsoft.com/en-us/dotnet/api/system.object.equals)([Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | Determines whether the specified object is equal to the current object.<br>(Inherited from [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | true if the specified object is equal to the current object; otherwise, false.
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [Finalize](https://docs.microsoft.com/en-us/dotnet/api/system.object.finalize)() | Allows an object to try to free resources and perform other cleanup operations before it is reclaimed by garbage collection.<br>(Inherited from [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | [GetHashCode](https://docs.microsoft.com/en-us/dotnet/api/system.object.gethashcode)() | Serves as the default hash function.<br>(Inherited from [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | A hash code for the current object.
| [Type](https://docs.microsoft.com/en-us/dotnet/api/system.type) | [GetType](https://docs.microsoft.com/en-us/dotnet/api/system.object.gettype)() | Gets the Type of the current instance.<br>(Inherited from [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | The exact runtime type of the current instance.
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [Init](https://docs.microsoft.com/en-us/dotnet/api/microsoft.aspnetcore.razor.taghelpers.taghelper.init)([TagHelperContext]($$TODO-TagHelperContext.html)) | Initializes the ITagHelper with the given context.Additions to Items should be done within this method to ensure they're added prior to executing the children.<br>(Inherited from [TagHelper](https://docs.microsoft.com/en-us/dotnet/api/microsoft.aspnetcore.razor.taghelpers.taghelper)) | 
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | [IsVisible](#isvisible)() | Gets a value that indicates if button should be rendered. | True when conditional indicator expression evaluates to true, false otherwise.
| [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) | [MemberwiseClone](https://docs.microsoft.com/en-us/dotnet/api/system.object.memberwiseclone)() | Creates a shallow copy of the current Object.<br>(Inherited from [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | A shallow copy of the current Object.
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [Process](https://docs.microsoft.com/en-us/dotnet/api/microsoft.aspnetcore.razor.taghelpers.taghelper.process)([TagHelperContext]($$TODO-TagHelperContext.html), [TagHelperOutput]($$TODO-TagHelperOutput.html)) | Synchronously executes the TagHelper with the given context and output.<br>(Inherited from [TagHelper](https://docs.microsoft.com/en-us/dotnet/api/microsoft.aspnetcore.razor.taghelpers.taghelper)) | A stateful HTML element used to generate an HTML tag.
| [Task]($$TODO-System.Threading.Task.html) | [ProcessAsync](https://docs.microsoft.com/en-us/dotnet/api/microsoft.aspnetcore.razor.taghelpers.taghelper.processasync)([TagHelperContext]($$TODO-TagHelperContext.html), [TagHelperOutput]($$TODO-TagHelperOutput.html)) | Asynchronously executes the TagHelper with the given context and output.<br>(Inherited from [TagHelper](https://docs.microsoft.com/en-us/dotnet/api/microsoft.aspnetcore.razor.taghelpers.taghelper)) | A Task that on completion updates the output.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | [ReferenceEquals](https://docs.microsoft.com/en-us/dotnet/api/system.object.referenceequals)([Object](https://docs.microsoft.com/en-us/dotnet/api/system.object), [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | Determines whether the specified Object instances are the same instance.<br>(Inherited from [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | true if objA is the same instance as objB or if both are null; otherwise, false.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | [ToString](https://docs.microsoft.com/en-us/dotnet/api/system.object.tostring)() | Returns a string that represents the current object.<br>(Inherited from [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | A string that represents the current object.

<br>
<br>

### IsVisible()

Gets a value that indicates if button should be rendered.

```cs
IsVisible();
```

#### Returns

[Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)

True when conditional indicator expression evaluates to true, false otherwise.


<br>
<br>

