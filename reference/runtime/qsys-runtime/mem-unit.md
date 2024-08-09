---
title: "MemUnit class                 | QSYS API Reference Guide"
description: "Defines methods to handle RPG MOVE semantics. "
last_modified_at: 2024-08-09T16:18:25Z
---

Defines methods to handle RPG MOVE semantics.

**Namespace:** ASNA.QSys.Runtime
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>

## Methods

| Signature | Description |
| --- | --- |
| [AdjustLeft](#string-adjustleftstring-source-bool-isnumeric-int-targetlength)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Adjust the length of a string to a given value, by padding or truncating the string on the left.
| [AdjustRight](#string-adjustrightstring-source-bool-isnumeric-int-targetlength)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Adjust the length of a string to a given value, by padding or truncating the string on the right.
| [CharToMemUnitsSigned](#string-chartomemunitssignedstring-digits)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Convert a string representing a number to a zoned numeric representation.
| [DecimalToMemUnits](#string-decimaltomemunitsdecimal-number-int-integrals-int-decimals)([Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Convert a decimal number to its zoned representation.
| [DecimalToMemUnitsSigned](#string-decimaltomemunitssigneddecimal-number-int-integrals-int-decimals)([Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Convert a decimal number to its zoned representation.
| [getCharValue](#int-getcharvaluechar-c)([Char](https://docs.microsoft.com/en-us/dotnet/api/system.char)) | Get the numeric digit encoded in a zoned char.
| [Int2ToMemUnits](#string-int2tomemunitsshort-number)([Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16)) | Convert a 2-byte integer number to a zoned numeric representation.
| [Int2ToMemUnitsSigned](#string-int2tomemunitssignedshort-number)([Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16)) | Convert a 2-byte integer number to a zoned numeric representation.
| [Int4ToMemUnits](#string-int4tomemunitsint-number)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Convert a 4-byte integer number to a zoned numeric representation.
| [Int4ToMemUnitsSigned](#string-int4tomemunitssignedint-number)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Convert a 4-byte integer number to a zoned numeric representation.
| [Int8ToMemUnits](#string-int8tomemunitslong-number)([Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64)) | Convert an 8-byte integer number to a zoned numeric representation.
| [Int8ToMemUnitsSigned](#string-int8tomemunitssignedlong-number)([Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64)) | Convert an 8-byte integer number to a zoned numeric representation.
| [MemUnitsToDecimal](#decimal-memunitstodecimalstring-digits-int-integrals-int-decimals)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Convert the zoned representation of a number to decimal.
| [MemUnitsToInt2](#short-memunitstoint2string-digits)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Convert the zoned representation of a number to a 2-byte integer number.
| [MemUnitsToInt4](#int-memunitstoint4string-digits)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Convert the zoned representation of a number to a 4-byte integer number.
| [MemUnitsToInt8](#long-memunitstoint8string-digits)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Convert the zoned representation of a number to a 8-byte integer number.
| [MergeLeft](#string-mergeleftstring-sourcevalue-string-targetvalue)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | RPG's MoveLeft. Merge the sourceValue into targetValue starting at position 0.
| [MergeRight](#string-mergerightstring-sourcevalue-string-targetvalue)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | RPG's Move(Right). Merge the sourceValue into targetValue starting at the end of targetValue.

### string AdjustLeft([string source](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [bool isNumeric](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [int targetLength](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Adjust the length of a string to a given value, by padding or truncating the string on the left.

```cs
string AdjustLeft(string source, bool isNumeric, int targetLength)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | source | The string to adjust.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | isNumeric | True to pad with '0' if necessary. False to pad with ' '.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetLength | The desired length.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The string at the desired length.

### string AdjustRight([string source](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [bool isNumeric](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [int targetLength](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Adjust the length of a string to a given value, by padding or truncating the string on the right.

```cs
string AdjustRight(string source, bool isNumeric, int targetLength)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | source | The string to adjust.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | isNumeric | True to pad with '0' if necessary. False to pad with ' '.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetLength | The desired length.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The string at the desired length.

### string CharToMemUnitsSigned([string digits](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Convert a string representing a number to a zoned numeric representation.

```cs
string CharToMemUnitsSigned(string digits)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | digits | The input string.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The string representing the number as zoned.

### string DecimalToMemUnits([decimal number](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [int integrals](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int decimals](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Convert a decimal number to its zoned representation.

```cs
string DecimalToMemUnits(decimal number, int integrals, int decimals)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | number | The number to convert.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | integrals | The number of integral digits in the decimal number.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | decimals | The number of decimal positions in the decimal number.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The string representing the number as zoned.

### string DecimalToMemUnitsSigned([decimal number](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [int integrals](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int decimals](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Convert a decimal number to its zoned representation.

```cs
string DecimalToMemUnitsSigned(decimal number, int integrals, int decimals)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | number | The number to convert.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | integrals | The number of integral digits in the decimal number.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | decimals | The number of decimal positions in the decimal number.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The string representing the number as zoned, with the zone stamped on every character if the number is negative.

### int getCharValue([char c](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/char))

Get the numeric digit encoded in a zoned char.

```cs
int getCharValue(char c)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Char](https://docs.microsoft.com/en-us/dotnet/api/system.char) | c | The zoned char encoding a digit.

#### Returns

| Type | Description
| --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | The integer value of the encoded char.

### string Int2ToMemUnits([short number](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Convert a 2-byte integer number to a zoned numeric representation.

```cs
string Int2ToMemUnits(short number)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | number | The number to convert.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The string representing the number as zoned.

### string Int2ToMemUnitsSigned([short number](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Convert a 2-byte integer number to a zoned numeric representation.

```cs
string Int2ToMemUnitsSigned(short number)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | number | The number to convert.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The string representing the number as zoned, with the zone stamped on every character if the number is negative.

### string Int4ToMemUnits([int number](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Convert a 4-byte integer number to a zoned numeric representation.

```cs
string Int4ToMemUnits(int number)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | number | The number to convert.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The string representing the number as zoned.

### string Int4ToMemUnitsSigned([int number](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Convert a 4-byte integer number to a zoned numeric representation.

```cs
string Int4ToMemUnitsSigned(int number)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | number | The number to convert.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The string representing the number as zoned, with the zone stamped on every character if the number is negative.

### string Int8ToMemUnits([long number](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Convert an 8-byte integer number to a zoned numeric representation.

```cs
string Int8ToMemUnits(long number)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | number | The number to convert.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The string representing the number as zoned.

### string Int8ToMemUnitsSigned([long number](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Convert an 8-byte integer number to a zoned numeric representation.

```cs
string Int8ToMemUnitsSigned(long number)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | number | The number to convert.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The string representing the number as zoned, with the zone stamped on every character if the number is negative.

### decimal MemUnitsToDecimal([string digits](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [int integrals](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int decimals](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Convert the zoned representation of a number to decimal.

```cs
decimal MemUnitsToDecimal(string digits, int integrals, int decimals)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | digits | The string with the zoned representaion of the number.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | integrals | The number of integral digits in the decimal number.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | decimals | The number of decimal positions in the decimal number.

#### Returns

| Type | Description
| --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | The decimal number equivalent to the zoned representation, in the proper size.

### short MemUnitsToInt2([string digits](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Convert the zoned representation of a number to a 2-byte integer number.

```cs
short MemUnitsToInt2(string digits)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | digits | The string with the zoned representaion of the number.

#### Returns

| Type | Description
| --- | ---
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | The 2-byte integer number equivalent to the zoned representation.

### int MemUnitsToInt4([string digits](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Convert the zoned representation of a number to a 4-byte integer number.

```cs
int MemUnitsToInt4(string digits)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | digits | The string with the zoned representaion of the number.

#### Returns

| Type | Description
| --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | The 4-byte integer number equivalent to the zoned representation.

### long MemUnitsToInt8([string digits](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Convert the zoned representation of a number to a 8-byte integer number.

```cs
long MemUnitsToInt8(string digits)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | digits | The string with the zoned representaion of the number.

#### Returns

| Type | Description
| --- | ---
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | The 8-byte integer number equivalent to the zoned representation.

### string MergeLeft([string sourceValue](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string targetValue](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

RPG's MoveLeft. Merge the sourceValue into targetValue starting at position 0.

```cs
string MergeLeft(string sourceValue, string targetValue)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | sourceValue | Source value.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | targetValue | Target value.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The result of the merge.

### string MergeRight([string sourceValue](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string targetValue](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

RPG's Move(Right). Merge the sourceValue into targetValue starting at the end of targetValue.

```cs
string MergeRight(string sourceValue, string targetValue)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | sourceValue | Source value.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | targetValue | Target value.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The result of the merge.
