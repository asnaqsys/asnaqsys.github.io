---
title: DdsTimeFieldTagHelper Class
---

Defines an input element to capture Times.

**Namespace:** ASNA.QSys.Expo.Tags <br/>
**Assembly:** ASNA.QSys.Expo.Tags

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [TagHelper](https://docs.microsoft.com/en-us/dotnet/api/microsoft.aspnetcore.razor.taghelpers.taghelper) --> [FieldBase](/reference/asna-qsys-expo/expo-tags/field-base.html) --> [DdsFieldBase](/reference/asna-qsys-expo/expo-tags/dds-field-base.html) --> DdsTimeFieldTagHelper

<br>
<br>

## Remarks

To define a field to capture or display time of day values, use the `DdsTimeField` Tag Helper.

For example, the following markup defines a span text element for the field `ARRIVEAT` in the `PACKAGE` record (defined in the Model).

```html
<div Row="7">
    .
    .
    .
    <DdsTimeField Col="27" For="PACKAGE.ARRIVEAT" />
</div>
```

The field `ARRIVEAT` is defined in the Model file, like so:

```cs
public class PACKAGE_Model : RecordModel
{
    .
    .
    [Time(USA)]
    public DateTime ARRIVEAT { get; private set; }


```

Note how the `Time` attribute defines the [format of the Time field](/reference/asna-qsys-expo/expo-model/time-attribute/dds-time-format.html) to be USA. The property accessors define the field `Usage`. In this example, the field is public get and private set, defining it as `OUTPUT Only`.

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
| [Byte](https://docs.microsoft.com/en-us/dotnet/api/system.byte) | DisplayAttrCode | Gets or sets hex Display attribute code indicating the legacy P-field Display Attribute code.<br>(Inherited from [FieldBase](/reference/asna-qsys-expo/expo-tags/field-base.html)) | 
| [ConditionalProperty](/reference/asna-qsys-expo/expo-model/conditional-property.html) | ErrorMessage | Gets or sets a value that indicates conditional property describing the Error Message.<br>(Inherited from [DdsFieldBase](/reference/asna-qsys-expo/expo-tags/dds-field-base.html)) | 
| [ConditionalProperty](/reference/asna-qsys-expo/expo-model/conditional-property.html) | ErrorMessageId | Gets or sets a value that indicates conditional property describing the Error Message ID.<br>(Inherited from [DdsFieldBase](/reference/asna-qsys-expo/expo-tags/dds-field-base.html)) | 
| [FieldAttribute](/reference/asna-qsys-expo/expo-model/field-attribute.html) | FieldAttribute | Gets the Date FieldAttribute from the Model. | 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | FieldName | Gets the name of the Field.<br>(Inherited from [DdsFieldBase](/reference/asna-qsys-expo/expo-tags/dds-field-base.html)) | 
| [ModelExpression](https://docs.microsoft.com/en-us/dotnet/api/microsoft.aspnetcore.mvc.viewfeatures.modelexpression) | For | Gets or sets a value that indicates the Model associated with the Mvc tag helper.<br>(Inherited from [DdsFieldBase](/reference/asna-qsys-expo/expo-tags/dds-field-base.html)) | 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | InvertFontColors | Gets or sets [condition expression](/reference/asna-qsys-expo/expo-model/conditional-properties-overview.html#condition-expression) string that determines if background and forground colors should be switched. Render equivalent to legacy Reverse-Image display attribute.<br>(Inherited from [FieldBase](/reference/asna-qsys-expo/expo-tags/field-base.html)) | 
| [LeftPadOption]($$TODO-LeftPadOption.html) | LeftPad | Gets or sets a LeftPadOption value indicating how to pad values after changing the value of an input-capable field.<br>(Inherited from [FieldBase](/reference/asna-qsys-expo/expo-tags/field-base.html)) | 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | MandatoryEnter | Gets or sets [condition expression](/reference/asna-qsys-expo/expo-model/conditional-properties-overview.html#condition-expression) string that determines if field input is mandatory. Mandatory Enter fields without value change will avoid the form submission.<br>(Inherited from [FieldBase](/reference/asna-qsys-expo/expo-tags/field-base.html)) | 
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | MandatoryFill | Gets or sets a value  that determines if filling up a field is mandatory. Mandatory Fill fields need to use the whole field length. The form will not be submitted until all fields are filled.<br>(Inherited from [FieldBase](/reference/asna-qsys-expo/expo-tags/field-base.html)) | 
| [string ](https://docs.microsoft.com/en-us/dotnet/api/system.string) | MapValues | Gets or sets a value that indicates a list of semicolon-separated output value mappings. Format of each mapping is 'program-value,display-value'. | 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | Order | When a set of ITagHelpers are executed, their Init(TagHelperContext)'s are first invoked in the specified Order; then their ProcessAsync(TagHelperContext, TagHelperOutput)'s are invoked in the specified Order. Lower values are executed first<br>(Inherited from [TagHelper](https://docs.microsoft.com/en-us/dotnet/api/microsoft.aspnetcore.razor.taghelpers.taghelper)) | 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | PositionCursor | Gets or sets a [condition expression](/reference/asna-qsys-expo/expo-model/conditional-properties-overview.html#condition-expression) string determining if the cursor should be positioned to this input-capable field.<br>(Inherited from [DdsFieldBase](/reference/asna-qsys-expo/expo-tags/dds-field-base.html)) | 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | TabIndex | Gets or sets a value indicating that its element can be focused, and where it participates in sequential keyboard navigation (usually with the Tab key, hence the name).<br>(Inherited from [FieldBase](/reference/asna-qsys-expo/expo-tags/field-base.html)) | 
| [TimeAttribute](/reference/asna-qsys-expo/expo-model/time-attribute.html) | TimeFieldAttribute | Gets the TimeAttribute from the Model. | 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | Underline | Gets or sets [condition expression](/reference/asna-qsys-expo/expo-model/conditional-properties-overview.html#condition-expression) string that determines if text should be underlined. Underline is rendered as a bottom-border CSS style.<br>(Inherited from [FieldBase](/reference/asna-qsys-expo/expo-tags/field-base.html)) | 
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

## Fields

| Type | Name | Description
| --- | --- | --- 
| [DdsFileTagHelper](/reference/asna-qsys-expo/expo-tags/dds-file-tag-helper.html) | ddsFile | Gets or sets a value indicating the associated DdsFile tag helper for the field/constant.<br>(Inherited from [FieldBase](/reference/asna-qsys-expo/expo-tags/field-base.html))

<br>
<br>

