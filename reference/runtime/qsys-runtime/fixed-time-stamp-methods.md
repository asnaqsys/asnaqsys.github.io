---
title: "FixedTimeStampMethods class   | QSYS API Reference Guide"
description: "Contains extension methods for handling RPG operations for FixedTimestamp values. "
last_modified_at: 2024-08-09T16:18:25Z
---

Contains extension methods for handling RPG operations for FixedTimestamp values.

**Namespace:** ASNA.QSys.Runtime
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>

## Methods

| Signature | Description |
| --- | --- |
| [AddDuration\<TSeparator\>](#datetime-addduration-tseparator-fixedtimestamp-tseparator-timestamp-double-duration-durationcode-durationcode)([FixedTimestamp\<TSeparator\>](/reference/runtime/qsys-runtime/fixed-timestamp-1.html), [Double](https://learn.microsoft.com/en-us/dotnet/api/system.double?view=net-8.0), [DurationCode](/reference/runtime/qsys-runtime/duration-code.html)) | Adds a duration span to a FixedTime value.
| [MergeDate\<TSeparator\>](#datetime-mergedate-tseparator-fixedtimestamp-tseparator-timestamp-datetime-date)([FixedTimestamp\<TSeparator\>](/reference/runtime/qsys-runtime/fixed-timestamp-1.html), [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime)) | Merges a date into the date part of a timestamp.
| [MergeTime\<TSeparator\>](#datetime-mergetime-tseparator-fixedtimestamp-tseparator-timestamp-datetime-time)([FixedTimestamp\<TSeparator\>](/reference/runtime/qsys-runtime/fixed-timestamp-1.html), [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime)) | Merges a time into the time part of a timestamp.
| [MoveLeft\<TSeparator\>](#short-moveleft-tseparator-fixedtimestamp-tseparator-timestamp-short-targetoperand)([FixedTimestamp\<TSeparator\>](/reference/runtime/qsys-runtime/fixed-timestamp-1.html), [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16)) | RPG's MOVEL. Moves left a datetime into a int2 (short).
| [MoveLeft\<TSeparator\>](#short-moveleft-tseparator-fixedtimestamp-tseparator-timestamp-short-targetoperand)([FixedTimestamp\<TSeparator\>](/reference/runtime/qsys-runtime/fixed-timestamp-1.html), [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16)) | RPG's MOVEL. Moves left a datetime into a int4 (int).
| [MoveLeft\<TSeparator\>](#short-moveleft-tseparator-fixedtimestamp-tseparator-timestamp-short-targetoperand)([FixedTimestamp\<TSeparator\>](/reference/runtime/qsys-runtime/fixed-timestamp-1.html), [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16)) | RPG's MOVEL. Moves left a datetime into a int8 (long).
| [MoveLeftToChar\<TSeparator\>](#char-movelefttochar-tseparator-fixedtimestamp-tseparator-timestamp)([FixedTimestamp\<TSeparator\>](/reference/runtime/qsys-runtime/fixed-timestamp-1.html)) | RPG's MOVEL. Moves left a date, time, timestamp in the given format to a char value.
| [MoveLeftWithPad\<TSeparator\>](#short-moveleftwithpad-tseparator-fixedtimestamp-tseparator-timestamp-short-targetoperand)([FixedTimestamp\<TSeparator\>](/reference/runtime/qsys-runtime/fixed-timestamp-1.html), [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16)) | RPG's MOVE. Moves right a datetime into a int2 (short) with pad.
| [MoveLeftWithPad\<TSeparator\>](#short-moveleftwithpad-tseparator-fixedtimestamp-tseparator-timestamp-short-targetoperand)([FixedTimestamp\<TSeparator\>](/reference/runtime/qsys-runtime/fixed-timestamp-1.html), [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16)) | RPG's MOVEL. Moves left a datetime into a int4 (int).
| [MoveLeftWithPad\<TSeparator\>](#short-moveleftwithpad-tseparator-fixedtimestamp-tseparator-timestamp-short-targetoperand)([FixedTimestamp\<TSeparator\>](/reference/runtime/qsys-runtime/fixed-timestamp-1.html), [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16)) | RPG's MOVEL. Moves left a datetime into a int8 (long).
| [MoveRight\<TSeparator\>](#short-moveright-tseparator-fixedtimestamp-tseparator-timestamp-short-targetoperand)([FixedTimestamp\<TSeparator\>](/reference/runtime/qsys-runtime/fixed-timestamp-1.html), [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16)) | RPG's MOVE. Moves right a datetime into a int2 (short).
| [MoveRight\<TSeparator\>](#short-moveright-tseparator-fixedtimestamp-tseparator-timestamp-short-targetoperand)([FixedTimestamp\<TSeparator\>](/reference/runtime/qsys-runtime/fixed-timestamp-1.html), [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16)) | RPG's MOVE. Moves right a datetime into a int4 (int).
| [MoveRight\<TSeparator\>](#short-moveright-tseparator-fixedtimestamp-tseparator-timestamp-short-targetoperand)([FixedTimestamp\<TSeparator\>](/reference/runtime/qsys-runtime/fixed-timestamp-1.html), [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16)) | RPG's MOVE. Moves right a datetime into a int8 (long).
| [MoveRightToChar\<TSeparator\>](#char-moverighttochar-tseparator-fixedtimestamp-tseparator-timestamp)([FixedTimestamp\<TSeparator\>](/reference/runtime/qsys-runtime/fixed-timestamp-1.html)) | RPG's MOVE. Moves right a date, time, timestamp in the given format to a char value.
| [MoveRightWithPad\<TSeparator\>](#short-moverightwithpad-tseparator-fixedtimestamp-tseparator-timestamp-short-targetoperand)([FixedTimestamp\<TSeparator\>](/reference/runtime/qsys-runtime/fixed-timestamp-1.html), [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16)) | RPG's MOVE. Moves right a datetime into a int2 (short) with pad.
| [MoveRightWithPad\<TSeparator\>](#short-moverightwithpad-tseparator-fixedtimestamp-tseparator-timestamp-short-targetoperand)([FixedTimestamp\<TSeparator\>](/reference/runtime/qsys-runtime/fixed-timestamp-1.html), [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16)) | RPG's MOVE. Moves right a datetime into a int4 (int) with pad.
| [MoveRightWithPad\<TSeparator\>](#short-moverightwithpad-tseparator-fixedtimestamp-tseparator-timestamp-short-targetoperand)([FixedTimestamp\<TSeparator\>](/reference/runtime/qsys-runtime/fixed-timestamp-1.html), [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16)) | RPG's MOVE. Moves right a datetime into a int8 (long) with pad.
| [SubtractDuration\<TSeparator\>](#datetime-subtractduration-tseparator-fixedtimestamp-tseparator-timestamp-double-duration-durationcode-durationcode)([FixedTimestamp\<TSeparator\>](/reference/runtime/qsys-runtime/fixed-timestamp-1.html), [Double](https://learn.microsoft.com/en-us/dotnet/api/system.double?view=net-8.0), [DurationCode](/reference/runtime/qsys-runtime/duration-code.html)) | Subtracts a duration span from a date or a timestamp value.
| [TimestampToDate\<TSeparator\>](#datetime-timestamptodate-tseparator-fixedtimestamp-tseparator-timestamp)([FixedTimestamp\<TSeparator\>](/reference/runtime/qsys-runtime/fixed-timestamp-1.html)) | Returns the Date portion of a timestamp.
| [TimestampToTime\<TSeparator\>](#datetime-timestamptotime-tseparator-fixedtimestamp-tseparator-timestamp)([FixedTimestamp\<TSeparator\>](/reference/runtime/qsys-runtime/fixed-timestamp-1.html)) | Returns the hours, minutes, and seconds of a timestamp.
| [TimestampToUSATime\<TSeparator\>](#datetime-timestamptousatime-tseparator-fixedtimestamp-tseparator-timestamp)([FixedTimestamp\<TSeparator\>](/reference/runtime/qsys-runtime/fixed-timestamp-1.html)) | Returns the hours and minutes of a timestamp.
| [ToDouble\<TSeparator\>](#double-todouble-tseparator-fixedtimestamp-tseparator-timestamp-bool-throwonoverflow)([FixedTimestamp\<TSeparator\>](/reference/runtime/qsys-runtime/fixed-timestamp-1.html), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Converts a timestamp value to double.
| [ToFixedDecimal\<TSeparator\>](#decimal-tofixeddecimal-tseparator-fixedtimestamp-tseparator-timestamp-int-digits-int-decimals)([FixedTimestamp\<TSeparator\>](/reference/runtime/qsys-runtime/fixed-timestamp-1.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Converts a timestamp to a decimal.
| [ToFloat\<TSeparator\>](#float-tofloat-tseparator-fixedtimestamp-tseparator-timestamp-bool-throwonoverflow)([FixedTimestamp\<TSeparator\>](/reference/runtime/qsys-runtime/fixed-timestamp-1.html), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Converts a timestamp value to float.
| [ToInt16\<TSeparator\>](#short-toint16-tseparator-fixedtimestamp-tseparator-timestamp-bool-throwonoverflow)([FixedTimestamp\<TSeparator\>](/reference/runtime/qsys-runtime/fixed-timestamp-1.html), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Converts a timestamp type to int 16.
| [ToInt32\<TSeparator\>](#int-toint32-tseparator-fixedtimestamp-tseparator-timestamp-bool-throwonoverflow)([FixedTimestamp\<TSeparator\>](/reference/runtime/qsys-runtime/fixed-timestamp-1.html), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Converts a timestamp type to int 32.
| [ToInt64\<TSeparator\>](#long-toint64-tseparator-fixedtimestamp-tseparator-timestamp-bool-throwonoverflow)([FixedTimestamp\<TSeparator\>](/reference/runtime/qsys-runtime/fixed-timestamp-1.html), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Converts a timestamp type to int 64.

### DateTime AddDuration\<TSeparator\>([FixedTimestamp\<TSeparator\> timestamp](/reference/runtime/qsys-runtime/fixed-timestamp-1.html), [double duration](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [DurationCode durationCode](/reference/runtime/qsys-runtime/duration-code.html))

Adds a duration span to a FixedTime value.

```cs
DateTime AddDuration<TSeparator>(FixedTimestamp<TSeparator> timestamp, double duration, DurationCode durationCode)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [FixedTimestamp\<TSeparator\>](/reference/runtime/qsys-runtime/fixed-timestamp-1.html) | timestamp | .NET FixedTime value specifying a FixedTime value.
| [Double](https://learn.microsoft.com/en-us/dotnet/api/system.double?view=net-8.0) | duration | A double value representing duration.
| [DurationCode](/reference/runtime/qsys-runtime/duration-code.html) | durationCode | Code determining what duration represents.

#### Returns

| Type | Description
| --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | The resulting DateTime value after adding to it the given duration.

### DateTime MergeDate\<TSeparator\>([FixedTimestamp\<TSeparator\> timestamp](/reference/runtime/qsys-runtime/fixed-timestamp-1.html), [DateTime date](https://docs.microsoft.com/en-us/dotnet/api/system.datetime))

Merges a date into the date part of a timestamp.

```cs
DateTime MergeDate<TSeparator>(FixedTimestamp<TSeparator> timestamp, DateTime date)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [FixedTimestamp\<TSeparator\>](/reference/runtime/qsys-runtime/fixed-timestamp-1.html) | timestamp | timestamp to be merged.
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | date | date to merge.

#### Returns

| Type | Description
| --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | .NET DateTime value.

### DateTime MergeTime\<TSeparator\>([FixedTimestamp\<TSeparator\> timestamp](/reference/runtime/qsys-runtime/fixed-timestamp-1.html), [DateTime time](https://docs.microsoft.com/en-us/dotnet/api/system.datetime))

Merges a time into the time part of a timestamp.

```cs
DateTime MergeTime<TSeparator>(FixedTimestamp<TSeparator> timestamp, DateTime time)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [FixedTimestamp\<TSeparator\>](/reference/runtime/qsys-runtime/fixed-timestamp-1.html) | timestamp | timestamp to be merged.
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | time | time to merge.

#### Returns

| Type | Description
| --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | .NET DateTime value.

### short MoveLeft\<TSeparator\>([FixedTimestamp\<TSeparator\> timestamp](/reference/runtime/qsys-runtime/fixed-timestamp-1.html), [short targetOperand](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVEL. Moves left a datetime into a int2 (short).

```cs
short MoveLeft<TSeparator>(FixedTimestamp<TSeparator> timestamp, short targetOperand)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [FixedTimestamp\<TSeparator\>](/reference/runtime/qsys-runtime/fixed-timestamp-1.html) | timestamp | The timestamp value.
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | targetOperand | The short value target of the operation.

#### Returns

| Type | Description
| --- | ---
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | The resulting short value of the operation.

### short MoveLeft\<TSeparator\>([FixedTimestamp\<TSeparator\> timestamp](/reference/runtime/qsys-runtime/fixed-timestamp-1.html), [short targetOperand](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVEL. Moves left a datetime into a int4 (int).

```cs
short MoveLeft<TSeparator>(FixedTimestamp<TSeparator> timestamp, short targetOperand)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [FixedTimestamp\<TSeparator\>](/reference/runtime/qsys-runtime/fixed-timestamp-1.html) | timestamp | The timestamp value.
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | targetOperand | The int value target of the operation.

#### Returns

| Type | Description
| --- | ---
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | The resulting int value of the operation.

### short MoveLeft\<TSeparator\>([FixedTimestamp\<TSeparator\> timestamp](/reference/runtime/qsys-runtime/fixed-timestamp-1.html), [short targetOperand](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVEL. Moves left a datetime into a int8 (long).

```cs
short MoveLeft<TSeparator>(FixedTimestamp<TSeparator> timestamp, short targetOperand)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [FixedTimestamp\<TSeparator\>](/reference/runtime/qsys-runtime/fixed-timestamp-1.html) | timestamp | The timestamp value.
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | targetOperand | The long value target of the operation.

#### Returns

| Type | Description
| --- | ---
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | The resulting long value of the operation.

### char MoveLeftToChar\<TSeparator\>([FixedTimestamp\<TSeparator\> timestamp](/reference/runtime/qsys-runtime/fixed-timestamp-1.html))

RPG's MOVEL. Moves left a date, time, timestamp in the given format to a char value.

```cs
char MoveLeftToChar<TSeparator>(FixedTimestamp<TSeparator> timestamp)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [FixedTimestamp\<TSeparator\>](/reference/runtime/qsys-runtime/fixed-timestamp-1.html) | timestamp | The timestamp value.

#### Returns

| Type | Description
| --- | ---
| [Char](https://docs.microsoft.com/en-us/dotnet/api/system.char) | The leftmost character of the string representation of timestamp.

### short MoveLeftWithPad\<TSeparator\>([FixedTimestamp\<TSeparator\> timestamp](/reference/runtime/qsys-runtime/fixed-timestamp-1.html), [short targetOperand](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVE. Moves right a datetime into a int2 (short) with pad.

```cs
short MoveLeftWithPad<TSeparator>(FixedTimestamp<TSeparator> timestamp, short targetOperand)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [FixedTimestamp\<TSeparator\>](/reference/runtime/qsys-runtime/fixed-timestamp-1.html) | timestamp | The timestamp value.
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | targetOperand | The short value target of the operation.

#### Returns

| Type | Description
| --- | ---
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | The resulting short value of the operation.

### short MoveLeftWithPad\<TSeparator\>([FixedTimestamp\<TSeparator\> timestamp](/reference/runtime/qsys-runtime/fixed-timestamp-1.html), [short targetOperand](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVEL. Moves left a datetime into a int4 (int).

```cs
short MoveLeftWithPad<TSeparator>(FixedTimestamp<TSeparator> timestamp, short targetOperand)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [FixedTimestamp\<TSeparator\>](/reference/runtime/qsys-runtime/fixed-timestamp-1.html) | timestamp | The timestamp value.
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | targetOperand | The int value target of the operation.

#### Returns

| Type | Description
| --- | ---
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | The resulting int value of the operation.

### short MoveLeftWithPad\<TSeparator\>([FixedTimestamp\<TSeparator\> timestamp](/reference/runtime/qsys-runtime/fixed-timestamp-1.html), [short targetOperand](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVEL. Moves left a datetime into a int8 (long).

```cs
short MoveLeftWithPad<TSeparator>(FixedTimestamp<TSeparator> timestamp, short targetOperand)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [FixedTimestamp\<TSeparator\>](/reference/runtime/qsys-runtime/fixed-timestamp-1.html) | timestamp | The timestamp value.
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | targetOperand | The long value target of the operation.

#### Returns

| Type | Description
| --- | ---
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | The resulting long value of the operation.

### short MoveRight\<TSeparator\>([FixedTimestamp\<TSeparator\> timestamp](/reference/runtime/qsys-runtime/fixed-timestamp-1.html), [short targetOperand](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVE. Moves right a datetime into a int2 (short).

```cs
short MoveRight<TSeparator>(FixedTimestamp<TSeparator> timestamp, short targetOperand)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [FixedTimestamp\<TSeparator\>](/reference/runtime/qsys-runtime/fixed-timestamp-1.html) | timestamp | The timestamp value.
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | targetOperand | The short value target of the operation.

#### Returns

| Type | Description
| --- | ---
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | The resulting short value of the operation.

### short MoveRight\<TSeparator\>([FixedTimestamp\<TSeparator\> timestamp](/reference/runtime/qsys-runtime/fixed-timestamp-1.html), [short targetOperand](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVE. Moves right a datetime into a int4 (int).

```cs
short MoveRight<TSeparator>(FixedTimestamp<TSeparator> timestamp, short targetOperand)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [FixedTimestamp\<TSeparator\>](/reference/runtime/qsys-runtime/fixed-timestamp-1.html) | timestamp | The timestamp value.
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | targetOperand | The int value target of the operation.

#### Returns

| Type | Description
| --- | ---
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | The resulting int value of the operation.

### short MoveRight\<TSeparator\>([FixedTimestamp\<TSeparator\> timestamp](/reference/runtime/qsys-runtime/fixed-timestamp-1.html), [short targetOperand](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVE. Moves right a datetime into a int8 (long).

```cs
short MoveRight<TSeparator>(FixedTimestamp<TSeparator> timestamp, short targetOperand)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [FixedTimestamp\<TSeparator\>](/reference/runtime/qsys-runtime/fixed-timestamp-1.html) | timestamp | The timestamp value.
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | targetOperand | The long value target of the operation.

#### Returns

| Type | Description
| --- | ---
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | The resulting long value of the operation.

### char MoveRightToChar\<TSeparator\>([FixedTimestamp\<TSeparator\> timestamp](/reference/runtime/qsys-runtime/fixed-timestamp-1.html))

RPG's MOVE. Moves right a date, time, timestamp in the given format to a char value.

```cs
char MoveRightToChar<TSeparator>(FixedTimestamp<TSeparator> timestamp)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [FixedTimestamp\<TSeparator\>](/reference/runtime/qsys-runtime/fixed-timestamp-1.html) | timestamp | The timestamp value.

#### Returns

| Type | Description
| --- | ---
| [Char](https://docs.microsoft.com/en-us/dotnet/api/system.char) | The rightmost character of the string representation of timestamp.

### short MoveRightWithPad\<TSeparator\>([FixedTimestamp\<TSeparator\> timestamp](/reference/runtime/qsys-runtime/fixed-timestamp-1.html), [short targetOperand](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVE. Moves right a datetime into a int2 (short) with pad.

```cs
short MoveRightWithPad<TSeparator>(FixedTimestamp<TSeparator> timestamp, short targetOperand)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [FixedTimestamp\<TSeparator\>](/reference/runtime/qsys-runtime/fixed-timestamp-1.html) | timestamp | The timestamp value.
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | targetOperand | The short value target of the operation.

#### Returns

| Type | Description
| --- | ---
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | The resulting short value of the operation.

### short MoveRightWithPad\<TSeparator\>([FixedTimestamp\<TSeparator\> timestamp](/reference/runtime/qsys-runtime/fixed-timestamp-1.html), [short targetOperand](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVE. Moves right a datetime into a int4 (int) with pad.

```cs
short MoveRightWithPad<TSeparator>(FixedTimestamp<TSeparator> timestamp, short targetOperand)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [FixedTimestamp\<TSeparator\>](/reference/runtime/qsys-runtime/fixed-timestamp-1.html) | timestamp | The timestamp value.
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | targetOperand | The int value target of the operation.

#### Returns

| Type | Description
| --- | ---
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | The resulting int value of the operation.

### short MoveRightWithPad\<TSeparator\>([FixedTimestamp\<TSeparator\> timestamp](/reference/runtime/qsys-runtime/fixed-timestamp-1.html), [short targetOperand](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVE. Moves right a datetime into a int8 (long) with pad.

```cs
short MoveRightWithPad<TSeparator>(FixedTimestamp<TSeparator> timestamp, short targetOperand)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [FixedTimestamp\<TSeparator\>](/reference/runtime/qsys-runtime/fixed-timestamp-1.html) | timestamp | The timestamp value.
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | targetOperand | The long value target of the operation.

#### Returns

| Type | Description
| --- | ---
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | The resulting long value of the operation.

### DateTime SubtractDuration\<TSeparator\>([FixedTimestamp\<TSeparator\> timestamp](/reference/runtime/qsys-runtime/fixed-timestamp-1.html), [double duration](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [DurationCode durationCode](/reference/runtime/qsys-runtime/duration-code.html))

Subtracts a duration span from a date or a timestamp value.

```cs
DateTime SubtractDuration<TSeparator>(FixedTimestamp<TSeparator> timestamp, double duration, DurationCode durationCode)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [FixedTimestamp\<TSeparator\>](/reference/runtime/qsys-runtime/fixed-timestamp-1.html) | timestamp | The timestamp value.
| [Double](https://learn.microsoft.com/en-us/dotnet/api/system.double?view=net-8.0) | duration | A double value representing duration.
| [DurationCode](/reference/runtime/qsys-runtime/duration-code.html) | durationCode | Code determining what duration represents.

#### Returns

| Type | Description
| --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | The resulting DateTime value after subracting from it the given duration.

### DateTime TimestampToDate\<TSeparator\>([FixedTimestamp\<TSeparator\> timestamp](/reference/runtime/qsys-runtime/fixed-timestamp-1.html))

Returns the Date portion of a timestamp.

```cs
DateTime TimestampToDate<TSeparator>(FixedTimestamp<TSeparator> timestamp)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [FixedTimestamp\<TSeparator\>](/reference/runtime/qsys-runtime/fixed-timestamp-1.html) | timestamp | The timestamp value.

#### Returns

| Type | Description
| --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | The DateTime value containing the date portion of the timestamp argument.

### DateTime TimestampToTime\<TSeparator\>([FixedTimestamp\<TSeparator\> timestamp](/reference/runtime/qsys-runtime/fixed-timestamp-1.html))

Returns the hours, minutes, and seconds of a timestamp.

```cs
DateTime TimestampToTime<TSeparator>(FixedTimestamp<TSeparator> timestamp)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [FixedTimestamp\<TSeparator\>](/reference/runtime/qsys-runtime/fixed-timestamp-1.html) | timestamp | The timestamp value.

#### Returns

| Type | Description
| --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | The DateTime value containing the hours, minutes, and seconds portion of the timestamp argument.

### DateTime TimestampToUSATime\<TSeparator\>([FixedTimestamp\<TSeparator\> timestamp](/reference/runtime/qsys-runtime/fixed-timestamp-1.html))

Returns the hours and minutes of a timestamp.

```cs
DateTime TimestampToUSATime<TSeparator>(FixedTimestamp<TSeparator> timestamp)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [FixedTimestamp\<TSeparator\>](/reference/runtime/qsys-runtime/fixed-timestamp-1.html) | timestamp | The timestamp value.

#### Returns

| Type | Description
| --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | The DateTime value containing the hours and minutes portion of the timestamp argument.

### double ToDouble\<TSeparator\>([FixedTimestamp\<TSeparator\> timestamp](/reference/runtime/qsys-runtime/fixed-timestamp-1.html), [bool throwOnOverflow](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Converts a timestamp value to double.

```cs
double ToDouble<TSeparator>(FixedTimestamp<TSeparator> timestamp, bool throwOnOverflow)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [FixedTimestamp\<TSeparator\>](/reference/runtime/qsys-runtime/fixed-timestamp-1.html) | timestamp | The timestamp value.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | throwOnOverflow | Default is false. Pass true if a runtime exception is desired when the conversion doesn't fit.

#### Returns

| Type | Description
| --- | ---
| [Double](https://learn.microsoft.com/en-us/dotnet/api/system.double?view=net-8.0) | The double value corresponding to the timestamp according to its format.

### decimal ToFixedDecimal\<TSeparator\>([FixedTimestamp\<TSeparator\> timestamp](/reference/runtime/qsys-runtime/fixed-timestamp-1.html), [int digits](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int decimals](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Converts a timestamp to a decimal.

```cs
decimal ToFixedDecimal<TSeparator>(FixedTimestamp<TSeparator> timestamp, int digits, int decimals)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [FixedTimestamp\<TSeparator\>](/reference/runtime/qsys-runtime/fixed-timestamp-1.html) | timestamp | The timestamp value.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | digits | number of digits in the targetOperand.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | decimals | number of decimal places in the targetOperand.

#### Returns

| Type | Description
| --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | The decimal value corresponding to the timestamp according to its format.

### float ToFloat\<TSeparator\>([FixedTimestamp\<TSeparator\> timestamp](/reference/runtime/qsys-runtime/fixed-timestamp-1.html), [bool throwOnOverflow](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Converts a timestamp value to float.

```cs
float ToFloat<TSeparator>(FixedTimestamp<TSeparator> timestamp, bool throwOnOverflow)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [FixedTimestamp\<TSeparator\>](/reference/runtime/qsys-runtime/fixed-timestamp-1.html) | timestamp | The timestamp value.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | throwOnOverflow | Default is false. Pass true if a runtime exception is desired when the conversion doesn't fit.

#### Returns

| Type | Description
| --- | ---
| [Single](https://learn.microsoft.com/en-us/dotnet/api/system.single?view=net-8.0) | The float value corresponding to the timestamp according to its format.

### short ToInt16\<TSeparator\>([FixedTimestamp\<TSeparator\> timestamp](/reference/runtime/qsys-runtime/fixed-timestamp-1.html), [bool throwOnOverflow](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Converts a timestamp type to int 16.

```cs
short ToInt16<TSeparator>(FixedTimestamp<TSeparator> timestamp, bool throwOnOverflow)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [FixedTimestamp\<TSeparator\>](/reference/runtime/qsys-runtime/fixed-timestamp-1.html) | timestamp | The timestamp value.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | throwOnOverflow | Default is false. Pass true if a runtime exception is desired when the conversion doesn't fit.

#### Returns

| Type | Description
| --- | ---
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | The short value corresponding to the timestamp according to its format.

### int ToInt32\<TSeparator\>([FixedTimestamp\<TSeparator\> timestamp](/reference/runtime/qsys-runtime/fixed-timestamp-1.html), [bool throwOnOverflow](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Converts a timestamp type to int 32.

```cs
int ToInt32<TSeparator>(FixedTimestamp<TSeparator> timestamp, bool throwOnOverflow)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [FixedTimestamp\<TSeparator\>](/reference/runtime/qsys-runtime/fixed-timestamp-1.html) | timestamp | The timestamp value.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | throwOnOverflow | Default is false. Pass true if a runtime exception is desired when the conversion doesn't fit.

#### Returns

| Type | Description
| --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | The int value corresponding to the timestamp according to its format.

### long ToInt64\<TSeparator\>([FixedTimestamp\<TSeparator\> timestamp](/reference/runtime/qsys-runtime/fixed-timestamp-1.html), [bool throwOnOverflow](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Converts a timestamp type to int 64.

```cs
long ToInt64<TSeparator>(FixedTimestamp<TSeparator> timestamp, bool throwOnOverflow)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [FixedTimestamp\<TSeparator\>](/reference/runtime/qsys-runtime/fixed-timestamp-1.html) | timestamp | The timestamp value.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | throwOnOverflow | Default is false. Pass true if a runtime exception is desired when the conversion doesn't fit.

#### Returns

| Type | Description
| --- | ---
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | The long value corresponding to the timestamp according to its format.
