---
title: "FixedDecimalMethods class     | QSYS API Reference Guide"
description: "Contains extension methods for handling RPG operations for FixedDecimal values. "
last_modified_at: 2024-08-09T17:25:29Z
---

Contains extension methods for handling RPG operations for FixedDecimal values.

**Namespace:** ASNA.QSys.Runtime
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>

## Methods

| Signature | Description |
| --- | --- |
| [ApplyEditWord\<TDigits, TDecimals\>](#string-applyeditword-tdigits-tdecimals-fixeddecimal-tdigits-tdecimals-num-string-editwordstring)([FixedDecimal\<TDigits, TDecimals\>](/reference/runtime/qsys-runtime/fixed-decimal-2.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Applies an edit word to a FixedDecimal number.
| [MoveLeftToChar\<TDigits, TDecimals\>](#char-movelefttochar-tdigits-tdecimals-fixeddecimal-tdigits-tdecimals-source)([FixedDecimal\<TDigits, TDecimals\>](/reference/runtime/qsys-runtime/fixed-decimal-2.html)) | RPG's MOVEL. Moves left a decimal to a char.
| [MoveRightToChar\<TDigits, TDecimals\>](#char-moverighttochar-tdigits-tdecimals-fixeddecimal-tdigits-tdecimals-source)([FixedDecimal\<TDigits, TDecimals\>](/reference/runtime/qsys-runtime/fixed-decimal-2.html)) | RPG's MOVE. Moves right a decimal to a char.
| [RoundUp\<TDigits, TDecimals\>](#decimal-roundup-tdigits-tdecimals-fixeddecimal-tdigits-tdecimals-num-int-decimalcount)([FixedDecimal\<TDigits, TDecimals\>](/reference/runtime/qsys-runtime/fixed-decimal-2.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Rounds up a decimal number to the desired decimal positions.
| [SetHiLoEq\<TDigits, TDecimals\>](#decimal-sethiloeq-tdigits-tdecimals-fixeddecimal-tdigits-tdecimals-source-indicator-hi-indicator-lo-indicator-eq)([FixedDecimal\<TDigits, TDecimals\>](/reference/runtime/qsys-runtime/fixed-decimal-2.html), [Indicator&](/reference/runtime/qsys-runtime/indicator.html), [Indicator&](/reference/runtime/qsys-runtime/indicator.html), [Indicator&](/reference/runtime/qsys-runtime/indicator.html)) | Sets the HI, LO, and EQ flags passed in, based on the value of source.
| [TestTime\<TDigits, TDecimals\>](#bool-testtime-tdigits-tdecimals-fixeddecimal-tdigits-tdecimals-source-datetimedatakind-kind-datetimeformat-format)([FixedDecimal\<TDigits, TDecimals\>](/reference/runtime/qsys-runtime/fixed-decimal-2.html), [DateTimeDataKind](/reference/runtime/qsys-runtime/date-time-data-kind.html), [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html)) | Tests whether a decimal number contains a valid date/time/timestamp value. 
| [ToDate\<TDigits, TDecimals\>](#datetime-todate-tdigits-tdecimals-fixeddecimal-tdigits-tdecimals-source-datetimeformat-format)([FixedDecimal\<TDigits, TDecimals\>](/reference/runtime/qsys-runtime/fixed-decimal-2.html), [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html)) | Converts a fixed decimal number to a date in the specified format.
| [ToStringBinary\<TDigits, TDecimals\>](#string-tostringbinary-tdigits-tdecimals-fixeddecimal-tdigits-tdecimals-source)([FixedDecimal\<TDigits, TDecimals\>](/reference/runtime/qsys-runtime/fixed-decimal-2.html)) | Returns as a string the 'memory' representation of a binary decimal number.
| [ToStringPacked\<TDigits, TDecimals\>](#string-tostringpacked-tdigits-tdecimals-fixeddecimal-tdigits-tdecimals-source)([FixedDecimal\<TDigits, TDecimals\>](/reference/runtime/qsys-runtime/fixed-decimal-2.html)) | Returns as a string the 'memory' representation of a packed decimal number.
| [ToStringZoned\<TDigits, TDecimals\>](#string-tostringzoned-tdigits-tdecimals-fixeddecimal-tdigits-tdecimals-source)([FixedDecimal\<TDigits, TDecimals\>](/reference/runtime/qsys-runtime/fixed-decimal-2.html)) | Returns as a string the 'memory' representation of a zoned decimal number.
| [ToTime\<TDigits, TDecimals\>](#datetime-totime-tdigits-tdecimals-fixeddecimal-tdigits-tdecimals-source-datetimeformat-format)([FixedDecimal\<TDigits, TDecimals\>](/reference/runtime/qsys-runtime/fixed-decimal-2.html), [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html)) | Converts a fixed decimal number to a time in the specified format.
| [ToTimestamp\<TDigits, TDecimals\>](#datetime-totimestamp-tdigits-tdecimals-fixeddecimal-tdigits-tdecimals-source)([FixedDecimal\<TDigits, TDecimals\>](/reference/runtime/qsys-runtime/fixed-decimal-2.html)) | Converts a fixed decimal number to a timestamp.

### string ApplyEditWord\<TDigits, TDecimals\>([FixedDecimal\<TDigits, TDecimals\> num](/reference/runtime/qsys-runtime/fixed-decimal-2.html), [string editwordString](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Applies an edit word to a FixedDecimal number.

```cs
string ApplyEditWord<TDigits, TDecimals>(FixedDecimal<TDigits, TDecimals> num, string editwordString)
```

### char MoveLeftToChar\<TDigits, TDecimals\>([FixedDecimal\<TDigits, TDecimals\> source](/reference/runtime/qsys-runtime/fixed-decimal-2.html))

RPG's MOVEL. Moves left a decimal to a char.

```cs
char MoveLeftToChar<TDigits, TDecimals>(FixedDecimal<TDigits, TDecimals> source)
```

### char MoveRightToChar\<TDigits, TDecimals\>([FixedDecimal\<TDigits, TDecimals\> source](/reference/runtime/qsys-runtime/fixed-decimal-2.html))

RPG's MOVE. Moves right a decimal to a char.

```cs
char MoveRightToChar<TDigits, TDecimals>(FixedDecimal<TDigits, TDecimals> source)
```

### decimal RoundUp\<TDigits, TDecimals\>([FixedDecimal\<TDigits, TDecimals\> num](/reference/runtime/qsys-runtime/fixed-decimal-2.html), [int decimalCount](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Rounds up a decimal number to the desired decimal positions.

```cs
decimal RoundUp<TDigits, TDecimals>(FixedDecimal<TDigits, TDecimals> num, int decimalCount)
```

### decimal SetHiLoEq\<TDigits, TDecimals\>([FixedDecimal\<TDigits, TDecimals\> source](/reference/runtime/qsys-runtime/fixed-decimal-2.html), [Indicator& hi](/reference/runtime/qsys-runtime/indicator.html), [Indicator& lo](/reference/runtime/qsys-runtime/indicator.html), [Indicator& eq](/reference/runtime/qsys-runtime/indicator.html))

Sets the HI, LO, and EQ flags passed in, based on the value of source.

```cs
decimal SetHiLoEq<TDigits, TDecimals>(FixedDecimal<TDigits, TDecimals> source, Indicator& hi, Indicator& lo, Indicator& eq)
```

### bool TestTime\<TDigits, TDecimals\>([FixedDecimal\<TDigits, TDecimals\> source](/reference/runtime/qsys-runtime/fixed-decimal-2.html), [DateTimeDataKind kind](/reference/runtime/qsys-runtime/date-time-data-kind.html), [DateTimeFormat format](/reference/datagate/datagate-common/date-time-format.html))

Tests whether a decimal number contains a valid date/time/timestamp value. 

```cs
bool TestTime<TDigits, TDecimals>(FixedDecimal<TDigits, TDecimals> source, DateTimeDataKind kind, DateTimeFormat format)
```

### DateTime ToDate\<TDigits, TDecimals\>([FixedDecimal\<TDigits, TDecimals\> source](/reference/runtime/qsys-runtime/fixed-decimal-2.html), [DateTimeFormat format](/reference/datagate/datagate-common/date-time-format.html))

Converts a fixed decimal number to a date in the specified format.

```cs
DateTime ToDate<TDigits, TDecimals>(FixedDecimal<TDigits, TDecimals> source, DateTimeFormat format)
```

### string ToStringBinary\<TDigits, TDecimals\>([FixedDecimal\<TDigits, TDecimals\> source](/reference/runtime/qsys-runtime/fixed-decimal-2.html))

Returns as a string the 'memory' representation of a binary decimal number.

```cs
string ToStringBinary<TDigits, TDecimals>(FixedDecimal<TDigits, TDecimals> source)
```

### string ToStringPacked\<TDigits, TDecimals\>([FixedDecimal\<TDigits, TDecimals\> source](/reference/runtime/qsys-runtime/fixed-decimal-2.html))

Returns as a string the 'memory' representation of a packed decimal number.

```cs
string ToStringPacked<TDigits, TDecimals>(FixedDecimal<TDigits, TDecimals> source)
```

### string ToStringZoned\<TDigits, TDecimals\>([FixedDecimal\<TDigits, TDecimals\> source](/reference/runtime/qsys-runtime/fixed-decimal-2.html))

Returns as a string the 'memory' representation of a zoned decimal number.

```cs
string ToStringZoned<TDigits, TDecimals>(FixedDecimal<TDigits, TDecimals> source)
```

### DateTime ToTime\<TDigits, TDecimals\>([FixedDecimal\<TDigits, TDecimals\> source](/reference/runtime/qsys-runtime/fixed-decimal-2.html), [DateTimeFormat format](/reference/datagate/datagate-common/date-time-format.html))

Converts a fixed decimal number to a time in the specified format.

```cs
DateTime ToTime<TDigits, TDecimals>(FixedDecimal<TDigits, TDecimals> source, DateTimeFormat format)
```

### DateTime ToTimestamp\<TDigits, TDecimals\>([FixedDecimal\<TDigits, TDecimals\> source](/reference/runtime/qsys-runtime/fixed-decimal-2.html))

Converts a fixed decimal number to a timestamp.

```cs
DateTime ToTimestamp<TDigits, TDecimals>(FixedDecimal<TDigits, TDecimals> source)
```
