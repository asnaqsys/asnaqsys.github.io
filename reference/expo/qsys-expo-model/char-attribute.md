---
title: "CharAttribute class           | QSYS API Reference Guide"
description: "Provides Char Attributes (for Properties) "
last_modified_at: 2024-08-08T21:42:10Z
---

Provides Char Attributes (for Properties)

**Namespace:** ASNA.QSys.Expo.Model
**Assembly:** ASNA.QSys.Expo.Model.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [Attribute](https://docs.microsoft.com/en-us/dotnet/api/system.attribute) --> [FieldAttribute](/reference/expo/qsys-expo-model/field-attribute.html)
<br>
<br>

## Remarks

Model Fields are declared as Record Properties. To annotate the [Fixed Type](https://asnaqsys.github.io/concepts/program-structure/qsys-fixedtypes.html) as `Char`, Model properties can use this attribute.

For example,

```cs
[Char(25)]
public string SFCSZ { get; private set; } // CITY-STATE-ZIP
```

Declares a read-only field of [Fixed Type](https://asnaqsys.github.io/concepts/program-structure/qsys-fixedtypes.html) `Char`, with length of 25 chars, named `SFCSZ` on a particular Model Record.


## Constructors

| Name | Description |
| --- | --- |
| [CharAttribute](#charattributeint32)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Char attribute constructor.

### CharAttribute([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

Char attribute constructor.

```cs
CharAttribute(Int32)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | length | field length

## Properties

| Type | Name | Description
| --- | --- | --- 
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | CompareAllowBlanks | Allow all-blank input to satisfy validity checking when any associated validity check fails. Legacy DDS CHECK(AB) |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | Equal | Exact value |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | GraterThan | Lower exclusive bound |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | InputOnlyValue | Input-only attribute |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | Length | Length attribute |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | LessThan | Upper exclusive bound |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | Max | Maximum acceptable value |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | Min | Minimum acceptable value |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | NotEqual | Excluded value |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | Upper | Gets a sets a value indicating if character input will be converted to uppercase or will be left alone to preserving the letter casing typed. Defaults to true. |

## Methods

| Signature | Description |
| --- | --- |
| [GetFrom](#charattribute-getfrommemberinfo-fieldmember)([MemberInfo](https://learn.microsoft.com/en-us/dotnet/api/system.reflection.memberinfo?view=net-8.0)) | Gets a CharAttribute from a field member

### CharAttribute GetFrom([MemberInfo fieldMember](https://learn.microsoft.com/en-us/dotnet/api/system.reflection.memberinfo?view=net-8.0))

Gets a CharAttribute from a field member

```cs
CharAttribute GetFrom(MemberInfo fieldMember)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [MemberInfo](https://learn.microsoft.com/en-us/dotnet/api/system.reflection.memberinfo?view=net-8.0) | fieldMember | field member information

#### Returns

| Type | Description
| --- | ---
| [CharAttribute](/reference/expo/qsys-expo-model/char-attribute.html) | the char attribute
