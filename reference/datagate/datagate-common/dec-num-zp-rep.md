---
title: "DecNumZPRep class"
description: "DecNumZPRep provides methods for interpreting the Acceler8DB &quot;ZPREP&quot; code for packed and zoned decimal data representation, thereby describi"
last_modified_at: 2024-08-09T17:25:07Z
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
| [DecNumZPRep](dec-num-zp-rep-ctor.html#decnumzprep-int32)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Initializes a new instance of the  class.

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
| [IsNegativePacked](dec-num-zp-rep-isnegativepacked.html#bool-isnegativepacked-byte-b)([Byte](https://docs.microsoft.com/en-us/dotnet/api/system.byte)) | Returns true if the specified byte represents a negative packeddecimal byte.
| [IsNegativeZone](dec-num-zp-rep-isnegativezone.html#bool-isnegativezone-byte-b)([Byte](https://docs.microsoft.com/en-us/dotnet/api/system.byte)) | Returns true if the specified byte represents a negative zoneddecimal byte.
| [IsPositivePacked](dec-num-zp-rep-ispositivepacked.html#bool-ispositivepacked-byte-b)([Byte](https://docs.microsoft.com/en-us/dotnet/api/system.byte)) | Returns true if the specified byte represents a positive packeddecimal byte.
| [IsPositiveZone](dec-num-zp-rep-ispositivezone.html#bool-ispositivezone-byte-b)([Byte](https://docs.microsoft.com/en-us/dotnet/api/system.byte)) | Returns true if the specified byte represents a positive zoneddecimal byte.

