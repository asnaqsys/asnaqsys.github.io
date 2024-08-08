---
title: "RecordAttribute class         | QSYS API Reference Guide"
description: "Defines  the Record Attribute on a type "
last_modified_at: 2024-08-08T21:42:10Z
---

Defines  the Record Attribute on a type

**Namespace:** ASNA.QSys.Expo.Model
**Assembly:** ASNA.QSys.Expo.Model.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [Attribute](https://docs.microsoft.com/en-us/dotnet/api/system.attribute) --> [BaseRecordAttribute](/reference/expo/qsys-expo-model/base-record-attribute.html)
<br>
<br>

## Remarks

IBM i Displayfiles allows the designer to specify metadata (via keywords) on records that describe how records should interact with user. [DDS](https://www.ibm.com/docs/en/i/7.1?topic=80-sflctl-subfile-control-keyword-display-files) allows to indicate on a particular Subfile control record specification how the Subfile that it controls should behave. 

For example, the following DDS specifications defines Subfile Control `SFLC` controlling Subfile `SFL1` with a particular size, activating `PgUp` and `PgDn` keys when certain indicators are `on`, when to clear the subfile records, when to display them etc.

```
0028.00     A          R SFLC                      SFLCTL(SFL1)                        000000
0030.00     A                                      SFLSIZ(0014)                        000000
0031.00     A                                      SFLPAG(0014)                        000000
0033.00     A N77                                  ROLLUP(50)                          000000
0034.00     A N76                                  ROLLDOWN(51)                        000000
0037.00     A N90                                  SFLDSP                              000000
0038.00     A N90                                  SFLDSPCTL                           000000
0039.00     A  90                                  SFLCLR                              000000
```

Razor syntax nor HTML syntax use the concept of Indicators. Records in Expo may include attributes, such as `FunctionKeys`, `DisplayFields`, `DisplayRecords` (indicated below), that complete the specification.

```cs
[
    SubfileControl(ClearRecords : "90",
        FunctionKeys = "F9 09;PageUp 51:!76;PageDown 50:!77",
        DisplayFields = "!90",
        DisplayRecords = "!90",
        Size = 14,
        IsExpandable = false,
        EraseFormats = "CUSTREC SALESREC"
    )
]
public class SFLC_Model : SubfileControlModel
{
```

The name indicated in C# syntax for the Record Attributes maps to the Properties listed on this class.

## Properties

| Type | Name | Description
| --- | --- | --- 
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | Alias | Gets or sets the Alias (alternative) name of a Record |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | AttentionKeys | Gets or sets the valid Attention Key collection as a semi-colon separated list of key expressions. Each expression has the form: key result-indicator : option-indicator. To negate option-indicator precede indicator with ! |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | CommandKeyIndicator | Gets or sets the Command Key Indicator number |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | EraseFormats | Gets or sets a collection of Record Formats to Erase. The string is a space-separated list of format names. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | FunctionKeys | Gets or sets the valid Function Key collection as a semi-colon separated list of key expressions. Each expression has the form: key result-indicator : option-indicator. To negate option-indicator precede indicator with ! |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | ReturnSameData | Gets or sets if the posted Form's data should be not be changed. Defaults to false |

## Methods

| Signature | Description |
| --- | --- |
| [GetFrom](#recordattribute-getfromtype-type)([Type](https://docs.microsoft.com/en-us/dotnet/api/system.type)) | Gets the RecordAttribute from the custom attributes of a Type

### RecordAttribute GetFrom([Type type](https://docs.microsoft.com/en-us/dotnet/api/system.type))

Gets the RecordAttribute from the custom attributes of a Type

```cs
RecordAttribute GetFrom(Type type)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Type](https://docs.microsoft.com/en-us/dotnet/api/system.type) | type | The object type

#### Returns

| Type | Description
| --- | ---
| [RecordAttribute](/reference/expo/qsys-expo-model/record-attribute.html) | the record attribute
