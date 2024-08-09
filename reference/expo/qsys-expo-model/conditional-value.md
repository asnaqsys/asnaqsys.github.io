---
title: "ConditionalValue class        | QSYS API Reference Guide"
description: "Defines ConditionalValue class "
last_modified_at: 2024-08-09T17:26:04Z
---

Defines ConditionalValue class

**Namespace:** ASNA.QSys.Expo.Model
**Assembly:** ASNA.QSys.Expo.Model.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>

When describing [ConditionalProperties](/reference/expo/qsys-expo-model/conditional-property.html) such as `FunctionKeys`[RecordAttributes](/reference/expo/qsys-expo-model/record-attribute.html), the Condition is expressed by:

1. A Condition expression.
2. An [Response Indicators](https://www.ibm.com/docs/en/i/7.2?topic=concepts-rpg-iv-indicators) Value. 

For example,

```cs
"F11 11 : !30"
```

| Expression | Response Indicator Value |
| --- | --- |
| `!30` | `11` |

The ConditionalValue for such Function Key specification would read:

*Function Key is Valid when Option Indicator 30 is `Off`. If the Command is issued, the Response Indicator 11 will be set to `On`*

Here is an overview of [Conditional Values concepts](/reference/expo/qsys-expo-model/landing-page-namespace.html#conditional-value).

## Constructors

| Name | Description |
| --- | --- |
| [ConditionalValue()](#conditionalvalue) | Initializes a new instance of the class ConditionalValue
| [ConditionalValue](#conditionalvaluestring-string)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Initializes a new instance of the class ConditionalValue, using the condition and value given as initial values.

### ConditionalValue()

Initializes a new instance of the class ConditionalValue

```cs
ConditionalValue()
```

### ConditionalValue([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Initializes a new instance of the class ConditionalValue, using the condition and value given as initial values.

```cs
ConditionalValue(String, String)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | condition | conditional expression
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | val | result indicator to turn on

## Properties

| Type | Name | Description
| --- | --- | --- 
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | Condition | Gets or sets the option-indicator-condition. Use & and | for (AND OR). Use ! to negate. Example "!76 & 50" meaning: If Not(*Ind76) AND *Ind50 |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | Value | Gets or sets the result-indicator to turn On. One indicator expected. Example: "51" meaning set result *In51=*On |

## Methods

| Signature | Description |
| --- | --- |
| [ToString()](#string-tostring) | Serializes the instance into a string.

### string ToString()

Serializes the instance into a string.

```cs
string ToString()
```
