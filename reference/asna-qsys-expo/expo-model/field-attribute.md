---
title: FieldAttribute Class
---

Provides Displayfile field attributes

**Namespace:** ASNA.QSys.Expo.Model <br/>
**Assembly:** ASNA.QSys.Expo.Model

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [Attribute](https://docs.microsoft.com/en-us/dotnet/api/system.attribute) --> FieldAttribute

<br>
<br>

## Remarks

IBM i Displayfiles allows the designer to specify metadata (via keywords) on fields that describe how fields should interact with user. For example, [DDS](https://www.ibm.com/docs/en/i/7.1?topic=ddf-dds-keyword-entries-display-files-positions-45-through-80) allows th indicate that a particular field on a records should be [protected](https://www.ibm.com/docs/en/i/7.1?topic=80-dspatr-display-attribute-keyword-display-files) from input, conditioned to a particular option indicator. 

For example, the following DDS specifications define field `SITMNBR` (in Record format `ORDLINE`), where not only does it describe the type and length of the display field, but the fact that when Indicator 88 is `On`, the field should be protected from input (aka read-only).

```
0076.00     A            SITMNBR        9Y 0B  3 15                                    000000
0078.00     A  88                                  DSPATR(PR)                          000000
```

Razor syntax nor HTML syntax use the concept of Indicators. Fields in Expo may include attributes, such as `Protect` (indicated below), that complete the specification.

```cs
public class ORDLINE_Model : RecordModel
{
    .
    .
    .

    [Dec(9, 0, Protect = "88")]
    public decimal SITMNBR { get; set; }

   .
   .
   .
}
```

The name indicated in C# syntax for the Field Attributes maps to the Properties listed on this class.

<br>
<br>

## Properties

| Type | Name | Description | Indexer
| --- | --- | --- | --- 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | Alias | Field Alias name | 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | BlanksIndicator | Blanks indicator | 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | ChangeIndicator | Change indicator | 
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | OutputData | Output Data | 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | Protect | Protect indicator | 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | ProtectCodeFieldName | Protect Code field name | 

<br>
<br>

## Methods

| Type | Name | Description | Return Description 
| --- | --- | --- | --- 
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | [Equals](https://docs.microsoft.com/en-us/dotnet/api/system.object.equals)([Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | Determines whether the specified object is equal to the current object.<br>(Inherited from [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | true if the specified object is equal to the current object; otherwise, false.
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [Finalize](https://docs.microsoft.com/en-us/dotnet/api/system.object.finalize)() | Allows an object to try to free resources and perform other cleanup operations before it is reclaimed by garbage collection.<br>(Inherited from [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | 
| [Attribute](https://docs.microsoft.com/en-us/dotnet/api/system.attribute) | [GetCustomAttribute](https://docs.microsoft.com/en-us/dotnet/api/system.attribute.getcustomattribute)([Assembly](https://docs.microsoft.com/en-us/dotnet/api/system.reflection.assembly), [Type](https://docs.microsoft.com/en-us/dotnet/api/system.type)) | Retrieves a custom attribute applied to a specified assembly. Parameters specify the assembly and the type of the custom attribute to search for.<br>(Inherited from [Attribute](https://docs.microsoft.com/en-us/dotnet/api/system.attribute)) | 
| [Attribute[]](https://docs.microsoft.com/en-us/dotnet/api/system.attribute) | [GetCustomAttributes](https://docs.microsoft.com/en-us/dotnet/api/system.attribute.getcustomattributes)([Assembly]($$TODO-Assembly.html)) | Retrieves an array of the custom attributes applied to an assembly. A parameter specifies the assembly.<br>(Inherited from [Attribute](https://docs.microsoft.com/en-us/dotnet/api/system.attribute)) | An Attribute array that contains the custom attributes applied to element, or an empty array if no such custom attributes exist.
| [FieldAttribute](/reference/asna-qsys-expo/expo-model/field-attribute.html) | [GetFrom](#getfrommemberinfo)([MemberInfo]($$TODO-Reflection.MemberInfo.html)) | Gets a FieldAttribute from the given MemberInfo | the field attribute
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | [GetHashCode](https://docs.microsoft.com/en-us/dotnet/api/system.object.gethashcode)() | Serves as the default hash function.<br>(Inherited from [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | A hash code for the current object.
| [Type](https://docs.microsoft.com/en-us/dotnet/api/system.type) | [GetType](https://docs.microsoft.com/en-us/dotnet/api/system.object.gettype)() | Gets the Type of the current instance.<br>(Inherited from [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | The exact runtime type of the current instance.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | [IsDefined](https://docs.microsoft.com/en-us/dotnet/api/system.attribute.isdefined)([Assembly]($$TODO-Assembly.html), [Type](https://docs.microsoft.com/en-us/dotnet/api/system.type)) | Determines whether any custom attributes are applied to an assembly. Parameters specify the assembly, and the type of the custom attribute to search for.<br>(Inherited from [Attribute](https://docs.microsoft.com/en-us/dotnet/api/system.attribute)) | true if a custom attribute of type attributeType is applied to element; otherwise, false.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | [Match](https://docs.microsoft.com/en-us/dotnet/api/system.attribute.match)([Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | When overridden in a derived class, returns a value that indicates whether this instance equals a specified object.<br>(Inherited from [Attribute](https://docs.microsoft.com/en-us/dotnet/api/system.attribute)) | An Object to compare with this instance of Attribute.
| [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) | [MemberwiseClone](https://docs.microsoft.com/en-us/dotnet/api/system.object.memberwiseclone)() | Creates a shallow copy of the current Object.<br>(Inherited from [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | A shallow copy of the current Object.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | [ReferenceEquals](https://docs.microsoft.com/en-us/dotnet/api/system.object.referenceequals)([Object](https://docs.microsoft.com/en-us/dotnet/api/system.object), [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | Determines whether the specified Object instances are the same instance.<br>(Inherited from [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | true if objA is the same instance as objB or if both are null; otherwise, false.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | [ToString](https://docs.microsoft.com/en-us/dotnet/api/system.object.tostring)() | Returns a string that represents the current object.<br>(Inherited from [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | A string that represents the current object.

<br>
<br>

### GetFrom([MemberInfo]($$TODO-Reflection.MemberInfo.html))

Gets a FieldAttribute from the given MemberInfo

```cs
GetFrom(Reflection.MemberInfo fieldMember);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [MemberInfo]($$TODO-Reflection.MemberInfo.html) | fieldMember | Field member information 

#### Returns

[FieldAttribute](/reference/asna-qsys-expo/expo-model/field-attribute.html)

the field attribute


<br>
<br>

