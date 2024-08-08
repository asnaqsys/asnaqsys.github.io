---
title: "ConditionalProperty class     | QSYS API Reference Guide"
description: "Defines a ConditionalProperty "
last_modified_at: 2024-08-08T21:42:10Z
---

Defines a ConditionalProperty

**Namespace:** ASNA.QSys.Expo.Model
**Assembly:** ASNA.QSys.Expo.Model.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>

## Remarks

Defines a ConditionalProperty.

A ConditionalProperty represents a collection of [Conditional Values](/reference/expo/qsys-expo-model/landing-page-namespace.html#conditional-value)

The ConditionalProperty class instance may be instantiated with an array of [Conditional Values](/reference/expo/qsys-expo-model/landing-page-namespace.html#conditional-value), or from a string representation.  

Here is an overview of [Conditional Property concepts](/reference/expo/qsys-expo-model/landing-page-namespace.html#conditional-property).


## Constructors

| Name | Description |
| --- | --- |
| [ConditionalProperty()](#conditionalproperty) | Initializes a new instance of ConditionalProperty class
| [ConditionalProperty](#conditionalpropertyconditionalvalue)([ConditionalValue\[\]](/reference/expo/qsys-expo-model/conditional-value.html)) | Initializes a new instance of ConditionalProperty class to the ConditionalValue collection given.
| [ConditionalProperty](#conditionalpropertystring)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Initializes a new instance of ConditionalProperty class by de-serializing the given collection in the form of a string

### ConditionalProperty()

Initializes a new instance of ConditionalProperty class

```cs
ConditionalProperty()
```

### ConditionalProperty([ConditionalValue\[\]](/reference/expo/qsys-expo-model/conditional-value.html))

Initializes a new instance of ConditionalProperty class to the ConditionalValue collection given.

```cs
ConditionalProperty(ConditionalValue[])
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [ConditionalValue\[\]](/reference/expo/qsys-expo-model/conditional-value.html) | Property | Initial ConditionalValue collection

### ConditionalProperty([String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Initializes a new instance of ConditionalProperty class by de-serializing the given collection in the form of a string

```cs
ConditionalProperty(String)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | propString | Serializes initial ConditionalValue collection

## Properties

| Type | Name | Description
| --- | --- | --- 
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | IsGiven | Gets a boolean value indicating if the ConditionalValue collection is NOT empty |
| [ConditionalValue\[\]](/reference/expo/qsys-expo-model/conditional-value.html) | Property | Gets or sets the ConditionalValue collection encapsulated by the Property |

## Methods

| Signature | Description |
| --- | --- |
| [Reset()](#void-reset) | Clears the encapsulated ConditionalValue collection
| [ToString()](#string-tostring) | Serializes the ConditionalValue collection into a string.

### void Reset()

Clears the encapsulated ConditionalValue collection

```cs
void Reset()
```

### string ToString()

Serializes the ConditionalValue collection into a string.

```cs
string ToString()
```
