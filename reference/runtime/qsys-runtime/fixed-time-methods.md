---
title: "FixedTimeMethods class        | QSYS API Reference Guide"
description: "Contains extension methods for handling RPG operations for FixedTime values. "
last_modified_at: 2024-08-09T17:25:29Z
---

Contains extension methods for handling RPG operations for FixedTime values.

**Namespace:** ASNA.QSys.Runtime
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>

## Methods

| Signature | Description |
| --- | --- |
| [AddDuration\<TFormat, TSeparator\>](#datetime-addduration-tformat-tseparator-fixedtime-tformat-tseparator-time-double-duration-durationcode-durationcode)([FixedTime\<TFormat, TSeparator\>](/reference/runtime/qsys-runtime/fixed-time-2.html), [Double](https://learn.microsoft.com/en-us/dotnet/api/system.double?view=net-8.0), [DurationCode](/reference/runtime/qsys-runtime/duration-code.html)) | Adds a duration span to a FixedTime value.
| [AddDurationToTime\<TFormat, TSeparator\>](#datetime-adddurationtotime-tformat-tseparator-fixedtime-tformat-tseparator-time-double-duration-durationcode-durationcode)([FixedTime\<TFormat, TSeparator\>](/reference/runtime/qsys-runtime/fixed-time-2.html), [Double](https://learn.microsoft.com/en-us/dotnet/api/system.double?view=net-8.0), [DurationCode](/reference/runtime/qsys-runtime/duration-code.html)) | Adds a duration span to a FixedTime value.
| [MoveLeftToChar\<TFormat, TSeparator\>](#char-movelefttochar-tformat-tseparator-fixedtime-tformat-tseparator-time)([FixedTime\<TFormat, TSeparator\>](/reference/runtime/qsys-runtime/fixed-time-2.html)) | RPG's MOVEL. Moves left a FixedTime in the given format to a char value.
| [MoveRightToChar\<TFormat, TSeparator\>](#char-moverighttochar-tformat-tseparator-fixedtime-tformat-tseparator-time)([FixedTime\<TFormat, TSeparator\>](/reference/runtime/qsys-runtime/fixed-time-2.html)) | RPG's MOVE. Moves right a FixedTime in the given format to a char value.
| [SubtractDuration\<TFormat, TSeparator\>](#datetime-subtractduration-tformat-tseparator-fixedtime-tformat-tseparator-time-double-duration-durationcode-durationcode)([FixedTime\<TFormat, TSeparator\>](/reference/runtime/qsys-runtime/fixed-time-2.html), [Double](https://learn.microsoft.com/en-us/dotnet/api/system.double?view=net-8.0), [DurationCode](/reference/runtime/qsys-runtime/duration-code.html)) | Subtracts a duration span from a FixedTime or a timestamp value.
| [SubtractDurationFromTime\<TFormat, TSeparator\>](#datetime-subtractdurationfromtime-tformat-tseparator-fixedtime-tformat-tseparator-time-double-duration-durationcode-durationcode)([FixedTime\<TFormat, TSeparator\>](/reference/runtime/qsys-runtime/fixed-time-2.html), [Double](https://learn.microsoft.com/en-us/dotnet/api/system.double?view=net-8.0), [DurationCode](/reference/runtime/qsys-runtime/duration-code.html)) | Subtracts a duration span from a FixedTime value.
| [ToDouble\<TFormat, TSeparator\>](#double-todouble-tformat-tseparator-fixedtime-tformat-tseparator-time-bool-throwonoverflow)([FixedTime\<TFormat, TSeparator\>](/reference/runtime/qsys-runtime/fixed-time-2.html), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Converts a FixedTime value to double.
| [ToFixedDecimal\<TFormat, TSeparator\>](#decimal-tofixeddecimal-tformat-tseparator-fixedtime-tformat-tseparator-time-int-digits-int-decimals)([FixedTime\<TFormat, TSeparator\>](/reference/runtime/qsys-runtime/fixed-time-2.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Converts a FixedTime value, converts it to a decimal.
| [ToFloat\<TFormat, TSeparator\>](#float-tofloat-tformat-tseparator-fixedtime-tformat-tseparator-time-bool-throwonoverflow)([FixedTime\<TFormat, TSeparator\>](/reference/runtime/qsys-runtime/fixed-time-2.html), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Converts a FixedTime value to float.
| [ToInt16\<TFormat, TSeparator\>](#short-toint16-tformat-tseparator-fixedtime-tformat-tseparator-time-bool-throwonoverflow)([FixedTime\<TFormat, TSeparator\>](/reference/runtime/qsys-runtime/fixed-time-2.html), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Converts a FixedTime value to int 16.
| [ToInt32\<TFormat, TSeparator\>](#int-toint32-tformat-tseparator-fixedtime-tformat-tseparator-time-bool-throwonoverflow)([FixedTime\<TFormat, TSeparator\>](/reference/runtime/qsys-runtime/fixed-time-2.html), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Converts a FixedTime value to int 32.
| [ToInt64\<TFormat, TSeparator\>](#long-toint64-tformat-tseparator-fixedtime-tformat-tseparator-time-bool-throwonoverflow)([FixedTime\<TFormat, TSeparator\>](/reference/runtime/qsys-runtime/fixed-time-2.html), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Converts a FixedTime value to int 64.

### DateTime AddDuration\<TFormat, TSeparator\>([FixedTime\<TFormat, TSeparator\> time](/reference/runtime/qsys-runtime/fixed-time-2.html), [double duration](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [DurationCode durationCode](/reference/runtime/qsys-runtime/duration-code.html))

Adds a duration span to a FixedTime value.

```cs
DateTime AddDuration<TFormat, TSeparator>(FixedTime<TFormat, TSeparator> time, double duration, DurationCode durationCode)
```

### DateTime AddDurationToTime\<TFormat, TSeparator\>([FixedTime\<TFormat, TSeparator\> time](/reference/runtime/qsys-runtime/fixed-time-2.html), [double duration](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [DurationCode durationCode](/reference/runtime/qsys-runtime/duration-code.html))

Adds a duration span to a FixedTime value.

```cs
DateTime AddDurationToTime<TFormat, TSeparator>(FixedTime<TFormat, TSeparator> time, double duration, DurationCode durationCode)
```

### char MoveLeftToChar\<TFormat, TSeparator\>([FixedTime\<TFormat, TSeparator\> time](/reference/runtime/qsys-runtime/fixed-time-2.html))

RPG's MOVEL. Moves left a FixedTime in the given format to a char value.

```cs
char MoveLeftToChar<TFormat, TSeparator>(FixedTime<TFormat, TSeparator> time)
```

### char MoveRightToChar\<TFormat, TSeparator\>([FixedTime\<TFormat, TSeparator\> time](/reference/runtime/qsys-runtime/fixed-time-2.html))

RPG's MOVE. Moves right a FixedTime in the given format to a char value.

```cs
char MoveRightToChar<TFormat, TSeparator>(FixedTime<TFormat, TSeparator> time)
```

### DateTime SubtractDuration\<TFormat, TSeparator\>([FixedTime\<TFormat, TSeparator\> time](/reference/runtime/qsys-runtime/fixed-time-2.html), [double duration](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [DurationCode durationCode](/reference/runtime/qsys-runtime/duration-code.html))

Subtracts a duration span from a FixedTime or a timestamp value.

```cs
DateTime SubtractDuration<TFormat, TSeparator>(FixedTime<TFormat, TSeparator> time, double duration, DurationCode durationCode)
```

### DateTime SubtractDurationFromTime\<TFormat, TSeparator\>([FixedTime\<TFormat, TSeparator\> time](/reference/runtime/qsys-runtime/fixed-time-2.html), [double duration](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [DurationCode durationCode](/reference/runtime/qsys-runtime/duration-code.html))

Subtracts a duration span from a FixedTime value.

```cs
DateTime SubtractDurationFromTime<TFormat, TSeparator>(FixedTime<TFormat, TSeparator> time, double duration, DurationCode durationCode)
```

### double ToDouble\<TFormat, TSeparator\>([FixedTime\<TFormat, TSeparator\> time](/reference/runtime/qsys-runtime/fixed-time-2.html), [bool throwOnOverflow](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Converts a FixedTime value to double.

```cs
double ToDouble<TFormat, TSeparator>(FixedTime<TFormat, TSeparator> time, bool throwOnOverflow)
```

### decimal ToFixedDecimal\<TFormat, TSeparator\>([FixedTime\<TFormat, TSeparator\> time](/reference/runtime/qsys-runtime/fixed-time-2.html), [int digits](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int decimals](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Converts a FixedTime value, converts it to a decimal.

```cs
decimal ToFixedDecimal<TFormat, TSeparator>(FixedTime<TFormat, TSeparator> time, int digits, int decimals)
```

### float ToFloat\<TFormat, TSeparator\>([FixedTime\<TFormat, TSeparator\> time](/reference/runtime/qsys-runtime/fixed-time-2.html), [bool throwOnOverflow](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Converts a FixedTime value to float.

```cs
float ToFloat<TFormat, TSeparator>(FixedTime<TFormat, TSeparator> time, bool throwOnOverflow)
```

### short ToInt16\<TFormat, TSeparator\>([FixedTime\<TFormat, TSeparator\> time](/reference/runtime/qsys-runtime/fixed-time-2.html), [bool throwOnOverflow](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Converts a FixedTime value to int 16.

```cs
short ToInt16<TFormat, TSeparator>(FixedTime<TFormat, TSeparator> time, bool throwOnOverflow)
```

### int ToInt32\<TFormat, TSeparator\>([FixedTime\<TFormat, TSeparator\> time](/reference/runtime/qsys-runtime/fixed-time-2.html), [bool throwOnOverflow](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Converts a FixedTime value to int 32.

```cs
int ToInt32<TFormat, TSeparator>(FixedTime<TFormat, TSeparator> time, bool throwOnOverflow)
```

### long ToInt64\<TFormat, TSeparator\>([FixedTime\<TFormat, TSeparator\> time](/reference/runtime/qsys-runtime/fixed-time-2.html), [bool throwOnOverflow](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Converts a FixedTime value to int 64.

```cs
long ToInt64<TFormat, TSeparator>(FixedTime<TFormat, TSeparator> time, bool throwOnOverflow)
```
