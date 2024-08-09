---
title: "ByteAttribute class           | QSYS API Reference Guide"
description: "Provides Byte Attributes (for Properties) "
last_modified_at: 2024-08-09T17:26:04Z
---

Provides Byte Attributes (for Properties)

**Namespace:** ASNA.QSys.Expo.Model
**Assembly:** ASNA.QSys.Expo.Model.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [Attribute](https://docs.microsoft.com/en-us/dotnet/api/system.attribute) --> [FieldAttribute](/reference/expo/qsys-expo-model/field-attribute.html)
<br>
<br>

## Remarks

Model Fields are declared as Record Properties. To annotate the [Fixed Type](https://asnaqsys.github.io/concepts/program-structure/qsys-fixedtypes.html) as `Byte`, Model properties can use this attribute.

For example,

```cs
[Byte()]
public byte MY_BYTE_FIELD { get; set; }
```
Declares a read/write field of [Fixed Type](https://asnaqsys.github.io/concepts/program-structure/qsys-fixedtypes.html) `Byte` named `MY_BYTE_FIELD` on a particular Model Record.

Note that there is no need to indicate the field length, one is the only possible length.


## Constructors

| Name | Description |
| --- | --- |
| [ByteAttribute()](#byteattribute) | Initializes a new ByteAttribute instance

### ByteAttribute()

Initializes a new ByteAttribute instance

```cs
ByteAttribute()
```

## Methods

| Signature | Description |
| --- | --- |
| [GetFrom](#byteattribute-getfrommemberinfo-fieldmember)([MemberInfo](https://learn.microsoft.com/en-us/dotnet/api/system.reflection.memberinfo?view=net-8.0)) | Gets a ByteAttribute from a field member

### ByteAttribute GetFrom([MemberInfo fieldMember](https://learn.microsoft.com/en-us/dotnet/api/system.reflection.memberinfo?view=net-8.0))

Gets a ByteAttribute from a field member

```cs
ByteAttribute GetFrom(MemberInfo fieldMember)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [MemberInfo](https://learn.microsoft.com/en-us/dotnet/api/system.reflection.memberinfo?view=net-8.0) | fieldMember | field member information

#### Returns

| Type | Description
| --- | ---
| [ByteAttribute](/reference/expo/qsys-expo-model/byte-attribute.html) | the byte attribute
