---
title: "DdsFieldBase class            | QSYS API Reference Guide"
description: "Provides common methods for DdsFields. "
last_modified_at: 2024-08-09T16:19:09Z
---

Provides common methods for DdsFields.

**Namespace:** ASNA.QSys.Expo.Tags
**Assembly:** ASNA.QSys.Expo.Tags.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [TagHelper](https://learn.microsoft.com/en-us/dotnet/api/microsoft.aspnetcore.razor.taghelpers.taghelper?view=aspnetcore-8.0) --> [FieldBase](/reference/expo/qsys-expo-tags/field-base.html)
<br>
<br>

## Remarks

A `FieldBase` is used by tag Helpers that may be bound to a Model field.

As an [abstract class](https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/classes-and-structs/abstract-and-sealed-classes-and-class-members) it cannot be used directly. The `FieldBase` is the class that implements all the common behavior for the rest of the DdsXXXFields: 

[DdsConstant](/reference/expo/qsys-expo-tags/dds-constant-tag-helper.html),
[DdsCharField](/reference/expo/qsys-expo-tags/dds-char-field-tag-helper.html),
[DdsDecField](/reference/expo/qsys-expo-tags/dds-dec-field-tag-helper.html),
[DdsDateField](/reference/expo/qsys-expo-tags/dds-date-field-tag-helper.html),
[DdsDecDateField](/reference/expo/qsys-expo-tags/dds-dec-date-field-tag-helper.html), 

etc.


## Properties

| Type | Name | Description
| --- | --- | --- 
| [ConditionalProperty](/reference/expo/qsys-expo-model/conditional-property.html) | ErrorMessage | Gets or sets a value that indicates conditional property describing the Error Message.  |
| [ConditionalProperty](/reference/expo/qsys-expo-model/conditional-property.html) | ErrorMessageId | Gets or sets a value that indicates conditional property describing the Error Message ID.  |
| [FieldAttribute](/reference/expo/qsys-expo-model/field-attribute.html) | FieldAttribute | When overriden in a derived class, gets a value that indicates the Field Attribute. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | FieldName | Gets the name of the Field. |
| [ModelExpression](https://docs.microsoft.com/en-us/dotnet/api/microsoft.aspnetcore.mvc.viewfeatures.modelexpression) | For | Gets or sets a value that indicates the Model associated with the Mvc tag helper. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | PositionCursor | Gets or sets a value that indicates the conditional expression string determining if the cursor should be positioned to this input-capable field. |
| [FieldUsages](/reference/expo/qsys-expo-model/field-usages.html) | Usage | Gets or sets a value that indicates the Field Usage. |
| [ValuesAttribute](/reference/expo/qsys-expo-model/values-attribute.html) | ValuesAttribute | Gets the ValuesAttribute from the Model. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | VirtualRowCol | Gets or sets a value that indicates the legacy row, col position that the logic may be expecting to identify. Format is 'Row,Col'. May not represent the current position of the tag helper. |

## Methods

| Signature | Description |
| --- | --- |
| [ProcessDdsField](#void-processddsfieldtaghelpercontext-context-taghelperoutput-output)([TagHelperContext](https://learn.microsoft.com/en-us/dotnet/api/microsoft.aspnetcore.razor.taghelpers.taghelpercontext?view=aspnetcore-8.0), [TagHelperOutput](https://learn.microsoft.com/en-us/dotnet/api/microsoft.aspnetcore.razor.taghelpers.taghelperoutput?view=aspnetcore-8.0)) | When overriden in a derived class, method is called by rendering engine to write the HTML output.  
| [ProcessValues](#bool-processvaluestaghelperoutput-output-string-gridcolumnstyle-string-valuestext-string-valuestextoptionseparator)([TagHelperOutput](https://learn.microsoft.com/en-us/dotnet/api/microsoft.aspnetcore.razor.taghelpers.taghelperoutput?view=aspnetcore-8.0), [String&](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Process Display Values.

### void ProcessDdsField([TagHelperContext context](https://learn.microsoft.com/en-us/dotnet/api/microsoft.aspnetcore.razor.taghelpers.taghelpercontext?view=aspnetcore-8.0), [TagHelperOutput output](https://learn.microsoft.com/en-us/dotnet/api/microsoft.aspnetcore.razor.taghelpers.taghelperoutput?view=aspnetcore-8.0))

When overriden in a derived class, method is called by rendering engine to write the HTML output.  

```cs
void ProcessDdsField(TagHelperContext context, TagHelperOutput output)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [TagHelperContext](https://learn.microsoft.com/en-us/dotnet/api/microsoft.aspnetcore.razor.taghelpers.taghelpercontext?view=aspnetcore-8.0) | context | Tag Helper context.
| [TagHelperOutput](https://learn.microsoft.com/en-us/dotnet/api/microsoft.aspnetcore.razor.taghelpers.taghelperoutput?view=aspnetcore-8.0) | output | Tag Helper output.

### bool ProcessValues([TagHelperOutput output](https://learn.microsoft.com/en-us/dotnet/api/microsoft.aspnetcore.razor.taghelpers.taghelperoutput?view=aspnetcore-8.0), [String& gridColumnStyle](https://docs.microsoft.com/en-us/dotnet/api/system.string), [string valuesText](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string valuesTextOptionSeparator](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Process Display Values.

```cs
bool ProcessValues(TagHelperOutput output, String& gridColumnStyle, string valuesText, string valuesTextOptionSeparator)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [TagHelperOutput](https://learn.microsoft.com/en-us/dotnet/api/microsoft.aspnetcore.razor.taghelpers.taghelperoutput?view=aspnetcore-8.0) | output | Class used to represent the output of a input-capable DdsField.
| [String&](https://docs.microsoft.com/en-us/dotnet/api/system.string) | gridColumnStyle | Reference to the string value used for the Grid-column style.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | valuesText | Lists valid display values. Each text description is single-quoted. List is comma separated.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | valuesTextOptionSeparator | String used to separate Value and Text for valuesText. Use null or empty to not use Values.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | 
