---
title: "DateTimeMethods class         | QSYS API Reference Guide"
description: "Contains extension methods for handling Date/Time/Timestamp conversions. "
last_modified_at: 2024-08-08T21:41:46Z
---

Contains extension methods for handling Date/Time/Timestamp conversions.

**Namespace:** ASNA.QSys.Runtime
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>

## Methods

| Signature | Description |
| --- | --- |
| [GetFormatLength](#int-getformatlengthdatetimedatakind-kind-datetimeformat-format-datetimeseparator-separator)([DateTimeDataKind](/reference/runtime/qsys-runtime/date-time-data-kind.html), [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html), [DateTimeSeparator](/reference/runtime/qsys-runtime/date-time-separator.html)) | Returns the length of the string representation of a date/time/timestamp type.
| [MergeDate](#datetime-mergedatedatetime-timestamp-datetime-date)([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime)) | Merges a date into the date part of a timestamp.
| [MergeTime](#datetime-mergetimedatetime-timestamp-datetime-time)([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime)) | Merges a time into the time part of a timestamp.
| [MoveLeft](#string-moveleftdatetime-datetime-datetimedatakind-datetimekind-datetimeformat-datetimeformat-datetimeseparator-datetimeseparator-string-targetoperand)([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind](/reference/runtime/qsys-runtime/date-time-data-kind.html), [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html), [DateTimeSeparator](/reference/runtime/qsys-runtime/date-time-separator.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | RPG's MOVEL. Moves left a DateTime to string.
| [MoveLeft](#decimal-moveleftdatetime-datetime-datetimedatakind-datetimekind-datetimeformat-datetimeformat-decimal-targetoperand-int-digits-int-decimals)([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind](/reference/runtime/qsys-runtime/date-time-data-kind.html), [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html), [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's MOVEL. Moves left a DateTime to decimal.
| [MoveLeft](#short-moveleftdatetime-datetime-datetimedatakind-datetimekind-datetimeformat-datetimeformat-short-targetoperand)([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind](/reference/runtime/qsys-runtime/date-time-data-kind.html), [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html), [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16)) | RPG's MOVEL. Moves left a datetime into a int2 (short).
| [MoveLeft](#int-moveleftdatetime-datetime-datetimedatakind-datetimekind-datetimeformat-datetimeformat-int-targetoperand)([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind](/reference/runtime/qsys-runtime/date-time-data-kind.html), [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's MOVEL. Moves left a datetime into a int4 (int).
| [MoveLeft](#long-moveleftdatetime-datetime-datetimedatakind-datetimekind-datetimeformat-datetimeformat-long-targetoperand)([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind](/reference/runtime/qsys-runtime/date-time-data-kind.html), [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html), [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64)) | RPG's MOVEL. Moves left a datetime into a int8 (long).
| [MoveLeftToChar](#char-movelefttochardatetime-datetime-datetimedatakind-datetimekind-datetimeformat-datetimeformat)([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind](/reference/runtime/qsys-runtime/date-time-data-kind.html), [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html)) | RPG's MOVEL. Moves left a date, time, timestamp in the given format to a char value.
| [MoveLeftWithPad](#string-moveleftwithpaddatetime-datetime-datetimedatakind-datetimekind-datetimeformat-datetimeformat-datetimeseparator-datetimeseparator-string-targetoperand)([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind](/reference/runtime/qsys-runtime/date-time-data-kind.html), [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html), [DateTimeSeparator](/reference/runtime/qsys-runtime/date-time-separator.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | RPG's MOVEL. Moves left a DateTime to string with pad.
| [MoveLeftWithPad](#decimal-moveleftwithpaddatetime-datetime-datetimedatakind-datetimekind-datetimeformat-datetimeformat-decimal-targetoperand-int-digits-int-decimals)([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind](/reference/runtime/qsys-runtime/date-time-data-kind.html), [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html), [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's MOVEL. Moves left a DateTime to decimal with pad.
| [MoveLeftWithPad](#short-moveleftwithpaddatetime-datetime-datetimedatakind-datetimekind-datetimeformat-datetimeformat-short-targetoperand)([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind](/reference/runtime/qsys-runtime/date-time-data-kind.html), [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html), [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16)) | RPG's MOVE. Moves right a datetime into a int2 (short) with pad.
| [MoveLeftWithPad](#int-moveleftwithpaddatetime-datetime-datetimedatakind-datetimekind-datetimeformat-datetimeformat-int-targetoperand)([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind](/reference/runtime/qsys-runtime/date-time-data-kind.html), [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's MOVEL. Moves left a datetime into a int4 (int).
| [MoveLeftWithPad](#long-moveleftwithpaddatetime-datetime-datetimedatakind-datetimekind-datetimeformat-datetimeformat-long-targetoperand)([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind](/reference/runtime/qsys-runtime/date-time-data-kind.html), [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html), [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64)) | RPG's MOVEL. Moves left a datetime into a int8 (long).
| [MoveRight](#string-moverightdatetime-datetime-datetimedatakind-datetimekind-datetimeformat-datetimeformat-datetimeseparator-datetimeseparator-string-targetoperand)([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind](/reference/runtime/qsys-runtime/date-time-data-kind.html), [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html), [DateTimeSeparator](/reference/runtime/qsys-runtime/date-time-separator.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | RPG's MOVE. Moves right a DateTime to string.
| [MoveRight](#decimal-moverightdatetime-datetime-datetimedatakind-datetimekind-datetimeformat-datetimeformat-decimal-targetoperand-int-digits-int-decimals)([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind](/reference/runtime/qsys-runtime/date-time-data-kind.html), [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html), [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's MOVE. Moves right s DateTime to decimal.
| [MoveRight](#short-moverightdatetime-datetime-datetimedatakind-datetimekind-datetimeformat-datetimeformat-short-targetoperand)([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind](/reference/runtime/qsys-runtime/date-time-data-kind.html), [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html), [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16)) | RPG's MOVE. Moves right a datetime into a int2 (short).
| [MoveRight](#int-moverightdatetime-datetime-datetimedatakind-datetimekind-datetimeformat-datetimeformat-int-targetoperand)([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind](/reference/runtime/qsys-runtime/date-time-data-kind.html), [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's MOVE. Moves right a datetime into a int4 (int).
| [MoveRight](#long-moverightdatetime-datetime-datetimedatakind-datetimekind-datetimeformat-datetimeformat-long-targetoperand)([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind](/reference/runtime/qsys-runtime/date-time-data-kind.html), [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html), [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64)) | RPG's MOVE. Moves right a datetime into a int8 (long).
| [MoveRightToChar](#char-moverighttochardatetime-datetime-datetimedatakind-datetimekind-datetimeformat-datetimeformat)([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind](/reference/runtime/qsys-runtime/date-time-data-kind.html), [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html)) | RPG's MOVE. Moves right a date, time, timestamp in the given format to a char value.
| [MoveRightWithPad](#string-moverightwithpaddatetime-datetime-datetimedatakind-datetimekind-datetimeformat-datetimeformat-datetimeseparator-datetimeseparator-string-targetoperand)([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind](/reference/runtime/qsys-runtime/date-time-data-kind.html), [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html), [DateTimeSeparator](/reference/runtime/qsys-runtime/date-time-separator.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | RPG's MOVE. Moves right a DateTime to string with pad.
| [MoveRightWithPad](#decimal-moverightwithpaddatetime-datetime-datetimedatakind-datetimekind-datetimeformat-datetimeformat-decimal-targetoperand-int-digits-int-decimals)([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind](/reference/runtime/qsys-runtime/date-time-data-kind.html), [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html), [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's MOVE. Moves right a DateTime to decimal with pad.
| [MoveRightWithPad](#short-moverightwithpaddatetime-datetime-datetimedatakind-datetimekind-datetimeformat-datetimeformat-short-targetoperand)([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind](/reference/runtime/qsys-runtime/date-time-data-kind.html), [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html), [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16)) | RPG's MOVE. Moves right a datetime into a int2 (short) with pad.
| [MoveRightWithPad](#int-moverightwithpaddatetime-datetime-datetimedatakind-datetimekind-datetimeformat-datetimeformat-int-targetoperand)([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind](/reference/runtime/qsys-runtime/date-time-data-kind.html), [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's MOVE. Moves right a datetime into a int4 (int) with pad.
| [MoveRightWithPad](#long-moverightwithpaddatetime-datetime-datetimedatakind-datetimekind-datetimeformat-datetimeformat-long-targetoperand)([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind](/reference/runtime/qsys-runtime/date-time-data-kind.html), [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html), [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64)) | RPG's MOVE. Moves right a datetime into a int8 (long) with pad.
| [NormalizeYear](#datetime-normalizeyeardatetime-datetime)([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime)) | Turns a 4 digit year into a 2 digit year between 1940 and 2039
| [TimestampToDate](#datetime-timestamptodatedatetime-timestamp)([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime)) | Returns the Date portion of a timestamp.
| [TimestampToTime](#datetime-timestamptotimedatetime-timestamp)([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime)) | Returns the hours, minutes, and seconds of a timestamp.
| [TimestampToUSATime](#datetime-timestamptousatimedatetime-timestamp)([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime)) | Returns the hours and minutes of a timestamp.
| [ToFixedDecimal](#decimal-tofixeddecimaldatetime-datetime-datetimedatakind-datetimekind-datetimeformat-datetimeformat-int-digits-int-decimals)([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind](/reference/runtime/qsys-runtime/date-time-data-kind.html), [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Converts a dateTime type, converts it to a decimal.
| [ToFixedDecimal](#decimal-tofixeddecimaldatetime-datetime-datetimedatakind-datetimekind-datetimeformat-datetimeformat)([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind](/reference/runtime/qsys-runtime/date-time-data-kind.html), [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html)) | Converts a dateTime type to decimal.
| [ToInt16](#short-toint16datetime-datetime-datetimedatakind-datetimekind-datetimeformat-datetimeformat-bool-throwonoverflow)([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind](/reference/runtime/qsys-runtime/date-time-data-kind.html), [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Converts a dateTime type to int 16.
| [ToInt32](#int-toint32datetime-datetime-datetimedatakind-datetimekind-datetimeformat-datetimeformat-bool-throwonoverflow)([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind](/reference/runtime/qsys-runtime/date-time-data-kind.html), [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Converts a dateTime type to int 32.
| [ToInt64](#long-toint64datetime-datetime-datetimedatakind-datetimekind-datetimeformat-datetimeformat-bool-throwonoverflow)([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind](/reference/runtime/qsys-runtime/date-time-data-kind.html), [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Converts a dateTime type to int 64.
| [ToString](#string-tostringdatetime-datetime-datetimedatakind-datetimekind-datetimeformat-datetimeformat-datetimeseparator-datetimeseparator)([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind](/reference/runtime/qsys-runtime/date-time-data-kind.html), [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html), [DateTimeSeparator](/reference/runtime/qsys-runtime/date-time-separator.html)) | Converts a DateTime with the specified Kind and Format to a string using the specified separator.

### int GetFormatLength([DateTimeDataKind kind](/reference/runtime/qsys-runtime/date-time-data-kind.html), [DateTimeFormat format](/reference/datagate/datagate-common/date-time-format.html), [DateTimeSeparator separator](/reference/runtime/qsys-runtime/date-time-separator.html))

Returns the length of the string representation of a date/time/timestamp type.

```cs
int GetFormatLength(DateTimeDataKind kind, DateTimeFormat format, DateTimeSeparator separator)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DateTimeDataKind](/reference/runtime/qsys-runtime/date-time-data-kind.html) | kind | The kind of datetime type.
| [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html) | format | The format of the type.
| [DateTimeSeparator](/reference/runtime/qsys-runtime/date-time-separator.html) | separator | The datetime separator.

#### Returns

| Type | Description
| --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | The computed length.

### DateTime MergeDate([DateTime timestamp](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTime date](https://docs.microsoft.com/en-us/dotnet/api/system.datetime))

Merges a date into the date part of a timestamp.

```cs
DateTime MergeDate(DateTime timestamp, DateTime date)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | timestamp | timestamp to be merged.
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | date | date to merge.

#### Returns

| Type | Description
| --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | .NET DateTime value.

### DateTime MergeTime([DateTime timestamp](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTime time](https://docs.microsoft.com/en-us/dotnet/api/system.datetime))

Merges a time into the time part of a timestamp.

```cs
DateTime MergeTime(DateTime timestamp, DateTime time)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | timestamp | timestamp to be merged.
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | time | time to merge.

#### Returns

| Type | Description
| --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | .NET DateTime value.

### string MoveLeft([DateTime dateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind dateTimeKind](/reference/runtime/qsys-runtime/date-time-data-kind.html), [DateTimeFormat dateTimeFormat](/reference/datagate/datagate-common/date-time-format.html), [DateTimeSeparator dateTimeSeparator](/reference/runtime/qsys-runtime/date-time-separator.html), [string targetOperand](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

RPG's MOVEL. Moves left a DateTime to string.

```cs
string MoveLeft(DateTime dateTime, DateTimeDataKind dateTimeKind, DateTimeFormat dateTimeFormat, DateTimeSeparator dateTimeSeparator, string targetOperand)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | dateTime | The date/time/timestamp value to move.
| [DateTimeDataKind](/reference/runtime/qsys-runtime/date-time-data-kind.html) | dateTimeKind | The DateTimeDataKind value that specifies whether it is a date, time, or timestamp.
| [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html) | dateTimeFormat | The DateTimeFormat of the value.
| [DateTimeSeparator](/reference/runtime/qsys-runtime/date-time-separator.html) | dateTimeSeparator | The DateTimeSeparator of the value.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | targetOperand | The string value that is the target of the MOVEL.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The string resulting from the MOVEL operation of the dateTime with the given format and separator into the targetOperand string.

### decimal MoveLeft([DateTime dateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind dateTimeKind](/reference/runtime/qsys-runtime/date-time-data-kind.html), [DateTimeFormat dateTimeFormat](/reference/datagate/datagate-common/date-time-format.html), [decimal targetOperand](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [int digits](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int decimals](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVEL. Moves left a DateTime to decimal.

```cs
decimal MoveLeft(DateTime dateTime, DateTimeDataKind dateTimeKind, DateTimeFormat dateTimeFormat, decimal targetOperand, int digits, int decimals)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | dateTime | .NET DateTime value.
| [DateTimeDataKind](/reference/runtime/qsys-runtime/date-time-data-kind.html) | dateTimeKind | The kind that the dateTime should be interpreted as.
| [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html) | dateTimeFormat | The format of the dateTime.
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | targetOperand | The targetOperand decimal.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | digits | The number of digits in the targetOperand.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | decimals | The number of decimal places in the targetOperand.

#### Returns

| Type | Description
| --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | The resulting decimal value of the operation.

### short MoveLeft([DateTime dateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind dateTimeKind](/reference/runtime/qsys-runtime/date-time-data-kind.html), [DateTimeFormat dateTimeFormat](/reference/datagate/datagate-common/date-time-format.html), [short targetOperand](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVEL. Moves left a datetime into a int2 (short).

```cs
short MoveLeft(DateTime dateTime, DateTimeDataKind dateTimeKind, DateTimeFormat dateTimeFormat, short targetOperand)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | dateTime | .NET DateTime value.
| [DateTimeDataKind](/reference/runtime/qsys-runtime/date-time-data-kind.html) | dateTimeKind | The kind that the dateTime should be interpreted as.
| [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html) | dateTimeFormat | The format of the dateTime.
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | targetOperand | The short value target of the operation.

#### Returns

| Type | Description
| --- | ---
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | The resulting short value of the operation.

### int MoveLeft([DateTime dateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind dateTimeKind](/reference/runtime/qsys-runtime/date-time-data-kind.html), [DateTimeFormat dateTimeFormat](/reference/datagate/datagate-common/date-time-format.html), [int targetOperand](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVEL. Moves left a datetime into a int4 (int).

```cs
int MoveLeft(DateTime dateTime, DateTimeDataKind dateTimeKind, DateTimeFormat dateTimeFormat, int targetOperand)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | dateTime | .NET DateTime value.
| [DateTimeDataKind](/reference/runtime/qsys-runtime/date-time-data-kind.html) | dateTimeKind | The kind that the dateTime should be interpreted as.
| [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html) | dateTimeFormat | The format of the dateTime.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetOperand | The int value target of the operation.

#### Returns

| Type | Description
| --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | The resulting int value of the operation.

### long MoveLeft([DateTime dateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind dateTimeKind](/reference/runtime/qsys-runtime/date-time-data-kind.html), [DateTimeFormat dateTimeFormat](/reference/datagate/datagate-common/date-time-format.html), [long targetOperand](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVEL. Moves left a datetime into a int8 (long).

```cs
long MoveLeft(DateTime dateTime, DateTimeDataKind dateTimeKind, DateTimeFormat dateTimeFormat, long targetOperand)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | dateTime | .NET DateTime value.
| [DateTimeDataKind](/reference/runtime/qsys-runtime/date-time-data-kind.html) | dateTimeKind | The kind that the dateTime should be interpreted as.
| [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html) | dateTimeFormat | The format of the dateTime.
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | targetOperand | The long value target of the operation.

#### Returns

| Type | Description
| --- | ---
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | The resulting long value of the operation.

### char MoveLeftToChar([DateTime dateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind dateTimeKind](/reference/runtime/qsys-runtime/date-time-data-kind.html), [DateTimeFormat dateTimeFormat](/reference/datagate/datagate-common/date-time-format.html))

RPG's MOVEL. Moves left a date, time, timestamp in the given format to a char value.

```cs
char MoveLeftToChar(DateTime dateTime, DateTimeDataKind dateTimeKind, DateTimeFormat dateTimeFormat)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | dateTime | .NET DateTime value.
| [DateTimeDataKind](/reference/runtime/qsys-runtime/date-time-data-kind.html) | dateTimeKind | The kind that the dateTime should be interpreted as.
| [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html) | dateTimeFormat | The format of the dateTime.

#### Returns

| Type | Description
| --- | ---
| [Char](https://docs.microsoft.com/en-us/dotnet/api/system.char) | The first character in the string representation of the DateTime value.

### string MoveLeftWithPad([DateTime dateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind dateTimeKind](/reference/runtime/qsys-runtime/date-time-data-kind.html), [DateTimeFormat dateTimeFormat](/reference/datagate/datagate-common/date-time-format.html), [DateTimeSeparator dateTimeSeparator](/reference/runtime/qsys-runtime/date-time-separator.html), [string targetOperand](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

RPG's MOVEL. Moves left a DateTime to string with pad.

```cs
string MoveLeftWithPad(DateTime dateTime, DateTimeDataKind dateTimeKind, DateTimeFormat dateTimeFormat, DateTimeSeparator dateTimeSeparator, string targetOperand)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | dateTime | The date/time/timestamp value to move.
| [DateTimeDataKind](/reference/runtime/qsys-runtime/date-time-data-kind.html) | dateTimeKind | The DateTimeDataKind value that specifies whether it is a date, time, or timestamp.
| [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html) | dateTimeFormat | The DateTimeFormat of the value.
| [DateTimeSeparator](/reference/runtime/qsys-runtime/date-time-separator.html) | dateTimeSeparator | The DateTimeSeparator of the value.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | targetOperand | The string value that is the target of the MOVEL.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The string resulting from the MOVEL operation of the dateTime with the given format and separator into the targetOperand string.

### decimal MoveLeftWithPad([DateTime dateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind dateTimeKind](/reference/runtime/qsys-runtime/date-time-data-kind.html), [DateTimeFormat dateTimeFormat](/reference/datagate/datagate-common/date-time-format.html), [decimal targetOperand](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [int digits](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int decimals](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVEL. Moves left a DateTime to decimal with pad.

```cs
decimal MoveLeftWithPad(DateTime dateTime, DateTimeDataKind dateTimeKind, DateTimeFormat dateTimeFormat, decimal targetOperand, int digits, int decimals)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | dateTime | .NET DateTime value.
| [DateTimeDataKind](/reference/runtime/qsys-runtime/date-time-data-kind.html) | dateTimeKind | The kind that the dateTime should be interpreted as.
| [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html) | dateTimeFormat | The format of the dateTime.
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | targetOperand | The targetOperand decimal.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | digits | The number of digits in the targetOperand.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | decimals | The number of decimal places in the targetOperand.

#### Returns

| Type | Description
| --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | The resulting decimal value of the operation.

### short MoveLeftWithPad([DateTime dateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind dateTimeKind](/reference/runtime/qsys-runtime/date-time-data-kind.html), [DateTimeFormat dateTimeFormat](/reference/datagate/datagate-common/date-time-format.html), [short targetOperand](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVE. Moves right a datetime into a int2 (short) with pad.

```cs
short MoveLeftWithPad(DateTime dateTime, DateTimeDataKind dateTimeKind, DateTimeFormat dateTimeFormat, short targetOperand)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | dateTime | .NET DateTime value.
| [DateTimeDataKind](/reference/runtime/qsys-runtime/date-time-data-kind.html) | dateTimeKind | The kind that the dateTime should be interpreted as.
| [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html) | dateTimeFormat | The format of the dateTime.
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | targetOperand | The short value target of the operation.

#### Returns

| Type | Description
| --- | ---
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | The resulting short value of the operation.

### int MoveLeftWithPad([DateTime dateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind dateTimeKind](/reference/runtime/qsys-runtime/date-time-data-kind.html), [DateTimeFormat dateTimeFormat](/reference/datagate/datagate-common/date-time-format.html), [int targetOperand](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVEL. Moves left a datetime into a int4 (int).

```cs
int MoveLeftWithPad(DateTime dateTime, DateTimeDataKind dateTimeKind, DateTimeFormat dateTimeFormat, int targetOperand)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | dateTime | .NET DateTime value.
| [DateTimeDataKind](/reference/runtime/qsys-runtime/date-time-data-kind.html) | dateTimeKind | The kind that the dateTime should be interpreted as.
| [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html) | dateTimeFormat | The format of the dateTime.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetOperand | The int value target of the operation.

#### Returns

| Type | Description
| --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | The resulting int value of the operation.

### long MoveLeftWithPad([DateTime dateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind dateTimeKind](/reference/runtime/qsys-runtime/date-time-data-kind.html), [DateTimeFormat dateTimeFormat](/reference/datagate/datagate-common/date-time-format.html), [long targetOperand](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVEL. Moves left a datetime into a int8 (long).

```cs
long MoveLeftWithPad(DateTime dateTime, DateTimeDataKind dateTimeKind, DateTimeFormat dateTimeFormat, long targetOperand)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | dateTime | .NET DateTime value.
| [DateTimeDataKind](/reference/runtime/qsys-runtime/date-time-data-kind.html) | dateTimeKind | The kind that the dateTime should be interpreted as.
| [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html) | dateTimeFormat | The format of the dateTime.
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | targetOperand | The long value target of the operation.

#### Returns

| Type | Description
| --- | ---
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | The resulting long value of the operation.

### string MoveRight([DateTime dateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind dateTimeKind](/reference/runtime/qsys-runtime/date-time-data-kind.html), [DateTimeFormat dateTimeFormat](/reference/datagate/datagate-common/date-time-format.html), [DateTimeSeparator dateTimeSeparator](/reference/runtime/qsys-runtime/date-time-separator.html), [string targetOperand](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

RPG's MOVE. Moves right a DateTime to string.

```cs
string MoveRight(DateTime dateTime, DateTimeDataKind dateTimeKind, DateTimeFormat dateTimeFormat, DateTimeSeparator dateTimeSeparator, string targetOperand)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | dateTime | The date/time/timestamp value to move.
| [DateTimeDataKind](/reference/runtime/qsys-runtime/date-time-data-kind.html) | dateTimeKind | The DateTimeDataKind value that specifies whether it is a date, time, or timestamp.
| [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html) | dateTimeFormat | The DateTimeFormat of the value.
| [DateTimeSeparator](/reference/runtime/qsys-runtime/date-time-separator.html) | dateTimeSeparator | The DateTimeSeparator of the value.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | targetOperand | The string value that is the target of the MOVE.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The string resulting from the MOVE operation of the dateTime with the given format and separator into the targetOperand string.

### decimal MoveRight([DateTime dateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind dateTimeKind](/reference/runtime/qsys-runtime/date-time-data-kind.html), [DateTimeFormat dateTimeFormat](/reference/datagate/datagate-common/date-time-format.html), [decimal targetOperand](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [int digits](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int decimals](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVE. Moves right s DateTime to decimal.

```cs
decimal MoveRight(DateTime dateTime, DateTimeDataKind dateTimeKind, DateTimeFormat dateTimeFormat, decimal targetOperand, int digits, int decimals)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | dateTime | The date/time/timestamp value to move.
| [DateTimeDataKind](/reference/runtime/qsys-runtime/date-time-data-kind.html) | dateTimeKind | The DateTimeDataKind value that specifies whether it is a date, time, or timestamp.
| [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html) | dateTimeFormat | The DateTimeFormat of the value.
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | targetOperand | The decimal value that is the target of the MOVE.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | digits | The total number of digits in the decimal number.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | decimals | The number of decimal positions in the decimal number.

#### Returns

| Type | Description
| --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | The decimal number resulting from the MOVE operation of the dateTime with the given format and separator into the targetOperand number.

### short MoveRight([DateTime dateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind dateTimeKind](/reference/runtime/qsys-runtime/date-time-data-kind.html), [DateTimeFormat dateTimeFormat](/reference/datagate/datagate-common/date-time-format.html), [short targetOperand](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVE. Moves right a datetime into a int2 (short).

```cs
short MoveRight(DateTime dateTime, DateTimeDataKind dateTimeKind, DateTimeFormat dateTimeFormat, short targetOperand)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | dateTime | .NET DateTime value.
| [DateTimeDataKind](/reference/runtime/qsys-runtime/date-time-data-kind.html) | dateTimeKind | The kind that the dateTime should be interpreted as.
| [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html) | dateTimeFormat | The format of the dateTime.
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | targetOperand | The short value target of the operation.

#### Returns

| Type | Description
| --- | ---
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | The resulting short value of the operation.

### int MoveRight([DateTime dateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind dateTimeKind](/reference/runtime/qsys-runtime/date-time-data-kind.html), [DateTimeFormat dateTimeFormat](/reference/datagate/datagate-common/date-time-format.html), [int targetOperand](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVE. Moves right a datetime into a int4 (int).

```cs
int MoveRight(DateTime dateTime, DateTimeDataKind dateTimeKind, DateTimeFormat dateTimeFormat, int targetOperand)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | dateTime | .NET DateTime value.
| [DateTimeDataKind](/reference/runtime/qsys-runtime/date-time-data-kind.html) | dateTimeKind | The kind that the dateTime should be interpreted as.
| [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html) | dateTimeFormat | The format of the dateTime.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetOperand | The int value target of the operation.

#### Returns

| Type | Description
| --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | The resulting int value of the operation.

### long MoveRight([DateTime dateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind dateTimeKind](/reference/runtime/qsys-runtime/date-time-data-kind.html), [DateTimeFormat dateTimeFormat](/reference/datagate/datagate-common/date-time-format.html), [long targetOperand](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVE. Moves right a datetime into a int8 (long).

```cs
long MoveRight(DateTime dateTime, DateTimeDataKind dateTimeKind, DateTimeFormat dateTimeFormat, long targetOperand)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | dateTime | .NET DateTime value.
| [DateTimeDataKind](/reference/runtime/qsys-runtime/date-time-data-kind.html) | dateTimeKind | The kind that the dateTime should be interpreted as.
| [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html) | dateTimeFormat | The format of the dateTime.
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | targetOperand | The long value target of the operation.

#### Returns

| Type | Description
| --- | ---
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | The resulting long value of the operation.

### char MoveRightToChar([DateTime dateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind dateTimeKind](/reference/runtime/qsys-runtime/date-time-data-kind.html), [DateTimeFormat dateTimeFormat](/reference/datagate/datagate-common/date-time-format.html))

RPG's MOVE. Moves right a date, time, timestamp in the given format to a char value.

```cs
char MoveRightToChar(DateTime dateTime, DateTimeDataKind dateTimeKind, DateTimeFormat dateTimeFormat)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | dateTime | .NET DateTime value.
| [DateTimeDataKind](/reference/runtime/qsys-runtime/date-time-data-kind.html) | dateTimeKind | The kind that the dateTime should be interpreted as.
| [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html) | dateTimeFormat | The format of the dateTime.

#### Returns

| Type | Description
| --- | ---
| [Char](https://docs.microsoft.com/en-us/dotnet/api/system.char) | The last character in the string representation of the DateTime value.

### string MoveRightWithPad([DateTime dateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind dateTimeKind](/reference/runtime/qsys-runtime/date-time-data-kind.html), [DateTimeFormat dateTimeFormat](/reference/datagate/datagate-common/date-time-format.html), [DateTimeSeparator dateTimeSeparator](/reference/runtime/qsys-runtime/date-time-separator.html), [string targetOperand](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

RPG's MOVE. Moves right a DateTime to string with pad.

```cs
string MoveRightWithPad(DateTime dateTime, DateTimeDataKind dateTimeKind, DateTimeFormat dateTimeFormat, DateTimeSeparator dateTimeSeparator, string targetOperand)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | dateTime | The date/time/timestamp value to move.
| [DateTimeDataKind](/reference/runtime/qsys-runtime/date-time-data-kind.html) | dateTimeKind | The DateTimeDataKind value that specifies whether it is a date, time, or timestamp.
| [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html) | dateTimeFormat | The DateTimeFormat of the value.
| [DateTimeSeparator](/reference/runtime/qsys-runtime/date-time-separator.html) | dateTimeSeparator | The DateTimeSeparator of the value.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | targetOperand | The string value that is the target of the MOVE.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The string resulting from the MOVE operation of the dateTime with the given format and separator into the targetOperand string.

### decimal MoveRightWithPad([DateTime dateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind dateTimeKind](/reference/runtime/qsys-runtime/date-time-data-kind.html), [DateTimeFormat dateTimeFormat](/reference/datagate/datagate-common/date-time-format.html), [decimal targetOperand](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [int digits](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int decimals](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVE. Moves right a DateTime to decimal with pad.

```cs
decimal MoveRightWithPad(DateTime dateTime, DateTimeDataKind dateTimeKind, DateTimeFormat dateTimeFormat, decimal targetOperand, int digits, int decimals)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | dateTime | The date/time/timestamp value to move.
| [DateTimeDataKind](/reference/runtime/qsys-runtime/date-time-data-kind.html) | dateTimeKind | The DateTimeDataKind value that specifies whether it is a date, time, or timestamp.
| [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html) | dateTimeFormat | The DateTimeFormat of the value.
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | targetOperand | The decimal value that is the target of the MOVE.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | digits | The total number of digits in the decimal number.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | decimals | The number of decimal positions in the decimal number.

#### Returns

| Type | Description
| --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | The decimal number resulting from the MOVE operation of the dateTime with the given format and separator into the targetOperand number.

### short MoveRightWithPad([DateTime dateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind dateTimeKind](/reference/runtime/qsys-runtime/date-time-data-kind.html), [DateTimeFormat dateTimeFormat](/reference/datagate/datagate-common/date-time-format.html), [short targetOperand](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVE. Moves right a datetime into a int2 (short) with pad.

```cs
short MoveRightWithPad(DateTime dateTime, DateTimeDataKind dateTimeKind, DateTimeFormat dateTimeFormat, short targetOperand)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | dateTime | .NET DateTime value.
| [DateTimeDataKind](/reference/runtime/qsys-runtime/date-time-data-kind.html) | dateTimeKind | The kind that the dateTime should be interpreted as.
| [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html) | dateTimeFormat | The format of the dateTime.
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | targetOperand | The short value target of the operation.

#### Returns

| Type | Description
| --- | ---
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | The resulting short value of the operation.

### int MoveRightWithPad([DateTime dateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind dateTimeKind](/reference/runtime/qsys-runtime/date-time-data-kind.html), [DateTimeFormat dateTimeFormat](/reference/datagate/datagate-common/date-time-format.html), [int targetOperand](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVE. Moves right a datetime into a int4 (int) with pad.

```cs
int MoveRightWithPad(DateTime dateTime, DateTimeDataKind dateTimeKind, DateTimeFormat dateTimeFormat, int targetOperand)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | dateTime | .NET DateTime value.
| [DateTimeDataKind](/reference/runtime/qsys-runtime/date-time-data-kind.html) | dateTimeKind | The kind that the dateTime should be interpreted as.
| [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html) | dateTimeFormat | The format of the dateTime.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetOperand | The int value target of the operation.

#### Returns

| Type | Description
| --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | The resulting int value of the operation.

### long MoveRightWithPad([DateTime dateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind dateTimeKind](/reference/runtime/qsys-runtime/date-time-data-kind.html), [DateTimeFormat dateTimeFormat](/reference/datagate/datagate-common/date-time-format.html), [long targetOperand](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVE. Moves right a datetime into a int8 (long) with pad.

```cs
long MoveRightWithPad(DateTime dateTime, DateTimeDataKind dateTimeKind, DateTimeFormat dateTimeFormat, long targetOperand)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | dateTime | .NET DateTime value.
| [DateTimeDataKind](/reference/runtime/qsys-runtime/date-time-data-kind.html) | dateTimeKind | The kind that the dateTime should be interpreted as.
| [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html) | dateTimeFormat | The format of the dateTime.
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | targetOperand | The long value target of the operation.

#### Returns

| Type | Description
| --- | ---
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | The resulting long value of the operation.

### DateTime NormalizeYear([DateTime dateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime))

Turns a 4 digit year into a 2 digit year between 1940 and 2039

```cs
DateTime NormalizeYear(DateTime dateTime)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | dateTime | .NET DateTime value.

#### Returns

| Type | Description
| --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | .NET DateTime value.

### DateTime TimestampToDate([DateTime timestamp](https://docs.microsoft.com/en-us/dotnet/api/system.datetime))

Returns the Date portion of a timestamp.

```cs
DateTime TimestampToDate(DateTime timestamp)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | timestamp | The timestamp as a DateTime value.

#### Returns

| Type | Description
| --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | The Date portion as a DateTime value.

### DateTime TimestampToTime([DateTime timestamp](https://docs.microsoft.com/en-us/dotnet/api/system.datetime))

Returns the hours, minutes, and seconds of a timestamp.

```cs
DateTime TimestampToTime(DateTime timestamp)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | timestamp | The timestamp as a DateTime value.

#### Returns

| Type | Description
| --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | The Time portion in hours, minutes, and seconds as a DateTime value.

### DateTime TimestampToUSATime([DateTime timestamp](https://docs.microsoft.com/en-us/dotnet/api/system.datetime))

Returns the hours and minutes of a timestamp.

```cs
DateTime TimestampToUSATime(DateTime timestamp)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | timestamp | The timestamp as a DateTime value.

#### Returns

| Type | Description
| --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | The Time portion in hours and minutes only as a DateTime value.

### decimal ToFixedDecimal([DateTime dateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind dateTimeKind](/reference/runtime/qsys-runtime/date-time-data-kind.html), [DateTimeFormat dateTimeFormat](/reference/datagate/datagate-common/date-time-format.html), [int digits](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int decimals](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Converts a dateTime type, converts it to a decimal.

```cs
decimal ToFixedDecimal(DateTime dateTime, DateTimeDataKind dateTimeKind, DateTimeFormat dateTimeFormat, int digits, int decimals)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | dateTime | .NET DateTime value.
| [DateTimeDataKind](/reference/runtime/qsys-runtime/date-time-data-kind.html) | dateTimeKind | The Kind of the DateTime being converted.
| [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html) | dateTimeFormat | The Format of the DateTime being converted.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | digits | Number of digits in the targetOperand.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | decimals | Number of decimal places in the targetOperand.

#### Returns

| Type | Description
| --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | The decimal number that results from the conversion.

### decimal ToFixedDecimal([DateTime dateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind dateTimeKind](/reference/runtime/qsys-runtime/date-time-data-kind.html), [DateTimeFormat dateTimeFormat](/reference/datagate/datagate-common/date-time-format.html))

Converts a dateTime type to decimal.

```cs
decimal ToFixedDecimal(DateTime dateTime, DateTimeDataKind dateTimeKind, DateTimeFormat dateTimeFormat)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | dateTime | .NET DateTime value.
| [DateTimeDataKind](/reference/runtime/qsys-runtime/date-time-data-kind.html) | dateTimeKind | The Kind of the DateTime being converted.
| [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html) | dateTimeFormat | The Format of the DateTime being converted.

#### Returns

| Type | Description
| --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | The decimal number that results from the conversion.

### short ToInt16([DateTime dateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind dateTimeKind](/reference/runtime/qsys-runtime/date-time-data-kind.html), [DateTimeFormat dateTimeFormat](/reference/datagate/datagate-common/date-time-format.html), [bool throwOnOverflow](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Converts a dateTime type to int 16.

```cs
short ToInt16(DateTime dateTime, DateTimeDataKind dateTimeKind, DateTimeFormat dateTimeFormat, bool throwOnOverflow)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | dateTime | .NET DateTime value.
| [DateTimeDataKind](/reference/runtime/qsys-runtime/date-time-data-kind.html) | dateTimeKind | The Kind of the DateTime being converted.
| [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html) | dateTimeFormat | The Format of the DateTime being converted.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | throwOnOverflow | Default is false. Pass true if a runtime exception is desired when the conversion doesn't fit.

#### Returns

| Type | Description
| --- | ---
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | The Int16 number that results from the conversion.

### int ToInt32([DateTime dateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind dateTimeKind](/reference/runtime/qsys-runtime/date-time-data-kind.html), [DateTimeFormat dateTimeFormat](/reference/datagate/datagate-common/date-time-format.html), [bool throwOnOverflow](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Converts a dateTime type to int 32.

```cs
int ToInt32(DateTime dateTime, DateTimeDataKind dateTimeKind, DateTimeFormat dateTimeFormat, bool throwOnOverflow)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | dateTime | .NET DateTime value.
| [DateTimeDataKind](/reference/runtime/qsys-runtime/date-time-data-kind.html) | dateTimeKind | The Kind of the DateTime being converted.
| [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html) | dateTimeFormat | The Format of the DateTime being converted.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | throwOnOverflow | Default is false. Pass true if a runtime exception is desired when the conversion doesn't fit.

#### Returns

| Type | Description
| --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | The Int32 number that results from the conversion.

### long ToInt64([DateTime dateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind dateTimeKind](/reference/runtime/qsys-runtime/date-time-data-kind.html), [DateTimeFormat dateTimeFormat](/reference/datagate/datagate-common/date-time-format.html), [bool throwOnOverflow](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Converts a dateTime type to int 64.

```cs
long ToInt64(DateTime dateTime, DateTimeDataKind dateTimeKind, DateTimeFormat dateTimeFormat, bool throwOnOverflow)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | dateTime | .NET DateTime value.
| [DateTimeDataKind](/reference/runtime/qsys-runtime/date-time-data-kind.html) | dateTimeKind | The Kind of the DateTime being converted.
| [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html) | dateTimeFormat | The Format of the DateTime being converted.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | throwOnOverflow | Default is false. Pass true if a runtime exception is desired when the conversion doesn't fit.

#### Returns

| Type | Description
| --- | ---
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | The Int64 number that results from the conversion.

### string ToString([DateTime dateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind dateTimeKind](/reference/runtime/qsys-runtime/date-time-data-kind.html), [DateTimeFormat dateTimeFormat](/reference/datagate/datagate-common/date-time-format.html), [DateTimeSeparator dateTimeSeparator](/reference/runtime/qsys-runtime/date-time-separator.html))

Converts a DateTime with the specified Kind and Format to a string using the specified separator.

```cs
string ToString(DateTime dateTime, DateTimeDataKind dateTimeKind, DateTimeFormat dateTimeFormat, DateTimeSeparator dateTimeSeparator)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | dateTime | .NET DateTime value.
| [DateTimeDataKind](/reference/runtime/qsys-runtime/date-time-data-kind.html) | dateTimeKind | The Kind of the DateTime being converted.
| [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html) | dateTimeFormat | The Format of the DateTime being converted.
| [DateTimeSeparator](/reference/runtime/qsys-runtime/date-time-separator.html) | dateTimeSeparator | The separator to use in the returned string.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | A string representation of a DateTime in the given format using the specified separator.
