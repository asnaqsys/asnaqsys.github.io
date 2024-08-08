---
title: "DecimalMethods class          | QSYS API Reference Guide"
description: "Contains extension methods for handling RPG operations for decimal numbers. "
last_modified_at: 2024-08-08T21:41:46Z
---

Contains extension methods for handling RPG operations for decimal numbers.

**Namespace:** ASNA.QSys.Runtime
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>

## Methods

| Signature | Description |
| --- | --- |
| [ApplyEditWord](#string-applyeditworddecimal-num-string-editwordstring)([Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | ApplyEditWord summary.
| [GetDigits](#decimal-getdigitsdecimal-num-int-digits-int-decimals-int-start)([Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Extracts digits from a decimal number.
| [GetDigits](#decimal-getdigitsdecimal-num-int-digits-int-decimals-int-start-int-length)([Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Extracts digits from a decimal number.
| [GetDigits](#decimal-getdigitsdecimal-num-int-digits-int-decimals-int-start-int-length-int-resdecimals)([Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Extracts digits from a decimal number.
| [MoveLeft](#decimal-moveleftdecimal-num-int-sourcedig-int-sourcedec-decimal-targetoperand-int-targetoperanddig-int-targetoperanddec)([Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's MOVEL. Moves left a decimal to a decimal.
| [MoveLeft](#string-moveleftdecimal-num-int-sourcedig-int-sourcedec-string-targetoperand)([Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | RPG's MOVEL. Moves left decimal to a string.
| [MoveLeft](#datetime-moveleftdecimal-num-int-sourcedig-int-sourcedec-datetime-datetime-datetimedatakind-datetimekind-datetimeformat-datetimeformat)([Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind](/reference/runtime/qsys-runtime/date-time-data-kind.html), [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html)) | RPG's MOVEL. Moves left a decimal into a DateTime.
| [MoveLeft](#short-moveleftdecimal-num-int-sourcedig-int-sourcedec-short-targetoperand)([Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16)) | RPG's MOVEL. Moves left a decimal to an int2 (short).
| [MoveLeft](#int-moveleftdecimal-num-int-sourcedig-int-sourcedec-int-targetoperand)([Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's MOVEL. Moves left a decimal to an int4 (int).
| [MoveLeft](#long-moveleftdecimal-num-int-sourcedig-int-sourcedec-long-targetoperand)([Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64)) | RPG's MOVEL. Moves left a decimal to an int8 (long).
| [MoveLeftToChar](#char-movelefttochardecimal-num-int-sourcedig-int-sourcedec)([Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's MOVEL. Moves right a decimal to a char.
| [MoveLeftWithPad](#decimal-moveleftwithpaddecimal-num-int-sourcedig-int-sourcedec-int-targetoperanddig-int-targetoperanddec)([Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's MOVEL. Moves left a decimal to a decimal with pad.
| [MoveLeftWithPad](#string-moveleftwithpaddecimal-num-int-sourcedig-int-sourcedec-string-targetoperand)([Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | RPG's MOVEL. Moves left decimal to a string, with pad.
| [MoveLeftWithPad](#datetime-moveleftwithpaddecimal-num-int-sourcedig-int-sourcedec-datetime-datetime-datetimedatakind-datetimekind-datetimeformat-datetimeformat)([Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind](/reference/runtime/qsys-runtime/date-time-data-kind.html), [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html)) | RPG's MOVEL. Moves left a decimal into a DateTime with pad.
| [MoveLeftWithPad](#short-moveleftwithpaddecimal-num-int-sourcedig-int-sourcedec-short-targetoperand)([Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16)) | RPG's MOVEL. Moves left a decimal to an int2 (short) with pad.
| [MoveLeftWithPad](#int-moveleftwithpaddecimal-num-int-sourcedig-int-sourcedec-int-targetoperand)([Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's MOVEL. Moves left a decimal to an int4 (int) with pad.
| [MoveLeftWithPad](#long-moveleftwithpaddecimal-num-int-sourcedig-int-sourcedec-long-targetoperand)([Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64)) | RPG's MOVEL. Moves left a decimal to an int8 (long) with pad.
| [MoveRight](#decimal-moverightdecimal-num-decimal-targetoperand-int-targetoperanddig-int-targetoperanddec)([Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's MOVE. Moves right a decimal to a decimal.
| [MoveRight](#string-moverightdecimal-num-int-sourcedig-int-sourcedec-string-targetoperand)([Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | RPG's MOVE. Moves right decimal to a string.
| [MoveRight](#datetime-moverightdecimal-num-int-sourcedig-int-sourcedec-datetime-datetime-datetimedatakind-datetimekind-datetimeformat-datetimeformat)([Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind](/reference/runtime/qsys-runtime/date-time-data-kind.html), [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html)) | RPG's MOVE. Moves right a decimal into a DateTime.
| [MoveRight](#short-moverightdecimal-num-int-sourcedig-int-sourcedec-short-targetoperand)([Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16)) | RPG's MOVE. Moves right a decimal to an int2 (short).
| [MoveRight](#int-moverightdecimal-num-int-sourcedig-int-sourcedec-int-targetoperand)([Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's MOVE. Moves right a decimal to an int4 (int).
| [MoveRight](#long-moverightdecimal-num-int-sourcedig-int-sourcedec-long-targetoperand)([Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64)) | RPG's MOVE. Moves right a decimal to an int8 (long).
| [MoveRightToChar](#char-moverighttochardecimal-num-int-sourcedig-int-sourcedec)([Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's MOVE. Moves right a decimal to a char.
| [MoveRightWithPad](#decimal-moverightwithpaddecimal-num-int-targetoperanddig-int-targetoperanddec)([Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's MOVE. Moves right a decimal to a decimal with pad.
| [MoveRightWithPad](#string-moverightwithpaddecimal-num-int-sourcedig-int-sourcedec-string-targetoperand)([Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | RPG's MOVE. Moves right decimal to a string, with pad.
| [MoveRightWithPad](#datetime-moverightwithpaddecimal-num-int-sourcedig-int-sourcedec-datetime-datetime-datetimedatakind-datetimekind-datetimeformat-datetimeformat)([Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind](/reference/runtime/qsys-runtime/date-time-data-kind.html), [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html)) | RPG's MOVE. Moves right a decimal into a DateTime with pad.
| [MoveRightWithPad](#short-moverightwithpaddecimal-num-int-sourcedig-int-sourcedec-short-targetoperand)([Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16)) | RPG's MOVE. Moves right a decimal to an int2 (short) with pad.
| [MoveRightWithPad](#int-moverightwithpaddecimal-num-int-sourcedig-int-sourcedec-int-targetoperand)([Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's MOVE. Moves right a decimal to an int4 (int) with pad.
| [MoveRightWithPad](#long-moverightwithpaddecimal-num-int-sourcedig-int-sourcedec-long-targetoperand)([Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64)) | RPG's MOVE. Moves right a decimal to an int8 (long) with pad.
| [RoundUp](#decimal-roundupdecimal-num-int-decimalcount)([Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Rounds up a decimal number to the desired decimal positions.
| [SetDigits](#decimal-setdigitsdecimal-num-int-digits-int-decimals-decimal-replace-int-start)([Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Replaces contiguous digits in a decimal number.
| [SetDigits](#decimal-setdigitsdecimal-num-int-digits-int-decimals-decimal-replace-int-start-int-length)([Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Replaces contiguous digits in a decimal number.
| [SetDigits](#decimal-setdigitsdecimal-num-int-digits-int-decimals-decimal-replace-int-start-int-repdigits-int-repdecimals)([Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Replaces contiguous digits in a decimal number.
| [Sum](#decimal-sumdecimal--array)([Decimal\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.decimal)) | Returns the added values of each element in the array.
| [Sum](#float-sumsingle--array)([Single\[\]](https://learn.microsoft.com/en-us/dotnet/api/system.single?view=net-8.0)) | Returns the added values of each element in the array.
| [Sum](#double-sumdouble--array)([Double\[\]](https://learn.microsoft.com/en-us/dotnet/api/system.double?view=net-8.0)) | Returns the added values of each element in the array.
| [TestTime](#bool-testtimedecimal-num-int-digits-int-decimals-datetimedatakind-kind-datetimeformat-format)([Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [DateTimeDataKind](/reference/runtime/qsys-runtime/date-time-data-kind.html), [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html)) | Tests whether a decimal number contains a valid date/time/timestamp value. 
| [ToDate](#datetime-todatedecimal-source-datetimeformat-format)([Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html)) | ToDate summary.
| [ToDecimal\<T\>](#decimal-todecimal-t-t-val)([T](https://learn.microsoft.com/en-us/dotnet/api/system.type?view=net-8.0)) | Converts a value of type T to decimal.
| [ToFixedDecimal](#decimal-tofixeddecimaldecimal-num-int-digits-int-decimals)([Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Adjusts the digits and decimal positions of a fixed decimal number.
| [ToFixedDecimal](#decimal-tofixeddecimaldecimal-num-int-decimals)([Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Truncates a decimal to the specified number of decimal positions.
| [ToFixedDecimalRounded](#decimal-tofixeddecimalroundeddecimal-num-int-digits-int-decimals)([Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Adjusts the digits and decimal positions of a fixed decimal number using Away From Zero rounding.
| [ToFixedDecimalRounded](#decimal-tofixeddecimalroundeddecimal-num-int-decimals)([Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Rounds a decimal to the specified number of decimal positions using Away From Zero rounding.
| [ToStringBinary](#string-tostringbinarydecimal-num-int-digits-int-decimals)([Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Returns as a string the 'memory' representation of a binary decimal number.
| [ToStringPacked](#string-tostringpackeddecimal-num-int-digits)([Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Returns as a string the 'memory' representation of a packed decimal number.
| [ToStringZoned](#string-tostringzoneddecimal-num-int-digits-int-decimals)([Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Returns as a string the 'memory' representation of a zoned decimal number.
| [ToTime](#datetime-totimedecimal-source-datetimeformat-format)([Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html)) | ToTime summary.
| [ToTimestamp](#datetime-totimestampdecimal-source)([Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal)) | ToTimestamp summary.

### string ApplyEditWord([decimal num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [string editwordString](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

ApplyEditWord summary.

```cs
string ApplyEditWord(decimal num, string editwordString)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | num | ApplyEditWord num param.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | editwordString | ApplyEditWord editwordString param.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | ApplyEditWord returns.

### decimal GetDigits([decimal num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [int digits](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int decimals](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int start](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Extracts digits from a decimal number.

```cs
decimal GetDigits(decimal num, int digits, int decimals, int start)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | num | The decimal number.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | digits | The number of digits the decimal number contains.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | decimals | The number of decimal positions.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | start | The 0-based starting position.

#### Returns

| Type | Description
| --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | The decimal number that contains the extracted digits.

### decimal GetDigits([decimal num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [int digits](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int decimals](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int start](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int length](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Extracts digits from a decimal number.

```cs
decimal GetDigits(decimal num, int digits, int decimals, int start, int length)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | num | The decimal number.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | digits | The number of digits the decimal number contains.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | decimals | The number of decimal positions.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | start | The 0-based starting position.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | length | The count of digits to extract.

#### Returns

| Type | Description
| --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | The decimal number that contains the extracted digits.

### decimal GetDigits([decimal num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [int digits](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int decimals](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int start](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int length](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int resDecimals](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Extracts digits from a decimal number.

```cs
decimal GetDigits(decimal num, int digits, int decimals, int start, int length, int resDecimals)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | num | The decimal number.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | digits | The number of digits the decimal number contains.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | decimals | The number of decimal positions.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | start | The 0-based starting position.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | length | The count of digits to extract.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | resDecimals | The decimal positions of the resulting decimal number.

#### Returns

| Type | Description
| --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | The decimal number that contains the extracted digits.

### decimal MoveLeft([decimal num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [int sourceDig](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int sourceDec](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [decimal targetOperand](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [int targetOperandDig](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int targetOperandDec](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVEL. Moves left a decimal to a decimal.

```cs
decimal MoveLeft(decimal num, int sourceDig, int sourceDec, decimal targetOperand, int targetOperandDig, int targetOperandDec)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | num | Decimal value of the source number.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | sourceDig | number of digits in the source.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | sourceDec | number of decimal places in the source.
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | targetOperand | Decimal value of the targetOperand number.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetOperandDig | number of digits in the targetOperand.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetOperandDec | number of decimal places in the targetOperand.

#### Returns

| Type | Description
| --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | The resulting decimal value of the operation.

### string MoveLeft([decimal num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [int sourceDig](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int sourceDec](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [string targetOperand](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

RPG's MOVEL. Moves left decimal to a string.

```cs
string MoveLeft(decimal num, int sourceDig, int sourceDec, string targetOperand)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | num | Decimal value of the source number.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | sourceDig | number of digits in the source.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | sourceDec | number of decimal places in the source.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | targetOperand | targetOperand string.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The resulting string value of the operation.

### DateTime MoveLeft([decimal num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [int sourceDig](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int sourceDec](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [DateTime dateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind dateTimeKind](/reference/runtime/qsys-runtime/date-time-data-kind.html), [DateTimeFormat dateTimeFormat](/reference/datagate/datagate-common/date-time-format.html))

RPG's MOVEL. Moves left a decimal into a DateTime.

```cs
DateTime MoveLeft(decimal num, int sourceDig, int sourceDec, DateTime dateTime, DateTimeDataKind dateTimeKind, DateTimeFormat dateTimeFormat)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | num | Decimal value of the source number.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | sourceDig | number of digits in the source.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | sourceDec | number of decimal places in the source.
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | dateTime | Date, Time, Timestamp.
| [DateTimeDataKind](/reference/runtime/qsys-runtime/date-time-data-kind.html) | dateTimeKind | DateTime Kind.
| [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html) | dateTimeFormat | DateTime Format.

#### Returns

| Type | Description
| --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | The resulting DateTime value of the operation.

### short MoveLeft([decimal num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [int sourceDig](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int sourceDec](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [short targetOperand](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVEL. Moves left a decimal to an int2 (short).

```cs
short MoveLeft(decimal num, int sourceDig, int sourceDec, short targetOperand)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | num | Decimal value of the source number.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | sourceDig | number of digits in the source.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | sourceDec | number of decimal places in the source.
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | targetOperand | short value of the targetOperand.

#### Returns

| Type | Description
| --- | ---
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | The resulting short value of the operation.

### int MoveLeft([decimal num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [int sourceDig](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int sourceDec](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int targetOperand](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVEL. Moves left a decimal to an int4 (int).

```cs
int MoveLeft(decimal num, int sourceDig, int sourceDec, int targetOperand)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | num | Decimal value of the source number.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | sourceDig | number of digits in the source.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | sourceDec | number of decimal places in the source.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetOperand | The int value target of the operation.

#### Returns

| Type | Description
| --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | The resulting int value of the operation.

### long MoveLeft([decimal num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [int sourceDig](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int sourceDec](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [long targetOperand](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVEL. Moves left a decimal to an int8 (long).

```cs
long MoveLeft(decimal num, int sourceDig, int sourceDec, long targetOperand)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | num | Decimal value of the source number.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | sourceDig | number of digits in the source.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | sourceDec | number of decimal places in the source.
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | targetOperand | The long value target of the operation.

#### Returns

| Type | Description
| --- | ---
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | The resulting long value of the operation.

### char MoveLeftToChar([decimal num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [int sourceDig](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int sourceDec](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVEL. Moves right a decimal to a char.

```cs
char MoveLeftToChar(decimal num, int sourceDig, int sourceDec)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | num | Decimal value of the source number.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | sourceDig | number of digits in the source.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | sourceDec | number of decimal places in the source.

#### Returns

| Type | Description
| --- | ---
| [Char](https://docs.microsoft.com/en-us/dotnet/api/system.char) | The first character in the string representation of the decimal value.

### decimal MoveLeftWithPad([decimal num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [int sourceDig](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int sourceDec](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int targetOperandDig](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int targetOperandDec](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVEL. Moves left a decimal to a decimal with pad.

```cs
decimal MoveLeftWithPad(decimal num, int sourceDig, int sourceDec, int targetOperandDig, int targetOperandDec)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | num | Decimal value of the source number.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | sourceDig | number of digits in the source.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | sourceDec | number of decimal places in the source.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetOperandDig | number of digits in the targetOperand.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetOperandDec | number of decimal places in the targetOperand.

#### Returns

| Type | Description
| --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | The resulting decimal value of the operation.

### string MoveLeftWithPad([decimal num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [int sourceDig](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int sourceDec](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [string targetOperand](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

RPG's MOVEL. Moves left decimal to a string, with pad.

```cs
string MoveLeftWithPad(decimal num, int sourceDig, int sourceDec, string targetOperand)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | num | Decimal value of the source number.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | sourceDig | number of digits in the source.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | sourceDec | number of decimal places in the source.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | targetOperand | targetOperand string.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The resulting string value of the operation.

### DateTime MoveLeftWithPad([decimal num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [int sourceDig](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int sourceDec](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [DateTime dateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind dateTimeKind](/reference/runtime/qsys-runtime/date-time-data-kind.html), [DateTimeFormat dateTimeFormat](/reference/datagate/datagate-common/date-time-format.html))

RPG's MOVEL. Moves left a decimal into a DateTime with pad.

```cs
DateTime MoveLeftWithPad(decimal num, int sourceDig, int sourceDec, DateTime dateTime, DateTimeDataKind dateTimeKind, DateTimeFormat dateTimeFormat)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | num | Decimal value of the source number.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | sourceDig | number of digits in the source.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | sourceDec | number of decimal places in the source.
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | dateTime | Date, Time, Timestamp.
| [DateTimeDataKind](/reference/runtime/qsys-runtime/date-time-data-kind.html) | dateTimeKind | DateTime Kind.
| [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html) | dateTimeFormat | DateTime Format.

#### Returns

| Type | Description
| --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | The resulting DateTime value of the operation.

### short MoveLeftWithPad([decimal num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [int sourceDig](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int sourceDec](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [short targetOperand](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVEL. Moves left a decimal to an int2 (short) with pad.

```cs
short MoveLeftWithPad(decimal num, int sourceDig, int sourceDec, short targetOperand)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | num | Decimal value of the source number.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | sourceDig | number of digits in the source.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | sourceDec | number of decimal places in the source.
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | targetOperand | short value of the targetOperand.

#### Returns

| Type | Description
| --- | ---
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | The resulting short value of the operation.

### int MoveLeftWithPad([decimal num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [int sourceDig](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int sourceDec](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int targetOperand](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVEL. Moves left a decimal to an int4 (int) with pad.

```cs
int MoveLeftWithPad(decimal num, int sourceDig, int sourceDec, int targetOperand)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | num | Decimal value of the source number.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | sourceDig | number of digits in the source.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | sourceDec | number of decimal places in the source.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetOperand | The int value target of the operation.

#### Returns

| Type | Description
| --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | The resulting int value of the operation.

### long MoveLeftWithPad([decimal num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [int sourceDig](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int sourceDec](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [long targetOperand](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVEL. Moves left a decimal to an int8 (long) with pad.

```cs
long MoveLeftWithPad(decimal num, int sourceDig, int sourceDec, long targetOperand)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | num | Decimal value of the source number.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | sourceDig | number of digits in the source.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | sourceDec | number of decimal places in the source.
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | targetOperand | The long value target of the operation.

#### Returns

| Type | Description
| --- | ---
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | The resulting long value of the operation.

### decimal MoveRight([decimal num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [decimal targetOperand](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [int targetOperandDig](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int targetOperandDec](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVE. Moves right a decimal to a decimal.

```cs
decimal MoveRight(decimal num, decimal targetOperand, int targetOperandDig, int targetOperandDec)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | num | Decimal value of the source number.
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | targetOperand | Decimal value of the targetOperand number.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetOperandDig | number of digits in the targetOperand.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetOperandDec | number of decimal places in the targetOperand.

#### Returns

| Type | Description
| --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | The resulting decimal value of the operation.

### string MoveRight([decimal num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [int sourceDig](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int sourceDec](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [string targetOperand](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

RPG's MOVE. Moves right decimal to a string.

```cs
string MoveRight(decimal num, int sourceDig, int sourceDec, string targetOperand)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | num | Decimal value of the source number.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | sourceDig | number of digits in the source.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | sourceDec | number of decimal places in the source.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | targetOperand | targetOperand string.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The resulting string value of the operation.

### DateTime MoveRight([decimal num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [int sourceDig](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int sourceDec](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [DateTime dateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind dateTimeKind](/reference/runtime/qsys-runtime/date-time-data-kind.html), [DateTimeFormat dateTimeFormat](/reference/datagate/datagate-common/date-time-format.html))

RPG's MOVE. Moves right a decimal into a DateTime.

```cs
DateTime MoveRight(decimal num, int sourceDig, int sourceDec, DateTime dateTime, DateTimeDataKind dateTimeKind, DateTimeFormat dateTimeFormat)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | num | Decimal value of the source number.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | sourceDig | number of digits in the source.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | sourceDec | number of decimal places in the source.
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | dateTime | Date, Time, Timestamp.
| [DateTimeDataKind](/reference/runtime/qsys-runtime/date-time-data-kind.html) | dateTimeKind | DateTime Kind.
| [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html) | dateTimeFormat | DateTime Format.

#### Returns

| Type | Description
| --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | The resulting DateTime value of the operation.

### short MoveRight([decimal num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [int sourceDig](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int sourceDec](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [short targetOperand](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVE. Moves right a decimal to an int2 (short).

```cs
short MoveRight(decimal num, int sourceDig, int sourceDec, short targetOperand)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | num | Decimal value of the source number.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | sourceDig | number of digits in the source.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | sourceDec | number of decimal places in the source.
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | targetOperand | short value of the targetOperand.

#### Returns

| Type | Description
| --- | ---
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | The resulting short value of the operation.

### int MoveRight([decimal num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [int sourceDig](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int sourceDec](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int targetOperand](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVE. Moves right a decimal to an int4 (int).

```cs
int MoveRight(decimal num, int sourceDig, int sourceDec, int targetOperand)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | num | Decimal value of the source number.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | sourceDig | number of digits in the source.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | sourceDec | number of decimal places in the source.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetOperand | The int value target of the operation.

#### Returns

| Type | Description
| --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | The resulting int value of the operation.

### long MoveRight([decimal num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [int sourceDig](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int sourceDec](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [long targetOperand](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVE. Moves right a decimal to an int8 (long).

```cs
long MoveRight(decimal num, int sourceDig, int sourceDec, long targetOperand)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | num | Decimal value of the source number.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | sourceDig | number of digits in the source.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | sourceDec | number of decimal places in the source.
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | targetOperand | The long value target of the operation.

#### Returns

| Type | Description
| --- | ---
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | The resulting long value of the operation.

### char MoveRightToChar([decimal num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [int sourceDig](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int sourceDec](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVE. Moves right a decimal to a char.

```cs
char MoveRightToChar(decimal num, int sourceDig, int sourceDec)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | num | Decimal value of the source number.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | sourceDig | number of digits in the source.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | sourceDec | number of decimal places in the source.

#### Returns

| Type | Description
| --- | ---
| [Char](https://docs.microsoft.com/en-us/dotnet/api/system.char) | The last character in the string representation of the decimal value.

### decimal MoveRightWithPad([decimal num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [int targetOperandDig](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int targetOperandDec](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVE. Moves right a decimal to a decimal with pad.

```cs
decimal MoveRightWithPad(decimal num, int targetOperandDig, int targetOperandDec)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | num | Decimal value of the source number.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetOperandDig | number of digits in the targetOperand.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetOperandDec | number of decimal places in the targetOperand.

#### Returns

| Type | Description
| --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | The resulting decimal value of the operation.

### string MoveRightWithPad([decimal num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [int sourceDig](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int sourceDec](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [string targetOperand](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

RPG's MOVE. Moves right decimal to a string, with pad.

```cs
string MoveRightWithPad(decimal num, int sourceDig, int sourceDec, string targetOperand)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | num | Decimal value of the source number.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | sourceDig | number of digits in the source.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | sourceDec | number of decimal places in the source.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | targetOperand | targetOperand string.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The resulting string value of the operation.

### DateTime MoveRightWithPad([decimal num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [int sourceDig](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int sourceDec](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [DateTime dateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind dateTimeKind](/reference/runtime/qsys-runtime/date-time-data-kind.html), [DateTimeFormat dateTimeFormat](/reference/datagate/datagate-common/date-time-format.html))

RPG's MOVE. Moves right a decimal into a DateTime with pad.

```cs
DateTime MoveRightWithPad(decimal num, int sourceDig, int sourceDec, DateTime dateTime, DateTimeDataKind dateTimeKind, DateTimeFormat dateTimeFormat)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | num | Decimal value of the source number.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | sourceDig | number of digits in the source.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | sourceDec | number of decimal places in the source.
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | dateTime | Date, Time, Timestamp.
| [DateTimeDataKind](/reference/runtime/qsys-runtime/date-time-data-kind.html) | dateTimeKind | DateTime Kind.
| [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html) | dateTimeFormat | DateTime Format.

#### Returns

| Type | Description
| --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | The resulting DateTime value of the operation.

### short MoveRightWithPad([decimal num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [int sourceDig](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int sourceDec](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [short targetOperand](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVE. Moves right a decimal to an int2 (short) with pad.

```cs
short MoveRightWithPad(decimal num, int sourceDig, int sourceDec, short targetOperand)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | num | Decimal value of the source number.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | sourceDig | number of digits in the source.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | sourceDec | number of decimal places in the source.
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | targetOperand | short value of the targetOperand.

#### Returns

| Type | Description
| --- | ---
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | The resulting short value of the operation.

### int MoveRightWithPad([decimal num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [int sourceDig](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int sourceDec](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int targetOperand](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVE. Moves right a decimal to an int4 (int) with pad.

```cs
int MoveRightWithPad(decimal num, int sourceDig, int sourceDec, int targetOperand)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | num | Decimal value of the source number.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | sourceDig | number of digits in the source.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | sourceDec | number of decimal places in the source.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetOperand | The int value target of the operation.

#### Returns

| Type | Description
| --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | The resulting int value of the operation.

### long MoveRightWithPad([decimal num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [int sourceDig](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int sourceDec](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [long targetOperand](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVE. Moves right a decimal to an int8 (long) with pad.

```cs
long MoveRightWithPad(decimal num, int sourceDig, int sourceDec, long targetOperand)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | num | Decimal value of the source number.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | sourceDig | number of digits in the source.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | sourceDec | number of decimal places in the source.
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | targetOperand | The long value target of the operation.

#### Returns

| Type | Description
| --- | ---
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | The resulting long value of the operation.

### decimal RoundUp([decimal num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [int decimalCount](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Rounds up a decimal number to the desired decimal positions.

```cs
decimal RoundUp(decimal num, int decimalCount)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | num | The number to round up.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | decimalCount | The desired number of decimal positions.

#### Returns

| Type | Description
| --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | The decimal value rounded up to the given decimal positions.

### decimal SetDigits([decimal num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [int digits](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int decimals](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [decimal replace](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [int start](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Replaces contiguous digits in a decimal number.

```cs
decimal SetDigits(decimal num, int digits, int decimals, decimal replace, int start)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | num | The number that will have its digits replaced.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | digits | The length of num.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | decimals | The decimal positions of num.
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | replace | The number that will replace the digits of num.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | start | The 0-based position in num where the replacement will start.

#### Returns

| Type | Description
| --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | The decimal number after replacing digits.

### decimal SetDigits([decimal num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [int digits](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int decimals](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [decimal replace](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [int start](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int length](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Replaces contiguous digits in a decimal number.

```cs
decimal SetDigits(decimal num, int digits, int decimals, decimal replace, int start, int length)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | num | The number that will have its digits replaced.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | digits | The length of num.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | decimals | The decimal positions of num.
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | replace | The number that will replace the digits of num.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | start | The 0-based position in num where the replacement will start.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | length | The length (digits) of the replacement.

#### Returns

| Type | Description
| --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | The decimal number after replacing digits.

### decimal SetDigits([decimal num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [int digits](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int decimals](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [decimal replace](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [int start](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int repDigits](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int repDecimals](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Replaces contiguous digits in a decimal number.

```cs
decimal SetDigits(decimal num, int digits, int decimals, decimal replace, int start, int repDigits, int repDecimals)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | num | The number that will have its digits replaced.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | digits | The length of num.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | decimals | The decimal positions of num.
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | replace | The number that will replace the digits of num.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | start | The 0-based position in num where the replacement will start.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | repDigits | The length (digits) of the replacement.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | repDecimals | The decimal positions of the replacement.

#### Returns

| Type | Description
| --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | The decimal number after replacing digits.

### decimal Sum([Decimal\[\] array](https://docs.microsoft.com/en-us/dotnet/api/system.decimal))

Returns the added values of each element in the array.

```cs
decimal Sum(Decimal[] array)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Decimal\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | array | The array whose elements will be summed.

#### Returns

| Type | Description
| --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | The added value of every element in the array.

### float Sum([Single\[\] array](https://learn.microsoft.com/en-us/dotnet/api/system.single?view=net-8.0))

Returns the added values of each element in the array.

```cs
float Sum(Single[] array)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Single\[\]](https://learn.microsoft.com/en-us/dotnet/api/system.single?view=net-8.0) | array | The array whose elements will be summed.

#### Returns

| Type | Description
| --- | ---
| [Single](https://learn.microsoft.com/en-us/dotnet/api/system.single?view=net-8.0) | The added value of every element in the array.

### double Sum([Double\[\] array](https://learn.microsoft.com/en-us/dotnet/api/system.double?view=net-8.0))

Returns the added values of each element in the array.

```cs
double Sum(Double[] array)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Double\[\]](https://learn.microsoft.com/en-us/dotnet/api/system.double?view=net-8.0) | array | The array whose elements will be summed.

#### Returns

| Type | Description
| --- | ---
| [Double](https://learn.microsoft.com/en-us/dotnet/api/system.double?view=net-8.0) | The added value of every element in the array.

### bool TestTime([decimal num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [int digits](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int decimals](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [DateTimeDataKind kind](/reference/runtime/qsys-runtime/date-time-data-kind.html), [DateTimeFormat format](/reference/datagate/datagate-common/date-time-format.html))

Tests whether a decimal number contains a valid date/time/timestamp value. 

```cs
bool TestTime(decimal num, int digits, int decimals, DateTimeDataKind kind, DateTimeFormat format)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | num | The decimal number to test.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | digits | The length of the decimal number.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | decimals | The decimal positions of the decimal number.
| [DateTimeDataKind](/reference/runtime/qsys-runtime/date-time-data-kind.html) | kind | whether the number represents a date, time, or timestamp.
| [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html) | format | The date/time/timestamp format in which the number is.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | True if the number represents a valid date/time/timestamp value in the given format. False otherwise.

### DateTime ToDate([decimal source](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [DateTimeFormat format](/reference/datagate/datagate-common/date-time-format.html))

ToDate summary.

```cs
DateTime ToDate(decimal source, DateTimeFormat format)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | source | ToDate source param.
| [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html) | format | ToDate format param.

#### Returns

| Type | Description
| --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | ToDate returns.

### decimal ToDecimal\<T\>([T val](https://learn.microsoft.com/en-us/dotnet/api/system.type?view=net-8.0))

Converts a value of type T to decimal.

```cs
decimal ToDecimal<T>(T val)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [T](https://learn.microsoft.com/en-us/dotnet/api/system.type?view=net-8.0) | val |  The value to convert.

#### Returns

| Type | Description
| --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | The decimal result of the conversion.

### decimal ToFixedDecimal([decimal num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [int digits](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int decimals](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Adjusts the digits and decimal positions of a fixed decimal number.

```cs
decimal ToFixedDecimal(decimal num, int digits, int decimals)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | num |  The decimal number to truncate.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | digits | The desired number of digits.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | decimals | The desired number of decimal positions.

#### Returns

| Type | Description
| --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | The decimal number adjusted to the given digits and decimal positions.

### decimal ToFixedDecimal([decimal num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [int decimals](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Truncates a decimal to the specified number of decimal positions.

```cs
decimal ToFixedDecimal(decimal num, int decimals)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | num | The decimal number to truncate.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | decimals | The desired number of decimal positions.

#### Returns

| Type | Description
| --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | The decimal number adjusted to the given decimal positions.

### decimal ToFixedDecimalRounded([decimal num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [int digits](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int decimals](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Adjusts the digits and decimal positions of a fixed decimal number using Away From Zero rounding.

```cs
decimal ToFixedDecimalRounded(decimal num, int digits, int decimals)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | num |  The decimal number to round up.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | digits | The desired number of digits.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | decimals | The desired number of decimal positions.

#### Returns

| Type | Description
| --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | The decimal number adjusted to the given digits and decimal positions with rounding.

### decimal ToFixedDecimalRounded([decimal num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [int decimals](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Rounds a decimal to the specified number of decimal positions using Away From Zero rounding.

```cs
decimal ToFixedDecimalRounded(decimal num, int decimals)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | num | The decimal number to round up.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | decimals | The desired number of decimal positions.

#### Returns

| Type | Description
| --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | The decimal number adjusted to the given decimal positions with rounding.

### string ToStringBinary([decimal num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [int digits](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int decimals](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Returns as a string the 'memory' representation of a binary decimal number.

```cs
string ToStringBinary(decimal num, int digits, int decimals)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | num | The decimal number to convert.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | digits | The total number of digits the decimal has.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | decimals | The number of decimal positions in the decimal number.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The resulting binary decimal representation of the decimal number.

### string ToStringPacked([decimal num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [int digits](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Returns as a string the 'memory' representation of a packed decimal number.

```cs
string ToStringPacked(decimal num, int digits)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | num | The decimal number to convert.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | digits | The total number of digits the decimal has.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The resulting packed decimal representation of the decimal number.

### string ToStringZoned([decimal num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [int digits](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int decimals](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Returns as a string the 'memory' representation of a zoned decimal number.

```cs
string ToStringZoned(decimal num, int digits, int decimals)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | num | The decimal number to convert.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | digits | The total number of digits the decimal has.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | decimals | The number of decimal positions in the decimal number.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The resulting zoned decimal representation of the decimal number.

### DateTime ToTime([decimal source](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [DateTimeFormat format](/reference/datagate/datagate-common/date-time-format.html))

ToTime summary.

```cs
DateTime ToTime(decimal source, DateTimeFormat format)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | source | ToTime source param.
| [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html) | format | ToTime format param.

#### Returns

| Type | Description
| --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | ToTime returns.

### DateTime ToTimestamp([decimal source](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types))

ToTimestamp summary.

```cs
DateTime ToTimestamp(decimal source)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | source | ToTimestamp source param.

#### Returns

| Type | Description
| --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | ToTimestamp returns.
