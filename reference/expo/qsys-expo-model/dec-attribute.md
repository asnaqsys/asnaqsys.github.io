---
title: "DecAttribute class            | QSYS API Reference Guide"
description: "Provides Decimal Attributes (for Properties) "
last_modified_at: 2024-08-09T16:18:58Z
---

Provides Decimal Attributes (for Properties)

**Namespace:** ASNA.QSys.Expo.Model
**Assembly:** ASNA.QSys.Expo.Model.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [Attribute](https://docs.microsoft.com/en-us/dotnet/api/system.attribute) --> [FieldAttribute](/reference/expo/qsys-expo-model/field-attribute.html)
<br>
<br>

## Remarks

Model Fields are declared as Record Properties. To annotate the [Fixed Type](/concepts/program-structure/qsys-fixedtypes.html) as `Dec`, Model properties can use this attribute.

For example,

```cs
[Dec(9, 0)]
public decimal SORDNUM { get; private set; } // ORDER NUMBER
```

Declares a read-only field of [Decimal Fixed Type](/concepts/program-structure/qsys-fixedtypes.html) `Dec`, with length nine and zero decimal positions, named `SORDNUM` on a particular Model Record.


## Constructors

| Name | Description |
| --- | --- |
| [DecAttribute](#decattributeint32-int32)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Initializes a new DecAttribute instance

### DecAttribute([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

Initializes a new DecAttribute instance

```cs
DecAttribute(Int32, Int32)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | length | Field length
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | decimals | number of decimals (defaults to zero)

## Properties

| Type | Name | Description
| --- | --- | --- 
| [ModulusValidation](/reference/expo/qsys-expo-model/modulus-validation.html) | CheckModulus | Modulus validation algorithm  |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | CompareAllowZeros | Allow all-blank(or zero) input to satisfy validity checking for an input-capable field when any associated validity check fails. Legacy DDS CHECK(AB) |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | Decimals | Decimal positions |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | Digits | Max Digits |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | Equal | Exact value |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | GraterThan | Lower exclusive bound |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | LessThan | Upper exclusive bound |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | Max | Maximum acceptable value |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | Min | Minimum acceptable value |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | NotEqual | Excluded value |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | ReturnCursorLocationCol | Indicating if this field will be set on input operations to the Column number of the field where the cursor was positioned. |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | ReturnCursorLocationRow | Indicating if this field will be set on input operations to the Row number of the field where the cursor was positioned. |

## Methods

| Signature | Description |
| --- | --- |
| [GetFrom](#decattribute-getfrommemberinfo-fieldmember)([MemberInfo](https://learn.microsoft.com/en-us/dotnet/api/system.reflection.memberinfo?view=net-8.0)) | Gets a DecAttribute from a field member

### DecAttribute GetFrom([MemberInfo fieldMember](https://learn.microsoft.com/en-us/dotnet/api/system.reflection.memberinfo?view=net-8.0))

Gets a DecAttribute from a field member

```cs
DecAttribute GetFrom(MemberInfo fieldMember)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [MemberInfo](https://learn.microsoft.com/en-us/dotnet/api/system.reflection.memberinfo?view=net-8.0) | fieldMember | field member information

#### Returns

| Type | Description
| --- | ---
| [DecAttribute](/reference/expo/qsys-expo-model/dec-attribute.html) | the dec attribute
