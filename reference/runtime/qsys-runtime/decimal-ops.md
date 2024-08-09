---
title: "DecimalOps class              | QSYS API Reference Guide"
description: "Provide fixed length decimal storage and operations. "
last_modified_at: 2024-08-09T16:18:25Z
---

Provide fixed length decimal storage and operations.

**Namespace:** ASNA.QSys.Runtime
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>

## Methods

| Signature | Description |
| --- | --- |
| [ConvertToString](#string-converttostringdecimal-number-int-integrals-int-decimals-bool-zeropad)([Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Formats a numeric value by fixing the number of digits and decimals and converts to string.
| [DecimalToMemUnits](#string-decimaltomemunitsdecimal-number-int-integrals-int-decimals)([Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Convert a decimal of the given size to its memory layout representation.
| [DecimalToMemUnitsSigned](#string-decimaltomemunitssigneddecimal-number-int-integrals-int-decimals)([Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Convert a decimal of the given size to its memory layout representation, encoding the sign in each of the digits.
| [Divide](#decimal-dividedecimal-f1-decimal-f2-decimal-globalremainder-int-resultdecimals-bool-isroundup-bool-checkoverflow)([Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Decimal&](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Executes a DIVIDE operation.
| [FixDecimal](#decimal-fixdecimaldecimal-number-int-digits-int-decimals-bool-checkoverflow)([Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Formats a numeric value by fixing the number of digits and decimals.
| [FixDecimalH](#decimal-fixdecimalhdecimal-number-int-digits-int-decimals-bool-checkoverflow)([Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Formats a numeric value by fixing the number of digits and decimals using half adjust.
| [FixI4](#decimal-fixi4int-digits-int-decimals-int-number-bool-checkoverflow)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Formats a numeric value by fixing the number of digits and decimals.
| [GetIndicators](#void-getindicatorsdecimal-number-boolean-hiindicator-boolean-loindicator-boolean-eqindicator)([Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Boolean&](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [Boolean&](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [Boolean&](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Gets the HI-LO-EQ indicator conditions.
| [MakeHiVal](#decimal-makehivalint-length-int-decimals)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Makes a decimal HI-VALUE.
| [MapFromPacked](#string-mapfrompackeddecimal-number-int-digits)([Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Converts Packed format number to a string.
| [MapToPacked](#decimal-maptopackedstring-basestring-int-decimalcount)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Converts number in a string to a Packed format numeric value.
| [MemUnitsToDecimal](#decimal-memunitstodecimalstring-digits-int-integrals-int-decimals)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Converts a string representing a the number as a memory digits to the numeric value.
| [RoundUp](#decimal-roundupdecimal-newvalue-int-integralcount-int-decimalcount-bool-checkoverflow)([Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Rounds-up a decimal value.
| [RoundUpDecimals](#decimal-roundupdecimalsdecimal-newvalue-int-decimalcount)([Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Round-up a decimal value.
| [Trim](#decimal-trimdecimal-newvalue-int-integralcount-int-decimalcount-vxadjust-adjustparm-bool-checkoverflow)([Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [vxAdjust](/reference/runtime/qsys-runtime/vx-adjust.html), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Trims a decimal value.
| [Truncate](#decimal-truncatedecimal-newvalue-int-integralcount-int-decimalcount-bool-checkoverflow)([Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Truncates a decimal value.
| [TruncateDecimals](#decimal-truncatedecimalsdecimal-newvalue-int-decimalcount)([Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Truncates a decimal value.

### string ConvertToString([decimal number](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [int integrals](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int decimals](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [bool zeroPad](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Formats a numeric value by fixing the number of digits and decimals and converts to string.

```cs
string ConvertToString(decimal number, int integrals, int decimals, bool zeroPad)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | number | Input value.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | integrals | Number of digits.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | decimals | Number of decimals.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | zeroPad | True if padding with zeros is to be performed; False otherwise.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | Fixed-length numeric result as string.

### string DecimalToMemUnits([decimal number](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [int integrals](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int decimals](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Convert a decimal of the given size to its memory layout representation.

```cs
string DecimalToMemUnits(decimal number, int integrals, int decimals)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | number | Input number.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | integrals | Number of digits.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | decimals | Number of decimal positions/

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The string memory representation.

### string DecimalToMemUnitsSigned([decimal number](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [int integrals](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int decimals](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Convert a decimal of the given size to its memory layout representation, encoding the sign in each of the digits.

```cs
string DecimalToMemUnitsSigned(decimal number, int integrals, int decimals)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | number | Input number.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | integrals | Number of digits.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | decimals | Number of decimal positions/

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The string memory representation.

### decimal Divide([decimal f1](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [decimal f2](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [Decimal& globalRemainder](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [int resultDecimals](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [bool isRoundUp](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [bool checkOverflow](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Executes a DIVIDE operation.

```cs
decimal Divide(decimal f1, decimal f2, Decimal& globalRemainder, int resultDecimals, bool isRoundUp, bool checkOverflow)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | f1 | Input factor one.
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | f2 | Input factor two.
| [Decimal&](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | globalRemainder | Output reminder.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | resultDecimals | Input result decimals.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | isRoundUp | True if rounding is to be performed in the result; False otherwise.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | checkOverflow | True if overflow condition is to be checked; False otherwise.

#### Returns

| Type | Description
| --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | The result of the decimal division with the requested resulting decimal positions, truncated or rounded.

### decimal FixDecimal([decimal number](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [int digits](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int decimals](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [bool checkOverflow](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Formats a numeric value by fixing the number of digits and decimals.

```cs
decimal FixDecimal(decimal number, int digits, int decimals, bool checkOverflow)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | number | Input value.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | digits | Number of digits.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | decimals | Number of decimals.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | checkOverflow | True if overflow is to be checked; False otherwise.

#### Returns

| Type | Description
| --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | Fixed-length numeric result.

### decimal FixDecimalH([decimal number](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [int digits](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int decimals](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [bool checkOverflow](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Formats a numeric value by fixing the number of digits and decimals using half adjust.

```cs
decimal FixDecimalH(decimal number, int digits, int decimals, bool checkOverflow)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | number | Input value.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | digits | Number of digits.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | decimals | Number of decimals.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | checkOverflow | True if overflow is to be checked; False otherwise.

#### Returns

| Type | Description
| --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | Fixed-length numeric result.

### decimal FixI4([int digits](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int decimals](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int number](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [bool checkOverflow](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Formats a numeric value by fixing the number of digits and decimals.

```cs
decimal FixI4(int digits, int decimals, int number, bool checkOverflow)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | digits | Number of digits.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | decimals | Number of decimals.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | number | Input value.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | checkOverflow | True if overflow is to be checked; False otherwise.

#### Returns

| Type | Description
| --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | Fixed-length numeric result.

### void GetIndicators([decimal number](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [Boolean& HiIndicator](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [Boolean& LoIndicator](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [Boolean& EqIndicator](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Gets the HI-LO-EQ indicator conditions.

```cs
void GetIndicators(decimal number, Boolean& HiIndicator, Boolean& LoIndicator, Boolean& EqIndicator)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | number | Input number.
| [Boolean&](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | HiIndicator | Output HI indicator.
| [Boolean&](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | LoIndicator | Output LO indicator.
| [Boolean&](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | EqIndicator | Output EQ indicator.

### decimal MakeHiVal([int length](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int decimals](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Makes a decimal HI-VALUE.

```cs
decimal MakeHiVal(int length, int decimals)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | length | Input Length.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | decimals | Input number of decimals.

#### Returns

| Type | Description
| --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | The highest decimal value that fits in the given length and decimal positions.

### string MapFromPacked([decimal number](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [int digits](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Converts Packed format number to a string.

```cs
string MapFromPacked(decimal number, int digits)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | number | Input number.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | digits | Number of digits.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The packed number converted to a string.

### decimal MapToPacked([string baseString](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [int decimalCount](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Converts number in a string to a Packed format numeric value.

```cs
decimal MapToPacked(string baseString, int decimalCount)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | baseString | Input string.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | decimalCount | Number of decimals.

#### Returns

| Type | Description
| --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | The converted packed decimal.

### decimal MemUnitsToDecimal([string digits](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [int integrals](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int decimals](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Converts a string representing a the number as a memory digits to the numeric value.

```cs
decimal MemUnitsToDecimal(string digits, int integrals, int decimals)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | digits | Input string.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | integrals | Number of digits.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | decimals | Number of decimals.

#### Returns

| Type | Description
| --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | The fixed-decimal conversion.

### decimal RoundUp([decimal newValue](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [int integralCount](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int decimalCount](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [bool checkOverflow](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Rounds-up a decimal value.

```cs
decimal RoundUp(decimal newValue, int integralCount, int decimalCount, bool checkOverflow)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | newValue | Input value.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | integralCount | Integral count.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | decimalCount | Decimal count.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | checkOverflow | True if overflow condition is to be checked; False otherwise.

#### Returns

| Type | Description
| --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | The rounded-up result.

### decimal RoundUpDecimals([decimal newValue](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [int decimalCount](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Round-up a decimal value.

```cs
decimal RoundUpDecimals(decimal newValue, int decimalCount)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | newValue | Input value.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | decimalCount | Decimal count.

#### Returns

| Type | Description
| --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | The rounded-up result.

### decimal Trim([decimal newValue](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [int integralCount](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int decimalCount](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [vxAdjust AdjustParm](/reference/runtime/qsys-runtime/vx-adjust.html), [bool checkOverflow](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Trims a decimal value.

```cs
decimal Trim(decimal newValue, int integralCount, int decimalCount, vxAdjust AdjustParm, bool checkOverflow)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | newValue | Input value.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | integralCount | Integral count.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | decimalCount | Decimal count.
| [vxAdjust](/reference/runtime/qsys-runtime/vx-adjust.html) | AdjustParm | How to half-adjust.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | checkOverflow | True if overflow condition is to be checked; False otherwise.

#### Returns

| Type | Description
| --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | The trimmed result.

### decimal Truncate([decimal newValue](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [int integralCount](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int decimalCount](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [bool checkOverflow](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Truncates a decimal value.

```cs
decimal Truncate(decimal newValue, int integralCount, int decimalCount, bool checkOverflow)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | newValue | Input value.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | integralCount | Integral count.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | decimalCount | Decimal count.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | checkOverflow | True if overflow condition is to be checked; False otherwise.

#### Returns

| Type | Description
| --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | The truncated result.

### decimal TruncateDecimals([decimal newValue](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [int decimalCount](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Truncates a decimal value.

```cs
decimal TruncateDecimals(decimal newValue, int decimalCount)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | newValue | Input value.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | decimalCount | Decimal count.

#### Returns

| Type | Description
| --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | The truncated result.
