---
title: ColorProperty Class
---

<style>
tr td:first-child {
    white-space: nowrap;
}
</style>

Defines ColorProperty

**Namespace:** ASNA.QSys.Expo.Model <br/>
**Assembly:** ASNA.QSys.Expo.Model

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [ConditionalProperty](/reference/asna-qsys-expo/expo-model/conditional-property.html) --> ColorProperty

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

<br>
<br>

## Constructors

| Name |  Description 
| --- | --- 
| [ColorProperty](#colorproperty)() | Initializes a new instance of ColorProperty class 
| [ColorProperty](#colorpropertystring)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Initializes a new instance of ColorProperty class with the Conditional Property collection in a string. 

<br>

### ColorProperty(  )

Initializes a new instance of ColorProperty class

```cs
ColorProperty(  );
```


<br>

### ColorProperty( [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) )

Initializes a new instance of ColorProperty class with the Conditional Property collection in a string.

```cs
ColorProperty( String propString );
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | propString | conditional property collection initial value 

<br>


<br>
<br>

## Properties

| Type | Name | Description | Indexer
| --- | --- | --- | --- 
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | IsGiven | Gets a boolean value indicating if the ConditionalValue collection is NOT empty<br>(Inherited from [ConditionalProperty](/reference/asna-qsys-expo/expo-model/conditional-property.html)) | 
| [ConditionalValue[]](/reference/asna-qsys-expo/expo-model/conditional-value.html) | Property | Gets or sets the ConditionalValue collection encapsulated by the Property<br>(Inherited from [ConditionalProperty](/reference/asna-qsys-expo/expo-model/conditional-property.html)) | 

<br>
<br>

## Methods

| Type | Name | Description | Return Description 
| --- | --- | --- | --- 
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | [Equals](https://docs.microsoft.com/en-us/dotnet/api/system.object.equals)([Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | Determines whether the specified object is equal to the current object.<br>(Inherited from [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | true if the specified object is equal to the current object; otherwise, false.
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [Finalize](https://docs.microsoft.com/en-us/dotnet/api/system.object.finalize)() | Allows an object to try to free resources and perform other cleanup operations before it is reclaimed by garbage collection.<br>(Inherited from [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | [GetHashCode](https://docs.microsoft.com/en-us/dotnet/api/system.object.gethashcode)() | Serves as the default hash function.<br>(Inherited from [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | A hash code for the current object.
| [Type](https://docs.microsoft.com/en-us/dotnet/api/system.type) | [GetType](https://docs.microsoft.com/en-us/dotnet/api/system.object.gettype)() | Gets the Type of the current instance.<br>(Inherited from [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | The exact runtime type of the current instance.
| [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) | [MemberwiseClone](https://docs.microsoft.com/en-us/dotnet/api/system.object.memberwiseclone)() | Creates a shallow copy of the current Object.<br>(Inherited from [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | A shallow copy of the current Object.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | [ReferenceEquals](https://docs.microsoft.com/en-us/dotnet/api/system.object.referenceequals)([Object](https://docs.microsoft.com/en-us/dotnet/api/system.object), [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | Determines whether the specified Object instances are the same instance.<br>(Inherited from [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | true if objA is the same instance as objB or if both are null; otherwise, false.
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [Reset](/reference/asna-qsys-expo/expo-model/conditional-property.html#reset)() | Clears the encapsulated ConditionalValue collection<br>(Inherited from [ConditionalProperty](/reference/asna-qsys-expo/expo-model/conditional-property.html)) | 
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | [ToString](https://docs.microsoft.com/en-us/dotnet/api/system.object.tostring)() | Returns a string that represents the current object.<br>(Inherited from [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | A string that represents the current object.

<br>
<br>

