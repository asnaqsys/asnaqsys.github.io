---
title: "DecNumZPRep class             | QSYS API Reference Guide"
description: "DecNumZPRep provides methods for interpreting the Acceler8DB &quot;ZPREP&quot; code for packed and zoned decimal data representation, thereby describi"
last_modified_at: 2024-08-08T21:41:32Z
---

DecNumZPRep provides methods for interpreting the Acceler8DB "ZPREP"
code for packed and zoned decimal data representation, thereby
describing the format of these data representations.

**Namespace:** ASNA.DataGate.Common
**Assembly:** ASNA.QSys.DataGate.Client.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [DecNumZPRep](#decnumzprepint32)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Initializes a new instance of the  class.

### DecNumZPRep([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

Initializes a new instance of the  class.

```cs
DecNumZPRep(Int32)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | format | The format of the decimal number.

## Properties

| Type | Name | Description
| --- | --- | --- 
| [DecNumZPRep](/reference/datagate/datagate-common/dec-num-zp-rep.html) | Default | The default zoned/packed decimal representation object forDG/Windows. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | NegPacked | Returns the 8-bit code for a packed decimal negative number.  Thecode is contained in the lower nibble, and the upper nibble iszero. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | NegZone | Returns the 8-bit code for a zoned decimal negative number.  Thecode is contained in the upper nibble, and the lower nibble iszero. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | PosPacked | Returns the 8-bit code for a packed decimal positive number.  Thecode is contained in the lower nibble, and the upper nibble iszero. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | PosZone | Returns the 8-bit code for a zoned decimal positive number.  Thecode is contained in the upper nibble, and the lower nibble iszero. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | Value | Gets the format of the decimal number. |

## Methods

| Signature | Description |
| --- | --- |
| [IsNegativePacked](#bool-isnegativepackedbyte-b)([Byte](https://docs.microsoft.com/en-us/dotnet/api/system.byte)) | Returns true if the specified byte represents a negative packeddecimal byte.
| [IsNegativeZone](#bool-isnegativezonebyte-b)([Byte](https://docs.microsoft.com/en-us/dotnet/api/system.byte)) | Returns true if the specified byte represents a negative zoneddecimal byte.
| [IsPositivePacked](#bool-ispositivepackedbyte-b)([Byte](https://docs.microsoft.com/en-us/dotnet/api/system.byte)) | Returns true if the specified byte represents a positive packeddecimal byte.
| [IsPositiveZone](#bool-ispositivezonebyte-b)([Byte](https://docs.microsoft.com/en-us/dotnet/api/system.byte)) | Returns true if the specified byte represents a positive zoneddecimal byte.

### bool IsNegativePacked([byte b](https://docs.microsoft.com/en-us/dotnet/api/system.byte))

Returns true if the specified byte represents a negative packeddecimal byte.

```cs
bool IsNegativePacked(byte b)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Byte](https://docs.microsoft.com/en-us/dotnet/api/system.byte) | b | The byte to check.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | 

### bool IsNegativeZone([byte b](https://docs.microsoft.com/en-us/dotnet/api/system.byte))

Returns true if the specified byte represents a negative zoneddecimal byte.

```cs
bool IsNegativeZone(byte b)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Byte](https://docs.microsoft.com/en-us/dotnet/api/system.byte) | b | The byte to check.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | 

### bool IsPositivePacked([byte b](https://docs.microsoft.com/en-us/dotnet/api/system.byte))

Returns true if the specified byte represents a positive packeddecimal byte.

```cs
bool IsPositivePacked(byte b)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Byte](https://docs.microsoft.com/en-us/dotnet/api/system.byte) | b | The byte to check.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | 

### bool IsPositiveZone([byte b](https://docs.microsoft.com/en-us/dotnet/api/system.byte))

Returns true if the specified byte represents a positive zoneddecimal byte.

```cs
bool IsPositiveZone(byte b)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Byte](https://docs.microsoft.com/en-us/dotnet/api/system.byte) | b | The byte to check.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | 
