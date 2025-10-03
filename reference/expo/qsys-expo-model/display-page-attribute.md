---
title: "DisplayPageAttribute class    | QSYS API Reference Guide"
description: "Defines a Display Page Attribute  "
last_modified_at: 2024-08-09T17:26:04Z
---

Defines a Display Page Attribute 

**Namespace:** ASNA.QSys.Expo.Model
**Assembly:** ASNA.QSys.Expo.Model.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [Attribute](https://docs.microsoft.com/en-us/dotnet/api/system.attribute)
<br>
<br>

## Remarks

Model Record classes may be annotated with attributes to specify meta-data to control the Display page.

For example,


```cs
[
    SubfileControl(
        FunctionKeys = "F9 09;PageUp 51:!76;PageDown 50:!77"
    )
]
public class SFLC_Model : SubfileControlModel
{
```

Specifies that the `SubfileControl` named **SFLC** enables `F9`, `PageUp` and `PageDown` keys (`F9` always, `PageUp` conditioned to Option Indicator *not* 76 and `PageDown` conditioned to Option Indicator *not* 77), with the Response indicators 09, 51 and 50 to turn on (when such key is pressed). Since this attribute is for "Function Keys" (as opposed to "AttentionKeys") then, `Input Data` is transmitted from the browser to the server.


## Properties

| Type | Name | Description
| --- | --- | --- 
| [AidKey](/reference/expo/qsys-expo-model/aid-key.html) | AlternateHelpKey | Gets or sets the Alternate Help Key. Defaults to AidKey.None, valid values are AidKey.F1 through AidKey.F24 |
| [AidKey](/reference/expo/qsys-expo-model/aid-key.html) | AlternatePageUpKey | Gets or sets the Alternate PageUp Key. Defaults to AidKey.None, valid values are AidKey.F1 through AidKey.F24 |
| [AidKey](/reference/expo/qsys-expo-model/aid-key.html) | AlternatePageDownKey | Gets or sets the Alternate PageDown Key. Defaults to AidKey.None, valid values are AidKey.F1 through AidKey.F24 |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | AttentionKeys | Gets or sets the valid Attention Key collection as a semi-colon separated list of key expressions. Each expression has the form: key result-indicator : option-indicator. To negate option-indicator precede indicator with ! |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | CommandKeyIndicator | Gets or sets the Command Key indicator number |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | FunctionKeys | Gets or sets the valid Function Key collection as a semi-colon separated list of key expressions. Each expression has the form: key result-indicator : option-indicator. To negate option-indicator precede indicator with ! |

## Methods

| Signature | Description |
| --- | --- |
| [GetFrom](#displaypageattribute-getfromtype-type)([Type](https://docs.microsoft.com/en-us/dotnet/api/system.type)) | Gets a DisplayPageAttribute of a particular type from the custom attributes.

### DisplayPageAttribute GetFrom([Type type](https://docs.microsoft.com/en-us/dotnet/api/system.type))

Gets a DisplayPageAttribute of a particular type from the custom attributes.

```cs
DisplayPageAttribute GetFrom(Type type)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Type](https://docs.microsoft.com/en-us/dotnet/api/system.type) | type | Object type

#### Returns

| Type | Description
| --- | ---
| [DisplayPageAttribute](/reference/expo/qsys-expo-model/display-page-attribute.html) | The attribute
