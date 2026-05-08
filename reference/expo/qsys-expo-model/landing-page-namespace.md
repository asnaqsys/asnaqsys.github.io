---
title: "ASNA.QSys.Expo.Model Namespace"
description: TOC Landing page for ASNA.QSys.Expo.Model Namespace
---

## Remarks

The `ASNA.QSys.Expo.Model` namespace is a key part of the ASNA QSys system. It contains classes, interfaces, enumerations, and structures that provide the fundamental functionalities of the system. This namespace is designed to provide a comprehensive set of tools for building, running, and managing ASNA applications.

Some of the key features provided by this namespace include:

- Runtime support for ASNA QSys applications, including data management, error handling, and system utilities.
- Interfaces for interacting with various parts of the ASNA system, such as the database, user interface, and system services.
- Enumerations that define the constants used throughout the ASNA system.
- Structures that encapsulate small groups of related variables, providing a convenient way to group related data.

This namespace is the parent topic in the Table of Contents, and it includes pages that describe the classes, interfaces, enumerations, and structures defined within it. Each of these pages provides detailed information about the usage, properties, methods, and events of each item.

Developers working with the ASNA QSys system should familiarize themselves with the contents of this namespace, as it forms the basis for most ASNA development tasks.

## Indicator expressions
Some of the properties of the Expo Tags and Model can be conditioned with an indicator expression. Monarch migrations preserves the conditional indicators on DDS fields, constants and keywords as conditional elements. 

The general term for these elements are conditional indicator expressions and are given as string values in Expo Tag Helpers properties and Expo Model Attribute properties.

These conditional strings are composed of indicator numbers, operators and values. 


### Condition Expression
The following are the syntax elements used by Condition Expressions:

 + **nn** Test for Indicator nn
 + **!** unary operator NOT
 + **&** binary operator AND
 + **\|** binary operator OR
 + **()** to specify operator precedence

For example, the following string contains an indicator expression:
```   
   01 & !02 & 03 & 04 | (05 & 06) | 07
```

The indicator expression will be evaluated as being **true** if: 
 + Indicators 01, 03 and 04 are ON (='1') AND indicator 02 is OFF (='0')
 + OR if Indicators 05 and 06 are ON
 + OR if Indicator 07 is ON

The special values *True, and *False can be used in place of an indicator.

The natural precedence of the operators are, from highest to lowest:
 + **!** unary operator NOT
 + **&** binary operator AND
 + **\|** binary operator OR

The use of parenthesis can specify a specific order of precedence in the evaluation of the expression.

The indicator expression above could have been generated from the following DDS sequence:

```
       01N02 03
     A 04
     O 05 06
     O 07
```

A condition is an expression involving indicators and operators as explained above. The special values *True, *False can be used in place of an indicator.

| Syntax  | Expression |
| ------- | ---------- |
| Example |	03 & !99   |
| Meaning |	**True** if *IN03 is *ON and *IN99 is *OFF; otherwise **False**.


### Conditional Value
A Conditional Value is a value followed by a colon and then a Conditional expression. It is possible to omit either the Value or Condition, but not both. If necessary, the Value should be enclosed in quotes.

|Syntax	  | Value : Condition
| ------- | ---------- |
|Example  | Red: 03 & !99
|Meaning  | The value **Red** is selected if *IN03 is *ON and *IN99 is *OFF

The Conditional Value functionality is implemented in the [ConditionalValue Class](/reference/expo/qsys-expo-model/conditional-value.html)

### Conditional Property
A Conditional Property is an array of comma separated Conditional Values.

|Syntax	  | Conditional value, Conditional value, Conditional value...
| ------- | ---------- |
|Example  | Red : 03 & !99, Green : 06, Blue : 05 \| 03
|Meaning  | The value **Red** is selected if *IN03 is *ON and *IN99 is *OFF <br/>otherwise, the value **Green** is selected if *IN06 is *ON <br/>otherwise, the value **Blue** is selected if *IN05 or *IN03 are *ON


The list of conditional values is processed from start to finish evaluating the "condition" controlling the "value." As soon as a condition is met, the associated value is used for the property. 

The Conditional Property functionality is implemented in the [ConditionalProperty Class](/reference/expo/qsys-expo-model/conditional-property.html)


### Conditional Property Sets
Conditional Property Sets are semi-colon separated sets of Conditional Properties. These are use for Attention and Function Keys.
