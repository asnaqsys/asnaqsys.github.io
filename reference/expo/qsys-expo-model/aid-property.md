---
title: "AidProperty class             | QSYS API Reference Guide"
description: "Specifies which resulting indicator to turn on for each possible AID key. Each Key might specify multiple indicators, each one conditioned via an bool"
last_modified_at: 2024-08-09T17:26:04Z
---

Specifies which resulting indicator to turn on for each possible AID key. Each Key might specify multiple indicators, each one conditioned via an boolean expression.

**Namespace:** ASNA.QSys.Expo.Model
**Assembly:** ASNA.QSys.Expo.Model.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>

## Remarks

Specifies which resulting indicator to turn on for each possible AID key. Each Key might specify multiple indicators, each one conditioned via an boolean expression.

IBM i Display file definition (DDS) has two record-level keywords that specify what to do when Command keys are issued by user input on a Browser:

1. [CA (Command Attention)](https://www.ibm.com/docs/en/i/7.1?topic=80-cann-command-attention-keyword-display-files)
2. [CF (Command Function)](https://www.ibm.com/docs/en/i/7.1?topic=80-cfnn-command-function-keyword-display-files) 

Both are used to specify that a particular command-key is available (other not listed are not allowed). Availability may be conditioned to an expression based on values of Option [Indicators](https://www.ibm.com/docs/en/i/7.2?topic=concepts-rpg-iv-indicators) set by the Application Logic.

Available commands are described by a number from 1 to 24 (corresponding to keyboard keys F1 to F12, and Shift F1 to Shift F12). Browser Pages may assign commands to clickable buttons.

In addition, the keyword specifies which [Response Indicator](https://www.ibm.com/docs/en/i/7.2?topic=concepts-rpg-iv-indicators) should turn **ON** when Command is issued. The Application Logic has access to such response indicators.

The difference between command "Attention" and "Function" is that an Attention command will *not* submit form data, while a Function command will.

A Record may define more than one CA and/or more than one CF.

Expo Display Page's Record Model class allows for the definition of Attention and Function commands using the following two attributes:

1. [AttentionKeys](/reference/expo/qsys-expo-model/base-record-attribute.html)
2. [FunctionKeys](/reference/expo/qsys-expo-model/base-record-attribute.html)

To specify a collection of command keys, a string is used in the C# declaration, like in the following example:

```cs
[
    Record(FunctionKeys = "F4 04;F6 06:!30;F11 11:!30;F12 12")
]
public class MyRecord_Model : RecordModel
```

In the example above, if we break the string at the semi-colon, we get:


1. `"F4 04"`
2. `"F6 06 : !30"`
3. `"F11 11 : !30"`
4. `"F12 12"`

Four Available Function Commands `F4, F6, F11 and F12`.

`F4` and `F12` are always available (not conditioned).
`F6` and `F11` are *only* available if `*IN30` (Option Indicator 30) is **not** *ON*. 

>Notice the use of `!` in the condition expression syntax, to negate the condition. 

Furthermore, the following [Response Indicators](https://www.ibm.com/docs/en/i/7.2?topic=concepts-rpg-iv-indicators) will be set, when a particular Command is issued. 

| Command | Response Indicator is set |
| --- | --- |
| `F4` | *IN04 |
| `F6` | *IN06 |
| `F11` | *IN11 |
| `F12` | *IN12 |

Note:
1. All *other* indicators are reset.
2. The response indicator can be any indicator (in the example they match - which may be common practice technique - but is not required).

The class `AidProperty` allows for processing such string attributes. It parses the collection and provides access to individual [Conditional Properties](/reference/expo/qsys-expo-model/conditional-property.html)

## Constructors

| Name | Description |
| --- | --- |
| [AidProperty()](#aidproperty) | Initializes a new AidProperty instance
| [AidProperty](#aidpropertystring)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Initializes a new AidProperty instance to the values found in aidString collection (semi-colon separated conditional key expressions)

### AidProperty()

Initializes a new AidProperty instance

```cs
AidProperty()
```

### AidProperty([String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Initializes a new AidProperty instance to the values found in aidString collection (semi-colon separated conditional key expressions)

```cs
AidProperty(String)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | aidString | the string initializer

## Properties

| Type | Name | Description
| --- | --- | --- 
| [ConditionalProperty\[\]](/reference/expo/qsys-expo-model/conditional-property.html) | condAid | Gets or sets the Array of ConditionalProperty items  |
| [ConditionalProperty\[\]](/reference/expo/qsys-expo-model/conditional-property.html) | ConditionalAid | Gets the Conditional Property collection |
| [ConditionalProperty](/reference/expo/qsys-expo-model/conditional-property.html) | Item | Gets the element indexed by aidKey from the Conditional Property collection. |

## Methods

| Signature | Description |
| --- | --- |
| [GetValidValues()](#string--getvalidvalues) | Gets the valid values collection (string array)
| [Reset()](#void-reset) | Resets the ConditionalProperty Array to its initial values

### String[] GetValidValues()

Gets the valid values collection (string array)

```cs
String[] GetValidValues()
```

### void Reset()

Resets the ConditionalProperty Array to its initial values

```cs
void Reset()
```
