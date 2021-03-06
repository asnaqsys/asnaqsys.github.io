---
title: SubfileRecordAttribute Class
---

Defines Subfile Record Attribute on a type

**Namespace:** ASNA.QSys.Expo.Model <br/>
**Assembly:** ASNA.QSys.Expo.Model

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [Attribute](https://docs.microsoft.com/en-us/dotnet/api/system.attribute) --> [BaseRecordAttribute](/reference/asna-qsys-expo/expo-model/base-record-attribute.html) --> SubfileRecordAttribute

<br>
<br>

## Remarks

The `SubfileRecordAttribute` class is a specialized class derived from [RecordAttribute class](/reference/asna-qsys-expo/expo-model/record-attribute.html) that provides meta-data to express in the Model [Subfile Displayfile Record](https://www.ibm.com/docs/en/i/7.4?topic=80-sfl-subfile-keyword-display-files) [DDS](https://www.ibm.com/docs/en/i/7.4?topic=dds-display-files) keywords.

The following excerpt of code describes to the `SFL1` Subfile model, the attribute `NextChanged` corresponding to the [legacy SFLNXTCHG DDS keyword](https://www.ibm.com/docs/en/i/7.4?topic=80-sflnxtchg-subfile-next-changed-keyword-display-files).

```cs
[
    SubfileRecord(NextChanged = "14")
]
public class SFL1_Model : SubfileRecordModel
{
    [Char(1, Protect = "*True")]
    public string SFCOLOR { get; set; }

    [Values(typeof(Decimal),"00","02","03","05","07","09","10","11")]
    [Dec(2, 0)]
    public decimal SFSEL { get; set; }
    .
    .
    .
}
```

<br>
<br>

## Properties

| Type | Name | Description | Indexer
| --- | --- | --- | --- 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | ChangeIndicator | Gets or sets the value that represents the Change indicator<br>(Inherited from [BaseRecordAttribute](/reference/asna-qsys-expo/expo-model/base-record-attribute.html)) | 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | FormatLevel | Gets or sets the Record Format Level Check hash code as a string<br>(Inherited from [BaseRecordAttribute](/reference/asna-qsys-expo/expo-model/base-record-attribute.html)) | 
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | IsMessageSubfile | Sets or gets a boolean value to indicate that the Subfile record is the Message Subfile. | 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | NextChanged | Sets or gets a conditional indicator expression that determines if the record should be set as changed, to force the get-next-changed operation to succeed (SFLNXTCHG). Defaults to null | 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | SetOffIndicators | Gets or sets a collection of Indicators to Set Off. The collection is a comma separated string<br>(Inherited from [BaseRecordAttribute](/reference/asna-qsys-expo/expo-model/base-record-attribute.html)) | 

<br>
<br>

## Methods

| Type | Name | Description | Return Description 
| --- | --- | --- | --- 
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | [Equals](https://docs.microsoft.com/en-us/dotnet/api/system.object.equals)([Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | Determines whether the specified object is equal to the current object.<br>(Inherited from [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | true if the specified object is equal to the current object; otherwise, false.
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [Finalize](https://docs.microsoft.com/en-us/dotnet/api/system.object.finalize)() | Allows an object to try to free resources and perform other cleanup operations before it is reclaimed by garbage collection.<br>(Inherited from [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | 
| [Attribute](https://docs.microsoft.com/en-us/dotnet/api/system.attribute) | [GetCustomAttribute](https://docs.microsoft.com/en-us/dotnet/api/system.attribute.getcustomattribute)([Assembly](https://docs.microsoft.com/en-us/dotnet/api/system.reflection.assembly), [Type](https://docs.microsoft.com/en-us/dotnet/api/system.type)) | Retrieves a custom attribute applied to a specified assembly. Parameters specify the assembly and the type of the custom attribute to search for.<br>(Inherited from [Attribute](https://docs.microsoft.com/en-us/dotnet/api/system.attribute)) | 
| [Attribute[]](https://docs.microsoft.com/en-us/dotnet/api/system.attribute) | [GetCustomAttributes](https://docs.microsoft.com/en-us/dotnet/api/system.attribute.getcustomattributes)([Assembly]($$TODO-Assembly.html)) | Retrieves an array of the custom attributes applied to an assembly. A parameter specifies the assembly.<br>(Inherited from [Attribute](https://docs.microsoft.com/en-us/dotnet/api/system.attribute)) | An Attribute array that contains the custom attributes applied to element, or an empty array if no such custom attributes exist.
| [SubfileRecordAttribute](/reference/asna-qsys-expo/expo-model/subfile-record-attribute.html) | [GetFrom](#getfromtype)([Type](https://docs.microsoft.com/en-us/dotnet/api/system.type)) | Gets the SubfileRecordAttribute from the Custom attributes on a type. | the subfile record attribute
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | [GetHashCode](https://docs.microsoft.com/en-us/dotnet/api/system.object.gethashcode)() | Serves as the default hash function.<br>(Inherited from [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | A hash code for the current object.
| [Type](https://docs.microsoft.com/en-us/dotnet/api/system.type) | [GetType](https://docs.microsoft.com/en-us/dotnet/api/system.object.gettype)() | Gets the Type of the current instance.<br>(Inherited from [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | The exact runtime type of the current instance.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | [IsDefined](https://docs.microsoft.com/en-us/dotnet/api/system.attribute.isdefined)([Assembly]($$TODO-Assembly.html), [Type](https://docs.microsoft.com/en-us/dotnet/api/system.type)) | Determines whether any custom attributes are applied to an assembly. Parameters specify the assembly, and the type of the custom attribute to search for.<br>(Inherited from [Attribute](https://docs.microsoft.com/en-us/dotnet/api/system.attribute)) | true if a custom attribute of type attributeType is applied to element; otherwise, false.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | [Match](https://docs.microsoft.com/en-us/dotnet/api/system.attribute.match)([Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | When overridden in a derived class, returns a value that indicates whether this instance equals a specified object.<br>(Inherited from [Attribute](https://docs.microsoft.com/en-us/dotnet/api/system.attribute)) | An Object to compare with this instance of Attribute.
| [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) | [MemberwiseClone](https://docs.microsoft.com/en-us/dotnet/api/system.object.memberwiseclone)() | Creates a shallow copy of the current Object.<br>(Inherited from [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | A shallow copy of the current Object.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | [ReferenceEquals](https://docs.microsoft.com/en-us/dotnet/api/system.object.referenceequals)([Object](https://docs.microsoft.com/en-us/dotnet/api/system.object), [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | Determines whether the specified Object instances are the same instance.<br>(Inherited from [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | true if objA is the same instance as objB or if both are null; otherwise, false.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | [ToString](https://docs.microsoft.com/en-us/dotnet/api/system.object.tostring)() | Returns a string that represents the current object.<br>(Inherited from [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | A string that represents the current object.

<br>
<br>

### GetFrom([Type](https://docs.microsoft.com/en-us/dotnet/api/system.type))

Gets the SubfileRecordAttribute from the Custom attributes on a type.

```cs
GetFrom(Type type);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Type](https://docs.microsoft.com/en-us/dotnet/api/system.type) | type | The object Type 

#### Returns

[SubfileRecordAttribute](/reference/asna-qsys-expo/expo-model/subfile-record-attribute.html)

the subfile record attribute


<br>
<br>

