---
title: "ColorProperty class           | QSYS API Reference Guide"
description: "Defines ColorProperty. Encapsulates the name of a color to be use when rendering fields and constants. "
last_modified_at: 2024-08-08T21:42:10Z
---

Defines ColorProperty. Encapsulates the name of a color to be use when rendering fields and constants.

**Namespace:** ASNA.QSys.Expo.Model
**Assembly:** ASNA.QSys.Expo.Model.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [ConditionalProperty](/reference/expo/qsys-expo-model/conditional-property.html)
<br>
<br>

## Remarks

The class `ColorProperty` is used the evaluate a conditional "Color" expression, like the one given to Displayfile fields in the markup.

For example, the following [RazorPage](https://docs.microsoft.com/en-us/aspnet/core/razor-pages/) element described for a `Char` field that is to be displayed with a color attribute depending on the value of Option Indicator 61: 

```html
<DdsCharField Col="71 For="SFLC.SFL1[rrn].SFFILESTAT" Upper=true Color="Green : !61 , DarkBlue : 61" />
```

The expression is:
```
"Green : !61 , DarkBlue : 61"
```

Which means: Color `Green` if Indicator 61 is *Off, Color `DarkBlue` is Indicator 61 is *On

Note: at Runtime, an instance of the class `ColorProperty` is used to evaluate the Color based on the current value of the Indicator 61 (in this example).


## Constructors

| Name | Description |
| --- | --- |
| [ColorProperty()](#colorproperty) | Initializes a new instance of ColorProperty class
| [ColorProperty](#colorpropertystring)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Initializes a new instance of ColorProperty class with the Conditional Property collection in a string.

### ColorProperty()

Initializes a new instance of ColorProperty class

```cs
ColorProperty()
```

### ColorProperty([String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Initializes a new instance of ColorProperty class with the Conditional Property collection in a string.

```cs
ColorProperty(String)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | propString | conditional property collection initial value
