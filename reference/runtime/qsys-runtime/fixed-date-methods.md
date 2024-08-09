---
title: "FixedDateMethods class        | QSYS API Reference Guide"
description: "Contains extension methods for handling RPG operations for FixedDate values. "
last_modified_at: 2024-08-09T17:25:29Z
---

Contains extension methods for handling RPG operations for FixedDate values.

**Namespace:** ASNA.QSys.Runtime
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>

## Methods

| Signature | Description |
| --- | --- |
| [AddDuration\<TFormat, TSeparator\>](#datetime-addduration-tformat-tseparator-fixeddate-tformat-tseparator-datetime-double-duration-durationcode-durationcode)([FixedDate\<TFormat, TSeparator\>](/reference/runtime/qsys-runtime/fixed-date-2.html), [Double](https://learn.microsoft.com/en-us/dotnet/api/system.double?view=net-8.0), [DurationCode](/reference/runtime/qsys-runtime/duration-code.html)) | Adds a duration span to a date or a timestamp value.
| [AddDurationToTime\<TFormat, TSeparator\>](#datetime-adddurationtotime-tformat-tseparator-fixeddate-tformat-tseparator-datetime-double-duration-durationcode-durationcode)([FixedDate\<TFormat, TSeparator\>](/reference/runtime/qsys-runtime/fixed-date-2.html), [Double](https://learn.microsoft.com/en-us/dotnet/api/system.double?view=net-8.0), [DurationCode](/reference/runtime/qsys-runtime/duration-code.html)) | Adds a duration span to a time value.
| [MoveLeftToChar\<TFormat, TSeparator\>](#char-movelefttochar-tformat-tseparator-fixeddate-tformat-tseparator-fixeddate)([FixedDate\<TFormat, TSeparator\>](/reference/runtime/qsys-runtime/fixed-date-2.html)) | RPG's MOVEL. Moves left a date, time, timestamp in the given format to a char value.
| [MoveRightToChar\<TFormat, TSeparator\>](#char-moverighttochar-tformat-tseparator-fixeddate-tformat-tseparator-fixeddate)([FixedDate\<TFormat, TSeparator\>](/reference/runtime/qsys-runtime/fixed-date-2.html)) | RPG's MOVE. Moves right a date in the given format to a char value.
| [NormalizeYear\<TFormat, TSeparator\>](#datetime-normalizeyear-tformat-tseparator-fixeddate-tformat-tseparator-fixeddate)([FixedDate\<TFormat, TSeparator\>](/reference/runtime/qsys-runtime/fixed-date-2.html)) | Turns a 4 digit year into a 2 digit year between 1940 and 2039
| [SubtractDuration\<TFormat, TSeparator\>](#datetime-subtractduration-tformat-tseparator-fixeddate-tformat-tseparator-datetime-double-duration-durationcode-durationcode)([FixedDate\<TFormat, TSeparator\>](/reference/runtime/qsys-runtime/fixed-date-2.html), [Double](https://learn.microsoft.com/en-us/dotnet/api/system.double?view=net-8.0), [DurationCode](/reference/runtime/qsys-runtime/duration-code.html)) | Subtracts a duration span from a date or a timestamp value.
| [SubtractDurationFromTime\<TFormat, TSeparator\>](#datetime-subtractdurationfromtime-tformat-tseparator-fixeddate-tformat-tseparator-datetime-double-duration-durationcode-durationcode)([FixedDate\<TFormat, TSeparator\>](/reference/runtime/qsys-runtime/fixed-date-2.html), [Double](https://learn.microsoft.com/en-us/dotnet/api/system.double?view=net-8.0), [DurationCode](/reference/runtime/qsys-runtime/duration-code.html)) | Subtracts a duration span from a time value.
| [TimestampToDate\<TFormat, TSeparator\>](#datetime-timestamptodate-tformat-tseparator-fixeddate-tformat-tseparator-fixeddate)([FixedDate\<TFormat, TSeparator\>](/reference/runtime/qsys-runtime/fixed-date-2.html)) | Returns the Date portion of a timestamp.
| [ToDouble\<TFormat, TSeparator\>](#double-todouble-tformat-tseparator-fixeddate-tformat-tseparator-fixeddate-bool-throwonoverflow)([FixedDate\<TFormat, TSeparator\>](/reference/runtime/qsys-runtime/fixed-date-2.html), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Converts a fixed date value to double.
| [ToFixedDecimal\<TFormat, TSeparator\>](#decimal-tofixeddecimal-tformat-tseparator-fixeddate-tformat-tseparator-fixeddate-int-digits-int-decimals)([FixedDate\<TFormat, TSeparator\>](/reference/runtime/qsys-runtime/fixed-date-2.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Converts a fixed date value to a decimal.
| [ToFloat\<TFormat, TSeparator\>](#float-tofloat-tformat-tseparator-fixeddate-tformat-tseparator-fixeddate-bool-throwonoverflow)([FixedDate\<TFormat, TSeparator\>](/reference/runtime/qsys-runtime/fixed-date-2.html), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Converts a fixed date value to float.
| [ToInt16\<TFormat, TSeparator\>](#short-toint16-tformat-tseparator-fixeddate-tformat-tseparator-fixeddate-bool-throwonoverflow)([FixedDate\<TFormat, TSeparator\>](/reference/runtime/qsys-runtime/fixed-date-2.html), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Converts a fixed date value to int 16.
| [ToInt32\<TFormat, TSeparator\>](#int-toint32-tformat-tseparator-fixeddate-tformat-tseparator-fixeddate-bool-throwonoverflow)([FixedDate\<TFormat, TSeparator\>](/reference/runtime/qsys-runtime/fixed-date-2.html), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Converts a fixed date value to int 32.
| [ToInt64\<TFormat, TSeparator\>](#long-toint64-tformat-tseparator-fixeddate-tformat-tseparator-fixeddate-bool-throwonoverflow)([FixedDate\<TFormat, TSeparator\>](/reference/runtime/qsys-runtime/fixed-date-2.html), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Converts a fixed date value to int 64.

### DateTime AddDuration\<TFormat, TSeparator\>([FixedDate\<TFormat, TSeparator\> dateTime](/reference/runtime/qsys-runtime/fixed-date-2.html), [double duration](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [DurationCode durationCode](/reference/runtime/qsys-runtime/duration-code.html))

Adds a duration span to a date or a timestamp value.

```cs
DateTime AddDuration<TFormat, TSeparator>(FixedDate<TFormat, TSeparator> dateTime, double duration, DurationCode durationCode)
```

### DateTime AddDurationToTime\<TFormat, TSeparator\>([FixedDate\<TFormat, TSeparator\> dateTime](/reference/runtime/qsys-runtime/fixed-date-2.html), [double duration](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [DurationCode durationCode](/reference/runtime/qsys-runtime/duration-code.html))

Adds a duration span to a time value.

```cs
DateTime AddDurationToTime<TFormat, TSeparator>(FixedDate<TFormat, TSeparator> dateTime, double duration, DurationCode durationCode)
```

### char MoveLeftToChar\<TFormat, TSeparator\>([FixedDate\<TFormat, TSeparator\> fixedDate](/reference/runtime/qsys-runtime/fixed-date-2.html))

RPG's MOVEL. Moves left a date, time, timestamp in the given format to a char value.

```cs
char MoveLeftToChar<TFormat, TSeparator>(FixedDate<TFormat, TSeparator> fixedDate)
```

### char MoveRightToChar\<TFormat, TSeparator\>([FixedDate\<TFormat, TSeparator\> fixedDate](/reference/runtime/qsys-runtime/fixed-date-2.html))

RPG's MOVE. Moves right a date in the given format to a char value.

```cs
char MoveRightToChar<TFormat, TSeparator>(FixedDate<TFormat, TSeparator> fixedDate)
```

### DateTime NormalizeYear\<TFormat, TSeparator\>([FixedDate\<TFormat, TSeparator\> fixedDate](/reference/runtime/qsys-runtime/fixed-date-2.html))

Turns a 4 digit year into a 2 digit year between 1940 and 2039

```cs
DateTime NormalizeYear<TFormat, TSeparator>(FixedDate<TFormat, TSeparator> fixedDate)
```

### DateTime SubtractDuration\<TFormat, TSeparator\>([FixedDate\<TFormat, TSeparator\> dateTime](/reference/runtime/qsys-runtime/fixed-date-2.html), [double duration](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [DurationCode durationCode](/reference/runtime/qsys-runtime/duration-code.html))

Subtracts a duration span from a date or a timestamp value.

```cs
DateTime SubtractDuration<TFormat, TSeparator>(FixedDate<TFormat, TSeparator> dateTime, double duration, DurationCode durationCode)
```

### DateTime SubtractDurationFromTime\<TFormat, TSeparator\>([FixedDate\<TFormat, TSeparator\> dateTime](/reference/runtime/qsys-runtime/fixed-date-2.html), [double duration](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [DurationCode durationCode](/reference/runtime/qsys-runtime/duration-code.html))

Subtracts a duration span from a time value.

```cs
DateTime SubtractDurationFromTime<TFormat, TSeparator>(FixedDate<TFormat, TSeparator> dateTime, double duration, DurationCode durationCode)
```

### DateTime TimestampToDate\<TFormat, TSeparator\>([FixedDate\<TFormat, TSeparator\> fixedDate](/reference/runtime/qsys-runtime/fixed-date-2.html))

Returns the Date portion of a timestamp.

```cs
DateTime TimestampToDate<TFormat, TSeparator>(FixedDate<TFormat, TSeparator> fixedDate)
```

### double ToDouble\<TFormat, TSeparator\>([FixedDate\<TFormat, TSeparator\> fixedDate](/reference/runtime/qsys-runtime/fixed-date-2.html), [bool throwOnOverflow](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Converts a fixed date value to double.

```cs
double ToDouble<TFormat, TSeparator>(FixedDate<TFormat, TSeparator> fixedDate, bool throwOnOverflow)
```

### decimal ToFixedDecimal\<TFormat, TSeparator\>([FixedDate\<TFormat, TSeparator\> fixedDate](/reference/runtime/qsys-runtime/fixed-date-2.html), [int digits](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int decimals](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Converts a fixed date value to a decimal.

```cs
decimal ToFixedDecimal<TFormat, TSeparator>(FixedDate<TFormat, TSeparator> fixedDate, int digits, int decimals)
```

### float ToFloat\<TFormat, TSeparator\>([FixedDate\<TFormat, TSeparator\> fixedDate](/reference/runtime/qsys-runtime/fixed-date-2.html), [bool throwOnOverflow](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Converts a fixed date value to float.

```cs
float ToFloat<TFormat, TSeparator>(FixedDate<TFormat, TSeparator> fixedDate, bool throwOnOverflow)
```

### short ToInt16\<TFormat, TSeparator\>([FixedDate\<TFormat, TSeparator\> fixedDate](/reference/runtime/qsys-runtime/fixed-date-2.html), [bool throwOnOverflow](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Converts a fixed date value to int 16.

```cs
short ToInt16<TFormat, TSeparator>(FixedDate<TFormat, TSeparator> fixedDate, bool throwOnOverflow)
```

### int ToInt32\<TFormat, TSeparator\>([FixedDate\<TFormat, TSeparator\> fixedDate](/reference/runtime/qsys-runtime/fixed-date-2.html), [bool throwOnOverflow](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Converts a fixed date value to int 32.

```cs
int ToInt32<TFormat, TSeparator>(FixedDate<TFormat, TSeparator> fixedDate, bool throwOnOverflow)
```

### long ToInt64\<TFormat, TSeparator\>([FixedDate\<TFormat, TSeparator\> fixedDate](/reference/runtime/qsys-runtime/fixed-date-2.html), [bool throwOnOverflow](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Converts a fixed date value to int 64.

```cs
long ToInt64<TFormat, TSeparator>(FixedDate<TFormat, TSeparator> fixedDate, bool throwOnOverflow)
```
