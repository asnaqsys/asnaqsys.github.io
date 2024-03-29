---
title: DdsDecDateFieldTagHelper Class
---

Defines an input element to capture Dates for fields defined as decimal values.

**Namespace:** ASNA.QSys.Expo.Tags <br/>
**Assembly:** ASNA.QSys.Expo.Tags

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [TagHelper](https://docs.microsoft.com/en-us/dotnet/api/microsoft.aspnetcore.razor.taghelpers.taghelper) --> [FieldBase](/reference/asna-qsys-expo/expo-tags/field-base.html) --> [DdsFieldBase](/reference/asna-qsys-expo/expo-tags/dds-field-base.html) --> [DdsDateFieldTagHelper](/reference/asna-qsys-expo/expo-tags/dds-date-field-tag-helper.html) --> DdsDecDateFieldTagHelper

<br>
<br>

## Remarks

Legacy Applications more commonly used Dates as numeric values (with a particular [EditWord](/reference/asna-qsys-expo/expo-model/edit-word.html)), more than the proper [Date type](https://www.ibm.com/docs/en/i/7.3?topic=fields-example-date-time-timestamp-dds).

During Migration patterns are observed to identify such dates and convert them to `DdsDecDateField` tag Helper to make the Calendar available on the Page (as if the proper [Date type](https://www.ibm.com/docs/en/i/7.3?topic=fields-example-date-time-timestamp-dds) was used).

This alone provides automated Modernization.

```html
<div Row="12" RowSpan="@SFLC_SubfilePage">
    @for (int rrn=0; rrn < Model.SFLC.SFL1.Count; rrn++)
    {
        int row = 12 + rrn;
        <DdsSubfileRecord RecordNumber="rrn" For="SFLC.SFL1">

            <DdsDecDateField Col="41+1" For="SFLC.SFL1[rrn].SFDELDATE" DateFormat="ISO" DateSeparator="-" SuppressLeadingZeroes=true Color="Green : !61 , DarkBlue : 61" />

        </DdsSubfileRecord>
    }
</div>
```

Note how the [DateFormat](/reference/asna-qsys-expo/expo-model/date-attribute/dds-date-format.html) and `DateSeparator`are defined in the *Presentation* (markup) and not in the model (as it is done for [DdsDateField](/reference/asna-qsys-expo/expo-tags/dds-date-field-tag-helper.html))

```cs
public class SFL1_Model : SubfileRecordModel
{
    .
    .
    .
    [Dec(8, 0)]
    public decimal SFDELDATE { get; private set; }
    .
    .
    .
}
```
The Model defines a [decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) type (which knows nothing about DateFormat or DateSeparators). The Application Logic will process the numeric value as usual.

<br>
<br>

## Properties

| Type | Name | Description | Indexer
| --- | --- | --- | --- 
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | AutoPostBack | Gets or sets boolean value to indicate that input-capable field should post-back the form as soon as user enters a value.<br>(Inherited from [FieldBase](/reference/asna-qsys-expo/expo-tags/field-base.html)) | 
| [AidKey](/reference/asna-qsys-expo/expo-model/aid-key.html) | AutoPostBackKey | Gets or sets the Aid Key that should be posted when AutoPostBack property is true.<br>(Inherited from [FieldBase](/reference/asna-qsys-expo/expo-tags/field-base.html)) | 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | Col | Gets or sets a value that indicates horizontal position for field/constant within the page. Valid values start at 1 typically up to 132.<br>(Inherited from [FieldBase](/reference/asna-qsys-expo/expo-tags/field-base.html)) | 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | Color | Gets or sets a value that indicates the [conditional property](/reference/asna-qsys-expo/expo-model/conditional-properties-overview.html#conditional-property) string that evaluates to a Web named color. Conditions are separated by comma and depend on conditional indicators.<br>(Inherited from [FieldBase](/reference/asna-qsys-expo/expo-tags/field-base.html)) | 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | ColSpan | Gets or sets a value that indicates the amount of positions used by field/constant. Default is zero, meaning: compute element length.<br>(Inherited from [FieldBase](/reference/asna-qsys-expo/expo-tags/field-base.html)) | 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | Comment | Gets or sets the text used to document the Field/Constant. Used as comment, does not render as HTML.<br>(Inherited from [FieldBase](/reference/asna-qsys-expo/expo-tags/field-base.html)) | 
| [DateAttribute](/reference/asna-qsys-expo/expo-model/date-attribute.html) | DateFieldAttribute | Gets the DateAttribute from the Model.<br>(Inherited from [DdsDateFieldTagHelper](/reference/asna-qsys-expo/expo-tags/dds-date-field-tag-helper.html)) | 
| [DdsDateFormat]($$TODO-DdsDateFormat.html) | DateFormat | Gets the DateFormat from the Model. | 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | DateSeparator | Gets the Date Separator from the Model. | 
| [DecAttribute](/reference/asna-qsys-expo/expo-model/dec-attribute.html) | DecFieldAttribute | Gets the DecAttribute from the Model. | 
| [Byte](https://docs.microsoft.com/en-us/dotnet/api/system.byte) | DisplayAttrCode | Gets or sets hex Display attribute code indicating the legacy P-field Display Attribute code.<br>(Inherited from [FieldBase](/reference/asna-qsys-expo/expo-tags/field-base.html)) | 
| [ConditionalProperty](/reference/asna-qsys-expo/expo-model/conditional-property.html) | ErrorMessage | Gets or sets a value that indicates conditional property describing the Error Message.<br>(Inherited from [DdsFieldBase](/reference/asna-qsys-expo/expo-tags/dds-field-base.html)) | 
| [ConditionalProperty](/reference/asna-qsys-expo/expo-model/conditional-property.html) | ErrorMessageId | Gets or sets a value that indicates conditional property describing the Error Message ID.<br>(Inherited from [DdsFieldBase](/reference/asna-qsys-expo/expo-tags/dds-field-base.html)) | 
| [FieldAttribute](/reference/asna-qsys-expo/expo-model/field-attribute.html) | FieldAttribute | When overriden in a derived class, gets a value that indicates the Field Attribute.<br>(Inherited from [DdsFieldBase](/reference/asna-qsys-expo/expo-tags/dds-field-base.html)) | 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | FieldName | Gets the name of the Field.<br>(Inherited from [DdsFieldBase](/reference/asna-qsys-expo/expo-tags/dds-field-base.html)) | 
| [DdsDayNames]($$TODO-DdsDayNames.html) | FirstDayOfWeek | Gets or sets the countries first day of the week.<br>(Inherited from [DdsDateFieldTagHelper](/reference/asna-qsys-expo/expo-tags/dds-date-field-tag-helper.html)) | 
| [ModelExpression](https://docs.microsoft.com/en-us/dotnet/api/microsoft.aspnetcore.mvc.viewfeatures.modelexpression) | For | Gets or sets a value that indicates the Model associated with the Mvc tag helper.<br>(Inherited from [DdsFieldBase](/reference/asna-qsys-expo/expo-tags/dds-field-base.html)) | 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | InvertFontColors | Gets or sets [condition expression](/reference/asna-qsys-expo/expo-model/conditional-properties-overview.html#condition-expression) string that determines if background and forground colors should be switched. Render equivalent to legacy Reverse-Image display attribute.<br>(Inherited from [FieldBase](/reference/asna-qsys-expo/expo-tags/field-base.html)) | 
| [LeftPadOption]($$TODO-LeftPadOption.html) | LeftPad | Gets or sets a LeftPadOption value indicating how to pad values after changing the value of an input-capable field.<br>(Inherited from [FieldBase](/reference/asna-qsys-expo/expo-tags/field-base.html)) | 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | MandatoryEnter | Gets or sets [condition expression](/reference/asna-qsys-expo/expo-model/conditional-properties-overview.html#condition-expression) string that determines if field input is mandatory. Mandatory Enter fields without value change will avoid the form submission.<br>(Inherited from [FieldBase](/reference/asna-qsys-expo/expo-tags/field-base.html)) | 
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | MandatoryFill | Gets or sets a value  that determines if filling up a field is mandatory. Mandatory Fill fields need to use the whole field length. The form will not be submitted until all fields are filled.<br>(Inherited from [FieldBase](/reference/asna-qsys-expo/expo-tags/field-base.html)) | 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | Order | When a set of ITagHelpers are executed, their Init(TagHelperContext)'s are first invoked in the specified Order; then their ProcessAsync(TagHelperContext, TagHelperOutput)'s are invoked in the specified Order. Lower values are executed first<br>(Inherited from [TagHelper](https://docs.microsoft.com/en-us/dotnet/api/microsoft.aspnetcore.razor.taghelpers.taghelper)) | 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | PositionCursor | Gets or sets a [condition expression](/reference/asna-qsys-expo/expo-model/conditional-properties-overview.html#condition-expression) string determining if the cursor should be positioned to this input-capable field.<br>(Inherited from [DdsFieldBase](/reference/asna-qsys-expo/expo-tags/dds-field-base.html)) | 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | TabIndex | Gets or sets a value indicating that its element can be focused, and where it participates in sequential keyboard navigation (usually with the Tab key, hence the name).<br>(Inherited from [FieldBase](/reference/asna-qsys-expo/expo-tags/field-base.html)) | 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | Underline | Gets or sets [condition expression](/reference/asna-qsys-expo/expo-model/conditional-properties-overview.html#condition-expression) string that determines if text should be underlined. Underline is rendered as a bottom-border CSS style.<br>(Inherited from [FieldBase](/reference/asna-qsys-expo/expo-tags/field-base.html)) | 
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | UseNativePicker | Gets or sets a value that indicates if the Browser's date picker should be used when capturing a date.<br>(Inherited from [DdsDateFieldTagHelper](/reference/asna-qsys-expo/expo-tags/dds-date-field-tag-helper.html)) | 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [VirtualRowCol](/reference/asna-qsys-expo/expo-tags/dds-field-base.html#virtualrowcol) | Gets or sets a value that indicates the legacy row, col position that the logic may be expecting to identify. Format is 'Row,Col'. May not represent the current position of the tag helper.<br>(Inherited from [DdsFieldBase](/reference/asna-qsys-expo/expo-tags/dds-field-base.html)) | 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | VisibleCondition | Gets or sets [condition expression](/reference/asna-qsys-expo/expo-model/conditional-properties-overview.html#condition-expression) string that determines if field/constant is visible. Non-visible fields/constants are not rendered.<br>(Inherited from [FieldBase](/reference/asna-qsys-expo/expo-tags/field-base.html)) | 

<br>
<br>

## Methods

| Type | Name | Description | Return Description 
| --- | --- | --- | --- 
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | [Equals](https://docs.microsoft.com/en-us/dotnet/api/system.object.equals)([Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | Determines whether the specified object is equal to the current object.<br>(Inherited from [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | true if the specified object is equal to the current object; otherwise, false.
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [EvalFieldUsageAndValue](/reference/asna-qsys-expo/expo-tags/dds-field-base.html#evalfieldusageandvalue)() | Determine the Usage property value according to the property's get/set access specification as declared in the Model.<br>(Inherited from [DdsFieldBase](/reference/asna-qsys-expo/expo-tags/dds-field-base.html)) | 
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [Finalize](https://docs.microsoft.com/en-us/dotnet/api/system.object.finalize)() | Allows an object to try to free resources and perform other cleanup operations before it is reclaimed by garbage collection.<br>(Inherited from [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | 
| [DdsDateFormat]($$TODO-DdsDateFormat.html) | [GetDateFormat](#getdateformat)() | Get the DdsDateFormat attribute from the Model. | A DdsDateFormat
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [GetDateSeparator](#getdateseparator)() | Gets the Data Separator from de Model. | A string
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [getFieldValue](/reference/asna-qsys-expo/expo-tags/dds-date-field-tag-helper.html#getfieldvalue)() | Gets the Date field's value as a string. Date format and separator are applied when formatting string.<br>(Inherited from [DdsDateFieldTagHelper](/reference/asna-qsys-expo/expo-tags/dds-date-field-tag-helper.html)) | A string value
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | [GetHashCode](https://docs.microsoft.com/en-us/dotnet/api/system.object.gethashcode)() | Serves as the default hash function.<br>(Inherited from [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | A hash code for the current object.
| [Type](https://docs.microsoft.com/en-us/dotnet/api/system.type) | [GetType](https://docs.microsoft.com/en-us/dotnet/api/system.object.gettype)() | Gets the Type of the current instance.<br>(Inherited from [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | The exact runtime type of the current instance.
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [Init](https://docs.microsoft.com/en-us/dotnet/api/microsoft.aspnetcore.razor.taghelpers.taghelper.init)([TagHelperContext]($$TODO-TagHelperContext.html)) | Initializes the ITagHelper with the given context.Additions to Items should be done within this method to ensure they're added prior to executing the children.<br>(Inherited from [TagHelper](https://docs.microsoft.com/en-us/dotnet/api/microsoft.aspnetcore.razor.taghelpers.taghelper)) | 
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | [IsVisible](/reference/asna-qsys-expo/expo-tags/field-base.html#isvisible)() | Gets a value that indicates if element should be rendered.<br>(Inherited from [FieldBase](/reference/asna-qsys-expo/expo-tags/field-base.html)) | True when conditional indicator expression evaluates to true, false otherwise.
| [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) | [MemberwiseClone](https://docs.microsoft.com/en-us/dotnet/api/system.object.memberwiseclone)() | Creates a shallow copy of the current Object.<br>(Inherited from [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | A shallow copy of the current Object.
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [Process](https://docs.microsoft.com/en-us/dotnet/api/microsoft.aspnetcore.razor.taghelpers.taghelper.process)([TagHelperContext]($$TODO-TagHelperContext.html), [TagHelperOutput]($$TODO-TagHelperOutput.html)) | Synchronously executes the TagHelper with the given context and output.<br>(Inherited from [TagHelper](https://docs.microsoft.com/en-us/dotnet/api/microsoft.aspnetcore.razor.taghelpers.taghelper)) | A stateful HTML element used to generate an HTML tag.
| [Task]($$TODO-System.Threading.Task.html) | [ProcessAsync](https://docs.microsoft.com/en-us/dotnet/api/microsoft.aspnetcore.razor.taghelpers.taghelper.processasync)([TagHelperContext]($$TODO-TagHelperContext.html), [TagHelperOutput]($$TODO-TagHelperOutput.html)) | Asynchronously executes the TagHelper with the given context and output.<br>(Inherited from [TagHelper](https://docs.microsoft.com/en-us/dotnet/api/microsoft.aspnetcore.razor.taghelpers.taghelper)) | A Task that on completion updates the output.
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [ProcessDdsField](/reference/asna-qsys-expo/expo-tags/dds-field-base.html#processddsfield)() | When overriden in a derived class, method is called by rendering engine to write the HTML output.<br>(Inherited from [DdsFieldBase](/reference/asna-qsys-expo/expo-tags/dds-field-base.html)) | 
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [ProcessValues](/reference/asna-qsys-expo/expo-tags/dds-field-base.html#processvalues)([TagHelperOutput](https://docs.microsoft.com/en-us/dotnet/api/microsoft.aspnetcore.razor.taghelpers.taghelperoutput?view=aspnetcore-5.0), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Process Display Values.<br>(Inherited from [DdsFieldBase](/reference/asna-qsys-expo/expo-tags/dds-field-base.html)) | 
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | [ReferenceEquals](https://docs.microsoft.com/en-us/dotnet/api/system.object.referenceequals)([Object](https://docs.microsoft.com/en-us/dotnet/api/system.object), [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | Determines whether the specified Object instances are the same instance.<br>(Inherited from [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | true if objA is the same instance as objB or if both are null; otherwise, false.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | [ToString](https://docs.microsoft.com/en-us/dotnet/api/system.object.tostring)() | Returns a string that represents the current object.<br>(Inherited from [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | A string that represents the current object.

<br>
<br>

### GetDateFormat()

Get the DdsDateFormat attribute from the Model.

```cs
GetDateFormat();
```

#### Returns

[DdsDateFormat]($$TODO-DdsDateFormat.html)

A DdsDateFormat


<br>
<br>

### GetDateSeparator()

Gets the Data Separator from de Model.

```cs
GetDateSeparator();
```

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

A string


<br>
<br>

## Fields

| Type | Name | Description
| --- | --- | --- 
| [DdsFileTagHelper](/reference/asna-qsys-expo/expo-tags/dds-file-tag-helper.html) | ddsFile | Gets or sets a value indicating the associated DdsFile tag helper for the field/constant.<br>(Inherited from [FieldBase](/reference/asna-qsys-expo/expo-tags/field-base.html))

<br>
<br>

