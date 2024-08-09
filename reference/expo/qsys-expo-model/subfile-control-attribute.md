---
title: "SubfileControlAttribute class | QSYS API Reference Guide"
description: "Defines Subfile Control Attribute on a type "
last_modified_at: 2024-08-09T17:26:04Z
---

Defines Subfile Control Attribute on a type

**Namespace:** ASNA.QSys.Expo.Model
**Assembly:** ASNA.QSys.Expo.Model.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [Attribute](https://docs.microsoft.com/en-us/dotnet/api/system.attribute) --> [BaseRecordAttribute](/reference/expo/qsys-expo-model/base-record-attribute.html) --> [RecordAttribute](/reference/expo/qsys-expo-model/record-attribute.html)
<br>
<br>

## Remarks

The `SubfileControlAttribute` class is a specialized class derived from [RecordAttribute class](/reference/expo/qsys-expo-model/base-record-attribute.html) that provides meta-data to express in the Model [Subfile Control Displayfile Record](https://www.ibm.com/docs/en/i/7.4?topic=80-sflctl-subfile-control-keyword-display-files) [DDS](https://www.ibm.com/docs/en/i/7.4?topic=dds-display-files) keywords.

The following excerpt of code describes to the Subfile Control model, several properties such as when to Clear the controlled Subfile, when to Display the records and fields.

```cs
[
    SubfileControl(ClearRecords : "90",
        FunctionKeys = "PageUp 51:!76;PageDown 50:!77",
        DisplayFields = "!90",
        DisplayRecords = "!90",
        Size = 20,
        IsExpandable = false,
        EraseFormats = "CUSTREC SALESREC"
    )
]
public class SFLC_Model : SubfileControlModel
{
    .
    .
    .
}
```
>Note how the first attribute is passed as a parameter to the constructor (using colon syntax), while the rest as attributes to the class (using assignment syntax). 


## Constructors

| Name | Description |
| --- | --- |
| [SubfileControlAttribute](#subfilecontrolattributestring)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Initializes a new SubfileControlAttribute instance.

### SubfileControlAttribute([String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Initializes a new SubfileControlAttribute instance.

```cs
SubfileControlAttribute(String)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | ClearRecords | Conditional Indicator expression that when true indicates that the Records in the Subfile should be cleared

## Properties

| Type | Name | Description
| --- | --- | --- 
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | ClearRecords | Gets the conditional indicator expression that determines if the records of the Subfile should be cleared  |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | DisplayFields | Gets the conditional indicator expression that determines if the Fields in the Subfile Controller should display |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | DisplayRecords | Gets the conditional indicator expression that determines if the Subfile Records should display |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | FoldDropIndicator | Gets or Sets the Fold/Drop toggle indicator numeric value. Defaults to zero (Fold/Drop does not apply) |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | InitializeRecords | Gets the conditional indicator expression that determines if Subfile Records should be initialized |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | InitNotActive | Gets or sets a boolean that, when set to "true", when initializing the subfile records (because expression for InitializeRecords evaluates to true), the added records to the subfile will be non-active - meaning that they are not part of the subfile yet until the records are written to, or the user enters values into them -. |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | IsExpandable | Gets or sets a boolean value indicating if the Subfile can expand |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | ProgramQ | Gets or sets the value of the PGMQ on a Message subfile |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | Size | Gets or sets the Subfile Size. Defaults to zero records. |

## Methods

| Signature | Description |
| --- | --- |
| [GetFrom](#subfilecontrolattribute-getfromtype-type)([Type](https://docs.microsoft.com/en-us/dotnet/api/system.type)) | Gets a SubfileControlAttribute from the Custom attributes on a type

### SubfileControlAttribute GetFrom([Type type](https://docs.microsoft.com/en-us/dotnet/api/system.type))

Gets a SubfileControlAttribute from the Custom attributes on a type

```cs
SubfileControlAttribute GetFrom(Type type)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Type](https://docs.microsoft.com/en-us/dotnet/api/system.type) | type | Input object type

#### Returns

| Type | Description
| --- | ---
| [SubfileControlAttribute](/reference/expo/qsys-expo-model/subfile-control-attribute.html) | the subfile control attribute
