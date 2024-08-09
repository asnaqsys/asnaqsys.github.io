---
title: "ValuesAttribute class         | QSYS API Reference Guide"
description: "Defines ValuesAttribute class "
last_modified_at: 2024-08-09T16:18:58Z
---

Defines ValuesAttribute class

**Namespace:** ASNA.QSys.Expo.Model
**Assembly:** ASNA.QSys.Expo.Model.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [Attribute](https://docs.microsoft.com/en-us/dotnet/api/system.attribute) --> [ValidationAttribute](https://learn.microsoft.com/en-us/dotnet/api/system.componentmodel.dataannotations.validationattribute?view=net-8.0)
<br>
<br>

## Remarks

The `ValuesAttribute` class is a specialized class derived from [ValidationAttribute](https://docs.microsoft.com/en-us/dotnet/api/system.componentmodel.dataannotations.validationattribute) that provides meta-data to express [VALUES](https://www.ibm.com/docs/en/i/7.4?topic=80-values-values-keyword-display-files) field-level keyword.

The following excerpt of code describes the Subfile field `SFSEL`, with the possible input values: 2, 3, 5, 7, 9, 10 and 11

```cs
public class SFL1_Model : SubfileRecordModel
{
    [Values(typeof(Decimal),"00","02","03","05","07","09","10","11")]
    [Dec(2, 0)]
    public decimal SFSEL { get; set; }
    .
    .
    .
}
```

This corresponds to the legacy DDS:

```
0007.00     A          R SFL1                      SFL
   .
   .
   .
0010.00     A            SFSEL          2Y 0B  8  4VALUES(0 2 3 5 7 9 10 11)
```

>Notes: 

1. The `Values` attribute requires indication of the type of value it should be used during validation. In this case `Decimal`.
2. The list of possible Values is indicated using string format. Each value will be converted to the indicated type before validation logic runs.
3. The first value added during Migration corresponds to the *Blanks* value (which is the value that represents **no input** to this field). For *character* fields a white space is used, for decimal fields the zero (as a string) is used.


## Constructors

| Name | Description |
| --- | --- |
| [ValuesAttribute](#valuesattributestring)([String\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Initializes a new instance of the class ValuesAttribute with the initial valid values provided
| [ValuesAttribute](#valuesattributeint32)([Int32\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Initializes a new instance of the class ValuesAttribute with the initial valid values provided
| [ValuesAttribute](#valuesattributetype-object)([Type](https://docs.microsoft.com/en-us/dotnet/api/system.type), [Object\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | Initializes a new instance of the class ValuesAttribute with the initial type and valid object values provided

### ValuesAttribute([String\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Initializes a new instance of the class ValuesAttribute with the initial valid values provided

```cs
ValuesAttribute(String[])
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.string) | validValues | initial values string array

### ValuesAttribute([Int32\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

Initializes a new instance of the class ValuesAttribute with the initial valid values provided

```cs
ValuesAttribute(Int32[])
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | validValues | initial values integer array

### ValuesAttribute([Type](https://docs.microsoft.com/en-us/dotnet/api/system.type), [Object\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.object))

Initializes a new instance of the class ValuesAttribute with the initial type and valid object values provided

```cs
ValuesAttribute(Type, Object[])
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Type](https://docs.microsoft.com/en-us/dotnet/api/system.type) | type | type of valid values
| [Object\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.object) | validValues | valid values object array

## Properties

| Type | Name | Description
| --- | --- | --- 
| [Type](https://docs.microsoft.com/en-us/dotnet/api/system.type) | ObjectType | Gets the Object Type |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | TrimStringValue | Gets or sets a boolean value indicating if the value in the string needs te trimmed |
| [Object\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.object) | ValidValues | Gets the array of valid values |

## Methods

| Signature | Description |
| --- | --- |
| [FormatErrorMessage](#string-formaterrormessagestring-name)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Applies formatting to an error message, based on the data field where the error occurred.
| [GetFrom](#valuesattribute-getfrommemberinfo-member)([MemberInfo](https://learn.microsoft.com/en-us/dotnet/api/system.reflection.memberinfo?view=net-8.0)) | Gets a ValuesAttribute from the MemberInfo instance provided as input (from object's custom attributes)
| [IsValid](#bool-isvalidobject-value)([Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | Gets a boolean valid indicating that the passed in value is valid

### string FormatErrorMessage([string name](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Applies formatting to an error message, based on the data field where the error occurred.

```cs
string FormatErrorMessage(string name)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | name | The field name to include in the formatted message.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | 

### ValuesAttribute GetFrom([MemberInfo member](https://learn.microsoft.com/en-us/dotnet/api/system.reflection.memberinfo?view=net-8.0))

Gets a ValuesAttribute from the MemberInfo instance provided as input (from object's custom attributes)

```cs
ValuesAttribute GetFrom(MemberInfo member)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [MemberInfo](https://learn.microsoft.com/en-us/dotnet/api/system.reflection.memberinfo?view=net-8.0) | member | member information

#### Returns

| Type | Description
| --- | ---
| [ValuesAttribute](/reference/expo/qsys-expo-model/values-attribute.html) | the ValuesAttribute

### bool IsValid([object value](https://docs.microsoft.com/en-us/dotnet/api/system.object))

Gets a boolean valid indicating that the passed in value is valid

```cs
bool IsValid(object value)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) | value | input value

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | true if valid
