---
title: "IntegerMethods class          | QSYS API Reference Guide"
description: "Contains extension methods for handling RPG operations and conversions for Integer (2, 4, and 8-byte long) values. "
last_modified_at: 2024-08-09T16:18:25Z
---

Contains extension methods for handling RPG operations and conversions for Integer (2, 4, and 8-byte long) values.

**Namespace:** ASNA.QSys.Runtime
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>

## Methods

| Signature | Description |
| --- | --- |
| [EditWord](#string-editwordshort-num-string-editwordstring)([Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | EditWord summary. 
| [EditWord](#string-editwordint-num-string-editwordstring)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | EditWord summary. 
| [EditWord](#string-editwordlong-num-string-editwordstring)([Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | EditWord summary.
| [MoveLeft](#datetime-moveleftshort-num-datetime-datetime-datetimedatakind-datetimekind-datetimeformat-datetimeformat)([Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16), [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind](/reference/runtime/qsys-runtime/date-time-data-kind.html), [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html)) | RPG's MOVEL. Moves left a int2 (short) to a datetime with given format and separators.
| [MoveLeft](#datetime-moveleftshort-num-ifixeddatetime-datetime)([Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16), [IFixedDateTime](/reference/runtime/qsys-runtime/i-fixed-date-time.html)) | RPG's MOVEL. Moves left a int2 (short) to a datetime with given format and separators.
| [MoveLeft](#datetime-moveleftint-num-datetime-datetime-datetimedatakind-datetimekind-datetimeformat-datetimeformat)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind](/reference/runtime/qsys-runtime/date-time-data-kind.html), [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html)) | RPG's MOVEL. Moves left a int4 (int) to a datetime with given format and separators.
| [MoveLeft](#datetime-moveleftint-num-ifixeddatetime-datetime)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [IFixedDateTime](/reference/runtime/qsys-runtime/i-fixed-date-time.html)) | RPG's MOVEL. Moves left a int4 (int) to a datetime with given format and separators.
| [MoveLeft](#datetime-moveleftlong-num-datetime-datetime-datetimedatakind-datetimekind-datetimeformat-datetimeformat)([Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64), [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind](/reference/runtime/qsys-runtime/date-time-data-kind.html), [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html)) | RPG's MOVE. Moves right a int8 (long) to a datetime with given format and separators.
| [MoveLeft](#datetime-moveleftlong-num-ifixeddatetime-datetime)([Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64), [IFixedDateTime](/reference/runtime/qsys-runtime/i-fixed-date-time.html)) | RPG's MOVE. Moves right a int8 (long) to a datetime with given format and separators.
| [MoveLeft](#decimal-moveleftshort-num-decimal-targetoperand-int-targetoperanddig-int-targetoperanddec)([Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16), [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's MOVEL. Moves left an int2 (short) to a decimal.
| [MoveLeft](#decimal-moveleftint-num-decimal-targetoperand-int-targetoperanddig-int-targetoperanddec)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's MOVEL. Moves left an int4 (int) to a decimal.
| [MoveLeft](#decimal-moveleftlong-num-decimal-targetoperand-int-targetoperanddig-int-targetoperanddec)([Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64), [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's MOVEL. Moves left an int8 (long) to a decimal.
| [MoveLeft](#string-moveleftshort-num-string-targetoperand)([Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | RPG's MOVEL. Moves left int2 (short) to a string.
| [MoveLeft](#string-moveleftint-num-string-targetoperand)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | RPG's MOVEL. Moves left int4 (int) to a string.
| [MoveLeft](#string-moveleftlong-num-string-targetoperand)([Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | RPG's MOVEL. Moves left int8 (long) to a string.
| [MoveLeft](#int-moveleftshort-num-int-targetoperand)([Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's MOVEL. Moves left an int2 (short) to an int4 (int).
| [MoveLeft](#long-moveleftshort-num-long-targetoperand)([Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16), [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64)) | RPG's MOVEL. Moves left an int2 (short) to an int8 (long).
| [MoveLeft](#long-moveleftint-num-long-targetoperand)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64)) | RPG's MOVEL. Moves left an int4 (int) to an int8 (long).
| [MoveLeft](#short-moveleftint-num-short-targetoperand)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16)) | RPG's MOVEL. Moves left an int4 (int) to an int2 (short).
| [MoveLeft](#short-moveleftlong-num-short-targetoperand)([Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64), [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16)) | RPG's MOVEL. Moves left an int8 (long) to an int2 (short).
| [MoveLeft](#int-moveleftlong-num-int-targetoperand)([Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's MOVEL. Moves left an int8 (long) to an int4 (int).
| [MoveLeft](#short-moveleftshort-num-short-targetoperand)([Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16), [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16)) | RPG's MOVEL. Moves left an int2 (short) to an int2 (short), this is actually the same as assignment.
| [MoveLeft](#int-moveleftint-num-int-targetoperand)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's MOVEL. Moves left an int4 (int) to an int4 (int), this is actually the same as assignment.
| [MoveLeft](#long-moveleftlong-num-long-targetoperand)([Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64), [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64)) | RPG's MOVEL. Moves left an int8 (long) to an int8 (long), this is actually the same as assignment.
| [MoveLeftToChar](#char-movelefttocharshort-num)([Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16)) | RPG's MOVEL. Moves left a short into a character.
| [MoveLeftToChar](#char-movelefttocharint-num)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's MOVEL. Moves left a int into a character.
| [MoveLeftToChar](#char-movelefttocharlong-num)([Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64)) | RPG's MOVEL. Moves left a long into a character.
| [MoveLeftWithPad](#datetime-moveleftwithpadshort-num-datetime-datetime-datetimedatakind-datetimekind-datetimeformat-datetimeformat)([Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16), [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind](/reference/runtime/qsys-runtime/date-time-data-kind.html), [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html)) | RPG's MOVEL. Moves left a int2 (short) to a datetime with given format and separators with pad.
| [MoveLeftWithPad](#datetime-moveleftwithpadshort-num-ifixeddatetime-datetime)([Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16), [IFixedDateTime](/reference/runtime/qsys-runtime/i-fixed-date-time.html)) | RPG's MOVEL. Moves left a int2 (short) to a datetime with given format and separators with pad.
| [MoveLeftWithPad](#datetime-moveleftwithpadint-num-datetime-datetime-datetimedatakind-datetimekind-datetimeformat-datetimeformat)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind](/reference/runtime/qsys-runtime/date-time-data-kind.html), [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html)) | RPG's MOVEL. Moves left a int4 (int) to a datetime with given format and separators with pad.
| [MoveLeftWithPad](#datetime-moveleftwithpadint-num-ifixeddatetime-datetime)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [IFixedDateTime](/reference/runtime/qsys-runtime/i-fixed-date-time.html)) | RPG's MOVEL. Moves left a int4 (int) to a datetime with given format and separators with pad.
| [MoveLeftWithPad](#datetime-moveleftwithpadlong-num-datetime-datetime-datetimedatakind-datetimekind-datetimeformat-datetimeformat)([Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64), [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind](/reference/runtime/qsys-runtime/date-time-data-kind.html), [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html)) | RPG's MOVE. Moves right a int8 (long) to a datetime with given format and separators with pad.
| [MoveLeftWithPad](#datetime-moveleftwithpadlong-num-ifixeddatetime-datetime)([Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64), [IFixedDateTime](/reference/runtime/qsys-runtime/i-fixed-date-time.html)) | RPG's MOVE. Moves right a int8 (long) to a datetime with given format and separators with pad.
| [MoveLeftWithPad](#decimal-moveleftwithpadshort-num-decimal-targetoperand-int-targetoperanddig-int-targetoperanddec)([Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16), [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's MOVEL. Moves left an int2 (short) to a decimal with pad.
| [MoveLeftWithPad](#decimal-moveleftwithpadint-num-decimal-targetoperand-int-targetoperanddig-int-targetoperanddec)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's MOVEL. Moves left an int4 (int) to a decimal with pad.
| [MoveLeftWithPad](#decimal-moveleftwithpadlong-num-decimal-targetoperand-int-targetoperanddig-int-targetoperanddec)([Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64), [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's MOVEL. Moves left an int8 (long) to a decimal with pad.
| [MoveLeftWithPad](#string-moveleftwithpadshort-num-string-targetoperand)([Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | RPG's MOVEL. Moves left int2 (short) to a string with pad.
| [MoveLeftWithPad](#string-moveleftwithpadint-num-string-targetoperand)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | RPG's MOVEL. Moves left int4 (int) to a string with pad.
| [MoveLeftWithPad](#string-moveleftwithpadlong-num-string-targetoperand)([Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | RPG's MOVEL. Moves left int8 (long) to a string with pad.
| [MoveLeftWithPad](#int-moveleftwithpadshort-num-int-targetoperand)([Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's MOVEL. Moves left an int2 (short) to an int4 (int) with pad.
| [MoveLeftWithPad](#long-moveleftwithpadshort-num-long-targetoperand)([Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16), [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64)) | RPG's MOVEL. Moves left an int2 (short) to an int8 (long) with pad.
| [MoveLeftWithPad](#long-moveleftwithpadint-num-long-targetoperand)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64)) | RPG's MOVEL. Moves left an int4 (int) to an int8 (long) with pad.
| [MoveRight](#datetime-moverightshort-num-datetime-datetime-datetimedatakind-datetimekind-datetimeformat-datetimeformat)([Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16), [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind](/reference/runtime/qsys-runtime/date-time-data-kind.html), [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html)) | RPG's MOVE. Moves right a int2 (short) to a datetime with given format and separators.
| [MoveRight](#datetime-moverightshort-num-ifixeddatetime-datetime)([Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16), [IFixedDateTime](/reference/runtime/qsys-runtime/i-fixed-date-time.html)) | RPG's MOVE. Moves right a int2 (short) to a datetime with given format and separators.
| [MoveRight](#datetime-moverightint-num-datetime-datetime-datetimedatakind-datetimekind-datetimeformat-datetimeformat)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind](/reference/runtime/qsys-runtime/date-time-data-kind.html), [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html)) | RPG's MOVE. Moves right a int4 (int) to a datetime with given format and separators.
| [MoveRight](#datetime-moverightint-num-ifixeddatetime-datetime)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [IFixedDateTime](/reference/runtime/qsys-runtime/i-fixed-date-time.html)) | RPG's MOVE. Moves right a int4 (int) to a datetime with given format and separators.
| [MoveRight](#datetime-moverightlong-num-datetime-datetime-datetimedatakind-datetimekind-datetimeformat-datetimeformat)([Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64), [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind](/reference/runtime/qsys-runtime/date-time-data-kind.html), [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html)) | RPG's MOVE. Moves right a int8 (long) to a datetime with given format and separators.
| [MoveRight](#datetime-moverightlong-num-ifixeddatetime-datetime)([Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64), [IFixedDateTime](/reference/runtime/qsys-runtime/i-fixed-date-time.html)) | RPG's MOVE. Moves right a int8 (long) to a datetime with given format and separators.
| [MoveRight](#decimal-moverightshort-num-decimal-targetoperand-int-targetoperanddig-int-targetoperanddec)([Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16), [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's MOVE. Moves right an int2 (short) to a decimal.
| [MoveRight](#decimal-moverightint-num-decimal-targetoperand-int-targetoperanddig-int-targetoperanddec)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's MOVE. Moves right an int4 (int) to a decimal.
| [MoveRight](#decimal-moverightlong-num-decimal-targetoperand-int-targetoperanddig-int-targetoperanddec)([Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64), [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's MOVE. Moves right an int8 (long) to a decimal.
| [MoveRight](#string-moverightshort-num-string-targetoperand)([Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | RPG's MOVE. Moves right int2 (short) to a string.
| [MoveRight](#string-moverightint-num-string-targetoperand)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | RPG's MOVE. Moves right int4 (int) to a string.
| [MoveRight](#string-moverightlong-num-string-targetoperand)([Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | RPG's MOVE. Moves right int8 (long) to a string.
| [MoveRight](#int-moverightshort-num-int-targetoperand)([Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's MOVE. Moves right an int2 (short) to an int4 (int).
| [MoveRight](#long-moverightshort-num-long-targetoperand)([Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16), [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64)) | RPG's MOVE. Moves right an int2 (short) to an int8 (long).
| [MoveRight](#long-moverightint-num-long-targetoperand)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64)) | RPG's MOVE. Moves right an int4 (int) to an int8 (long).
| [MoveRight](#short-moverightint-num-short-targetoperand)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16)) | RPG's MOVE. Moves right an int4 (int) to an int2 (short).
| [MoveRight](#short-moverightlong-num-short-targetoperand)([Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64), [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16)) | RPG's MOVE. Moves right an int8 (long) to an int2 (short).
| [MoveRight](#int-moverightlong-num-int-targetoperand)([Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's MOVE. Moves right an int8 (long) to an int4 (int).
| [MoveRight](#short-moverightshort-num-short-targetoperand)([Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16), [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16)) | RPG's MOVE. Moves right an int2 (short) to an int2 (short), this is actually the same as assignment.
| [MoveRight](#int-moverightint-num-int-targetoperand)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's MOVE. Moves right an int4 (int) to an int4 (int), this is actually the same as assignment.
| [MoveRight](#long-moverightlong-num-long-targetoperand)([Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64), [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64)) | RPG's MOVE. Moves right an int8 (long) to an int8 (long), this is actually the same as assignment.
| [MoveRightToChar](#char-moverighttocharshort-num)([Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16)) | RPG's MOVE. Moves right a short into a character.
| [MoveRightToChar](#char-moverighttocharint-num)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's MOVE. Moves right a int into a character.
| [MoveRightToChar](#char-moverighttocharlong-num)([Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64)) | RPG's MOVE. Moves right a long into a character.
| [MoveRightWithPad](#datetime-moverightwithpadshort-num-datetime-datetime-datetimedatakind-datetimekind-datetimeformat-datetimeformat)([Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16), [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind](/reference/runtime/qsys-runtime/date-time-data-kind.html), [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html)) | RPG's MOVE. Moves right a int2 (short) to a datetime with given format and separators with pad.
| [MoveRightWithPad](#datetime-moverightwithpadshort-num-ifixeddatetime-datetime)([Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16), [IFixedDateTime](/reference/runtime/qsys-runtime/i-fixed-date-time.html)) | RPG's MOVE. Moves right a int2 (short) to a datetime with given format and separators with pad.
| [MoveRightWithPad](#datetime-moverightwithpadint-num-datetime-datetime-datetimedatakind-datetimekind-datetimeformat-datetimeformat)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind](/reference/runtime/qsys-runtime/date-time-data-kind.html), [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html)) | RPG's MOVE. Moves right a int4 (int) to a datetime with given format and separators with pad.
| [MoveRightWithPad](#datetime-moverightwithpadint-num-ifixeddatetime-datetime)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [IFixedDateTime](/reference/runtime/qsys-runtime/i-fixed-date-time.html)) | RPG's MOVE. Moves right a int4 (int) to a datetime with given format and separators with pad.
| [MoveRightWithPad](#datetime-moverightwithpadlong-num-datetime-datetime-datetimedatakind-datetimekind-datetimeformat-datetimeformat)([Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64), [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind](/reference/runtime/qsys-runtime/date-time-data-kind.html), [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html)) | RPG's MOVE. Moves right a int8 (long) to a datetime with given format and separators with pad.
| [MoveRightWithPad](#datetime-moverightwithpadlong-num-ifixeddatetime-datetime)([Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64), [IFixedDateTime](/reference/runtime/qsys-runtime/i-fixed-date-time.html)) | RPG's MOVE. Moves right a int8 (long) to a datetime with given format and separators with pad.
| [MoveRightWithPad](#decimal-moverightwithpadshort-num-decimal-targetoperand-int-targetoperanddig-int-targetoperanddec)([Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16), [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's MOVE. Moves right an int2 (short) to a decimal with pad.
| [MoveRightWithPad](#decimal-moverightwithpadint-num-decimal-targetoperand-int-targetoperanddig-int-targetoperanddec)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's MOVE. Moves right an int4 (int) to a decimal with pad.
| [MoveRightWithPad](#decimal-moverightwithpadlong-num-decimal-targetoperand-int-targetoperanddig-int-targetoperanddec)([Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64), [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's MOVE. Moves right an int8 (long) to a decimal with pad.
| [MoveRightWithPad](#string-moverightwithpadshort-num-string-targetoperand)([Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | RPG's MOVE. Moves right int2 (short) to a string with pad.
| [MoveRightWithPad](#string-moverightwithpadint-num-string-targetoperand)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | RPG's MOVE. Moves right int4 (int) to a string with pad.
| [MoveRightWithPad](#string-moverightwithpadlong-num-string-targetoperand)([Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | RPG's MOVE. Moves right int8 (long) to a string with pad.
| [MoveRightWithPad](#int-moverightwithpadshort-num-int-targetoperand)([Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's MOVE. Moves right an int2 (short) to an int4 (int) with pad.
| [MoveRightWithPad](#long-moverightwithpadshort-num-long-targetoperand)([Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16), [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64)) | RPG's MOVE. Moves right an int2 (short) to an int8 (long) with pad.
| [MoveRightWithPad](#long-moverightwithpadint-num-long-targetoperand)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64)) | RPG's MOVE. Moves right an int4 (int) to an int8 (long) with pad.
| [Sum](#short-sumint16--array)([Int16\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.int16)) | Returns the added values of each element in the array.
| [Sum](#int-sumint32--array)([Int32\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Returns the added values of each element in the array.
| [Sum](#long-sumint64--array)([Int64\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.int64)) | Returns the added values of each element in the array.
| [TestTime](#bool-testtimeshort-num-datetimedatakind-kind-datetimeformat-format)([Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16), [DateTimeDataKind](/reference/runtime/qsys-runtime/date-time-data-kind.html), [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html)) | Tests whether a short contains a valid date/time/timestamp value. 
| [TestTime](#bool-testtimeint-num-datetimedatakind-kind-datetimeformat-format)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [DateTimeDataKind](/reference/runtime/qsys-runtime/date-time-data-kind.html), [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html)) | Tests whether an int number contains a valid date/time/timestamp value. 
| [TestTime](#bool-testtimelong-num-datetimedatakind-kind-datetimeformat-format)([Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64), [DateTimeDataKind](/reference/runtime/qsys-runtime/date-time-data-kind.html), [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html)) | Tests whether a long number contains a valid date/time/timestamp value. 
| [ToDate](#datetime-todateint-source-datetimeformat-format)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html)) | ToDate summary.
| [ToDate](#datetime-todateshort-source-datetimeformat-format)([Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16), [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html)) | ToDate summary.
| [ToDate](#datetime-todatelong-source-datetimeformat-format)([Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64), [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html)) | ToDate summary.
| [ToFixedDecimal](#decimal-tofixeddecimalint-num-int-digits-int-decimals)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Adjusts the digits and decimal positions of a fixed decimal number using Away From Zero rounding.
| [ToFixedDecimalRounded](#decimal-tofixeddecimalroundedint-num-int-digits-int-decimals)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Adjusts the digits and decimal positions of a fixed decimal number using Away From Zero rounding.
| [ToStringByte](#string-tostringbytebyte-num)([Byte](https://docs.microsoft.com/en-us/dotnet/api/system.byte)) | Returns as a string the char equivalent of a byte number.
| [ToStringInt](#string-tostringintint-num)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Returns as a string the char equivalent of a int number.
| [ToStringLong](#string-tostringlonglong-num)([Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64)) | Returns as a string the char equivalentof a long number.
| [ToStringShort](#string-tostringshortshort-num)([Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16)) | Returns as a string the char equivalent of a short number.
| [ToTime](#datetime-totimeint-source-datetimeformat-format)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html)) | ToTime summary.
| [ToTime](#datetime-totimeshort-source-datetimeformat-format)([Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16), [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html)) | ToTime summary.
| [ToTime](#datetime-totimelong-source-datetimeformat-format)([Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64), [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html)) | ToTime summary.
| [ToTimestamp](#datetime-totimestampint-source)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | ToTimestamp summary.
| [ToTimestamp](#datetime-totimestampshort-source)([Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16)) | ToTimestamp summary.
| [ToTimestamp](#datetime-totimestamplong-source)([Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64)) | ToTimestamp summary.

### string EditWord([short num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [string editwordString](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

EditWord summary. 

```cs
string EditWord(short num, string editwordString)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | num | EditWord num param.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | editwordString | EditWord editwordString param.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | EditWord returns.

### string EditWord([int num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [string editwordString](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

EditWord summary. 

```cs
string EditWord(int num, string editwordString)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | num | EditWord num param.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | editwordString | EditWord editwordString param.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | EditWord returns.

### string EditWord([long num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [string editwordString](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

EditWord summary.

```cs
string EditWord(long num, string editwordString)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | num | EditWord num param.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | editwordString | EditWord editwordString param.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | EditWord returns.

### DateTime MoveLeft([short num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [DateTime dateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind dateTimeKind](/reference/runtime/qsys-runtime/date-time-data-kind.html), [DateTimeFormat dateTimeFormat](/reference/datagate/datagate-common/date-time-format.html))

RPG's MOVEL. Moves left a int2 (short) to a datetime with given format and separators.

```cs
DateTime MoveLeft(short num, DateTime dateTime, DateTimeDataKind dateTimeKind, DateTimeFormat dateTimeFormat)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | num | short value of the source number.
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | dateTime | Date, Time, Timestamp.
| [DateTimeDataKind](/reference/runtime/qsys-runtime/date-time-data-kind.html) | dateTimeKind | DateTime Kind.
| [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html) | dateTimeFormat | DateTime Format.

#### Returns

| Type | Description
| --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | The resulting DateTime value of the operation.

### DateTime MoveLeft([short num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [IFixedDateTime dateTime](/reference/runtime/qsys-runtime/i-fixed-date-time.html))

RPG's MOVEL. Moves left a int2 (short) to a datetime with given format and separators.

```cs
DateTime MoveLeft(short num, IFixedDateTime dateTime)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | num | short value of the source number.
| [IFixedDateTime](/reference/runtime/qsys-runtime/i-fixed-date-time.html) | dateTime | Date, Time, Timestamp.

#### Returns

| Type | Description
| --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | The resulting DateTime value of the operation.

### DateTime MoveLeft([int num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [DateTime dateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind dateTimeKind](/reference/runtime/qsys-runtime/date-time-data-kind.html), [DateTimeFormat dateTimeFormat](/reference/datagate/datagate-common/date-time-format.html))

RPG's MOVEL. Moves left a int4 (int) to a datetime with given format and separators.

```cs
DateTime MoveLeft(int num, DateTime dateTime, DateTimeDataKind dateTimeKind, DateTimeFormat dateTimeFormat)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | num | int value of the source number.
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | dateTime | Date, Time, Timestamp.
| [DateTimeDataKind](/reference/runtime/qsys-runtime/date-time-data-kind.html) | dateTimeKind | DateTime Kind.
| [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html) | dateTimeFormat | DateTime Format.

#### Returns

| Type | Description
| --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | The resulting DateTime value of the operation.

### DateTime MoveLeft([int num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [IFixedDateTime dateTime](/reference/runtime/qsys-runtime/i-fixed-date-time.html))

RPG's MOVEL. Moves left a int4 (int) to a datetime with given format and separators.

```cs
DateTime MoveLeft(int num, IFixedDateTime dateTime)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | num | int value of the source number.
| [IFixedDateTime](/reference/runtime/qsys-runtime/i-fixed-date-time.html) | dateTime | Date, Time, Timestamp.

#### Returns

| Type | Description
| --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | The resulting DateTime value of the operation.

### DateTime MoveLeft([long num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [DateTime dateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind dateTimeKind](/reference/runtime/qsys-runtime/date-time-data-kind.html), [DateTimeFormat dateTimeFormat](/reference/datagate/datagate-common/date-time-format.html))

RPG's MOVE. Moves right a int8 (long) to a datetime with given format and separators.

```cs
DateTime MoveLeft(long num, DateTime dateTime, DateTimeDataKind dateTimeKind, DateTimeFormat dateTimeFormat)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | num | long value of the source number.
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | dateTime | Date, Time, Timestamp.
| [DateTimeDataKind](/reference/runtime/qsys-runtime/date-time-data-kind.html) | dateTimeKind | DateTime Kind.
| [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html) | dateTimeFormat | DateTime Format.

#### Returns

| Type | Description
| --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | The resulting DateTime value of the operation.

### DateTime MoveLeft([long num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [IFixedDateTime dateTime](/reference/runtime/qsys-runtime/i-fixed-date-time.html))

RPG's MOVE. Moves right a int8 (long) to a datetime with given format and separators.

```cs
DateTime MoveLeft(long num, IFixedDateTime dateTime)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | num | long value of the source number.
| [IFixedDateTime](/reference/runtime/qsys-runtime/i-fixed-date-time.html) | dateTime | Date, Time, Timestamp.

#### Returns

| Type | Description
| --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | The resulting DateTime value of the operation.

### decimal MoveLeft([short num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [decimal targetOperand](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [int targetOperandDig](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int targetOperandDec](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVEL. Moves left an int2 (short) to a decimal.

```cs
decimal MoveLeft(short num, decimal targetOperand, int targetOperandDig, int targetOperandDec)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | num | short value of the source number.
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | targetOperand | targetOperand represents what is currently in the target.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetOperandDig | number of digits in the targetOperand.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetOperandDec | number of decimal places in the targetOperand.

#### Returns

| Type | Description
| --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | The resulting decimal value of the operation.

### decimal MoveLeft([int num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [decimal targetOperand](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [int targetOperandDig](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int targetOperandDec](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVEL. Moves left an int4 (int) to a decimal.

```cs
decimal MoveLeft(int num, decimal targetOperand, int targetOperandDig, int targetOperandDec)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | num | int value of the source number.
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | targetOperand | targetOperand represents what is currently in the target.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetOperandDig | number of digits in the targetOperand.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetOperandDec | number of decimal places in the targetOperand.

#### Returns

| Type | Description
| --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | The resulting decimal value of the operation.

### decimal MoveLeft([long num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [decimal targetOperand](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [int targetOperandDig](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int targetOperandDec](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVEL. Moves left an int8 (long) to a decimal.

```cs
decimal MoveLeft(long num, decimal targetOperand, int targetOperandDig, int targetOperandDec)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | num | long value of the source number.
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | targetOperand | targetOperand represents what is currently in the target.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetOperandDig | number of digits in the targetOperand.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetOperandDec | number of decimal places in the targetOperand.

#### Returns

| Type | Description
| --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | The resulting decimal value of the operation.

### string MoveLeft([short num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [string targetOperand](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

RPG's MOVEL. Moves left int2 (short) to a string.

```cs
string MoveLeft(short num, string targetOperand)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | num | short value of the source number.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | targetOperand | targetOperand represents what is currently in the target.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The resulting string value of the operation.

### string MoveLeft([int num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [string targetOperand](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

RPG's MOVEL. Moves left int4 (int) to a string.

```cs
string MoveLeft(int num, string targetOperand)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | num | int value of the source number.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | targetOperand | targetOperand represents what is currently in the target.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The resulting string value of the operation.

### string MoveLeft([long num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [string targetOperand](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

RPG's MOVEL. Moves left int8 (long) to a string.

```cs
string MoveLeft(long num, string targetOperand)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | num | long value of the source number.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | targetOperand | targetOperand represents what is currently in the target.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The resulting string value of the operation.

### int MoveLeft([short num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int targetOperand](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVEL. Moves left an int2 (short) to an int4 (int).

```cs
int MoveLeft(short num, int targetOperand)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | num | short value of the source.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetOperand | targetOperand represents what is currently in the target.

#### Returns

| Type | Description
| --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | The resulting int value of the operation.

### long MoveLeft([short num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [long targetOperand](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVEL. Moves left an int2 (short) to an int8 (long).

```cs
long MoveLeft(short num, long targetOperand)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | num | long value of the source.
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | targetOperand | targetOperand represents what is currently in the target.

#### Returns

| Type | Description
| --- | ---
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | The resulting long value of the operation.

### long MoveLeft([int num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [long targetOperand](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVEL. Moves left an int4 (int) to an int8 (long).

```cs
long MoveLeft(int num, long targetOperand)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | num | int value of the source.
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | targetOperand | targetOperand represents what is currently in the target.

#### Returns

| Type | Description
| --- | ---
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | The resulting long value of the operation.

### short MoveLeft([int num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [short targetOperand](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVEL. Moves left an int4 (int) to an int2 (short).

```cs
short MoveLeft(int num, short targetOperand)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | num | int value of the source.
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | targetOperand | targetOperand represents what is currently in the target.

#### Returns

| Type | Description
| --- | ---
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | The resulting short value of the operation.

### short MoveLeft([long num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [short targetOperand](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVEL. Moves left an int8 (long) to an int2 (short).

```cs
short MoveLeft(long num, short targetOperand)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | num | long value of the source.
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | targetOperand | targetOperand represents what is currently in the target.

#### Returns

| Type | Description
| --- | ---
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | The resulting short value of the operation.

### int MoveLeft([long num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int targetOperand](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVEL. Moves left an int8 (long) to an int4 (int).

```cs
int MoveLeft(long num, int targetOperand)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | num | long value of the source.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetOperand | targetOperand represents what is currently in the target.

#### Returns

| Type | Description
| --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | The resulting int value of the operation.

### short MoveLeft([short num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [short targetOperand](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVEL. Moves left an int2 (short) to an int2 (short), this is actually the same as assignment.

```cs
short MoveLeft(short num, short targetOperand)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | num | short value of the source.
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | targetOperand | targetOperand represents what is currently in the target.

#### Returns

| Type | Description
| --- | ---
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | The resulting short value of the operation.

### int MoveLeft([int num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int targetOperand](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVEL. Moves left an int4 (int) to an int4 (int), this is actually the same as assignment.

```cs
int MoveLeft(int num, int targetOperand)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | num | int value of the source.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetOperand | targetOperand represents what is currently in the target.

#### Returns

| Type | Description
| --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | The resulting int value of the operation.

### long MoveLeft([long num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [long targetOperand](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVEL. Moves left an int8 (long) to an int8 (long), this is actually the same as assignment.

```cs
long MoveLeft(long num, long targetOperand)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | num | long value of the source.
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | targetOperand | targetOperand represents what is currently in the target.

#### Returns

| Type | Description
| --- | ---
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | The resulting long value of the operation.

### char MoveLeftToChar([short num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVEL. Moves left a short into a character.

```cs
char MoveLeftToChar(short num)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | num | The short value to move.

#### Returns

| Type | Description
| --- | ---
| [Char](https://docs.microsoft.com/en-us/dotnet/api/system.char) | The leftmost byte of the short value as a character.

### char MoveLeftToChar([int num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVEL. Moves left a int into a character.

```cs
char MoveLeftToChar(int num)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | num | The int value to move.

#### Returns

| Type | Description
| --- | ---
| [Char](https://docs.microsoft.com/en-us/dotnet/api/system.char) | The leftmost byte of the int value as a character.

### char MoveLeftToChar([long num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVEL. Moves left a long into a character.

```cs
char MoveLeftToChar(long num)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | num | The long value to move.

#### Returns

| Type | Description
| --- | ---
| [Char](https://docs.microsoft.com/en-us/dotnet/api/system.char) | The leftmost byte of the long value as a character.

### DateTime MoveLeftWithPad([short num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [DateTime dateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind dateTimeKind](/reference/runtime/qsys-runtime/date-time-data-kind.html), [DateTimeFormat dateTimeFormat](/reference/datagate/datagate-common/date-time-format.html))

RPG's MOVEL. Moves left a int2 (short) to a datetime with given format and separators with pad.

```cs
DateTime MoveLeftWithPad(short num, DateTime dateTime, DateTimeDataKind dateTimeKind, DateTimeFormat dateTimeFormat)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | num | short value of the source number.
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | dateTime | Date, Time, Timestamp.
| [DateTimeDataKind](/reference/runtime/qsys-runtime/date-time-data-kind.html) | dateTimeKind | DateTime Kind.
| [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html) | dateTimeFormat | DateTime Format.

#### Returns

| Type | Description
| --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | The resulting DateTime value of the operation.

### DateTime MoveLeftWithPad([short num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [IFixedDateTime dateTime](/reference/runtime/qsys-runtime/i-fixed-date-time.html))

RPG's MOVEL. Moves left a int2 (short) to a datetime with given format and separators with pad.

```cs
DateTime MoveLeftWithPad(short num, IFixedDateTime dateTime)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | num | short value of the source number.
| [IFixedDateTime](/reference/runtime/qsys-runtime/i-fixed-date-time.html) | dateTime | Date, Time, Timestamp.

#### Returns

| Type | Description
| --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | The resulting DateTime value of the operation.

### DateTime MoveLeftWithPad([int num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [DateTime dateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind dateTimeKind](/reference/runtime/qsys-runtime/date-time-data-kind.html), [DateTimeFormat dateTimeFormat](/reference/datagate/datagate-common/date-time-format.html))

RPG's MOVEL. Moves left a int4 (int) to a datetime with given format and separators with pad.

```cs
DateTime MoveLeftWithPad(int num, DateTime dateTime, DateTimeDataKind dateTimeKind, DateTimeFormat dateTimeFormat)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | num | int value of the source number.
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | dateTime | Date, Time, Timestamp.
| [DateTimeDataKind](/reference/runtime/qsys-runtime/date-time-data-kind.html) | dateTimeKind | DateTime Kind.
| [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html) | dateTimeFormat | DateTime Format.

#### Returns

| Type | Description
| --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | The resulting DateTime value of the operation.

### DateTime MoveLeftWithPad([int num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [IFixedDateTime dateTime](/reference/runtime/qsys-runtime/i-fixed-date-time.html))

RPG's MOVEL. Moves left a int4 (int) to a datetime with given format and separators with pad.

```cs
DateTime MoveLeftWithPad(int num, IFixedDateTime dateTime)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | num | int value of the source number.
| [IFixedDateTime](/reference/runtime/qsys-runtime/i-fixed-date-time.html) | dateTime | Date, Time, Timestamp.

#### Returns

| Type | Description
| --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | The resulting DateTime value of the operation.

### DateTime MoveLeftWithPad([long num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [DateTime dateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind dateTimeKind](/reference/runtime/qsys-runtime/date-time-data-kind.html), [DateTimeFormat dateTimeFormat](/reference/datagate/datagate-common/date-time-format.html))

RPG's MOVE. Moves right a int8 (long) to a datetime with given format and separators with pad.

```cs
DateTime MoveLeftWithPad(long num, DateTime dateTime, DateTimeDataKind dateTimeKind, DateTimeFormat dateTimeFormat)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | num | long value of the source number.
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | dateTime | Date, Time, Timestamp.
| [DateTimeDataKind](/reference/runtime/qsys-runtime/date-time-data-kind.html) | dateTimeKind | DateTime Kind.
| [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html) | dateTimeFormat | DateTime Format.

#### Returns

| Type | Description
| --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | The resulting DateTime value of the operation.

### DateTime MoveLeftWithPad([long num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [IFixedDateTime dateTime](/reference/runtime/qsys-runtime/i-fixed-date-time.html))

RPG's MOVE. Moves right a int8 (long) to a datetime with given format and separators with pad.

```cs
DateTime MoveLeftWithPad(long num, IFixedDateTime dateTime)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | num | long value of the source number.
| [IFixedDateTime](/reference/runtime/qsys-runtime/i-fixed-date-time.html) | dateTime | Date, Time, Timestamp.

#### Returns

| Type | Description
| --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | The resulting DateTime value of the operation.

### decimal MoveLeftWithPad([short num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [decimal targetOperand](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [int targetOperandDig](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int targetOperandDec](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVEL. Moves left an int2 (short) to a decimal with pad.

```cs
decimal MoveLeftWithPad(short num, decimal targetOperand, int targetOperandDig, int targetOperandDec)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | num | short value of the source number.
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | targetOperand | targetOperand represents what is currently in the target.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetOperandDig | number of digits in the targetOperand.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetOperandDec | number of decimal places in the targetOperand.

#### Returns

| Type | Description
| --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | The resulting decimal value of the operation.

### decimal MoveLeftWithPad([int num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [decimal targetOperand](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [int targetOperandDig](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int targetOperandDec](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVEL. Moves left an int4 (int) to a decimal with pad.

```cs
decimal MoveLeftWithPad(int num, decimal targetOperand, int targetOperandDig, int targetOperandDec)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | num | int value of the source number.
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | targetOperand | targetOperand represents what is currently in the target.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetOperandDig | number of digits in the targetOperand.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetOperandDec | number of decimal places in the targetOperand.

#### Returns

| Type | Description
| --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | The resulting decimal value of the operation.

### decimal MoveLeftWithPad([long num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [decimal targetOperand](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [int targetOperandDig](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int targetOperandDec](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVEL. Moves left an int8 (long) to a decimal with pad.

```cs
decimal MoveLeftWithPad(long num, decimal targetOperand, int targetOperandDig, int targetOperandDec)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | num | long value of the source number.
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | targetOperand | targetOperand represents what is currently in the target.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetOperandDig | number of digits in the targetOperand.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetOperandDec | number of decimal places in the targetOperand.

#### Returns

| Type | Description
| --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | The resulting decimal value of the operation.

### string MoveLeftWithPad([short num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [string targetOperand](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

RPG's MOVEL. Moves left int2 (short) to a string with pad.

```cs
string MoveLeftWithPad(short num, string targetOperand)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | num | short value of the source number.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | targetOperand | targetOperand represents what is currently in the target.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The resulting string value of the operation.

### string MoveLeftWithPad([int num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [string targetOperand](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

RPG's MOVEL. Moves left int4 (int) to a string with pad.

```cs
string MoveLeftWithPad(int num, string targetOperand)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | num | int value of the source number.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | targetOperand | targetOperand represents what is currently in the target.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The resulting string value of the operation.

### string MoveLeftWithPad([long num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [string targetOperand](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

RPG's MOVEL. Moves left int8 (long) to a string with pad.

```cs
string MoveLeftWithPad(long num, string targetOperand)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | num | long value of the source number.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | targetOperand | targetOperand represents what is currently in the target.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The resulting string value of the operation.

### int MoveLeftWithPad([short num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int targetOperand](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVEL. Moves left an int2 (short) to an int4 (int) with pad.

```cs
int MoveLeftWithPad(short num, int targetOperand)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | num | short value of the source.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetOperand | targetOperand represents what is currently in the target.

#### Returns

| Type | Description
| --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | The resulting int value of the operation.

### long MoveLeftWithPad([short num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [long targetOperand](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVEL. Moves left an int2 (short) to an int8 (long) with pad.

```cs
long MoveLeftWithPad(short num, long targetOperand)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | num | short value of the source.
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | targetOperand | targetOperand represents what is currently in the target.

#### Returns

| Type | Description
| --- | ---
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | The resulting long value of the operation.

### long MoveLeftWithPad([int num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [long targetOperand](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVEL. Moves left an int4 (int) to an int8 (long) with pad.

```cs
long MoveLeftWithPad(int num, long targetOperand)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | num | int value of the source.
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | targetOperand | targetOperand represents what is currently in the target.

#### Returns

| Type | Description
| --- | ---
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | The resulting long value of the operation.

### DateTime MoveRight([short num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [DateTime dateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind dateTimeKind](/reference/runtime/qsys-runtime/date-time-data-kind.html), [DateTimeFormat dateTimeFormat](/reference/datagate/datagate-common/date-time-format.html))

RPG's MOVE. Moves right a int2 (short) to a datetime with given format and separators.

```cs
DateTime MoveRight(short num, DateTime dateTime, DateTimeDataKind dateTimeKind, DateTimeFormat dateTimeFormat)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | num | short value of the source number.
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | dateTime | Date, Time, Timestamp.
| [DateTimeDataKind](/reference/runtime/qsys-runtime/date-time-data-kind.html) | dateTimeKind | DateTime Kind.
| [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html) | dateTimeFormat | DateTime Format.

#### Returns

| Type | Description
| --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | The resulting DateTime value of the operation.

### DateTime MoveRight([short num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [IFixedDateTime dateTime](/reference/runtime/qsys-runtime/i-fixed-date-time.html))

RPG's MOVE. Moves right a int2 (short) to a datetime with given format and separators.

```cs
DateTime MoveRight(short num, IFixedDateTime dateTime)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | num | short value of the source number.
| [IFixedDateTime](/reference/runtime/qsys-runtime/i-fixed-date-time.html) | dateTime | Date, Time, Timestamp.

#### Returns

| Type | Description
| --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | The resulting DateTime value of the operation.

### DateTime MoveRight([int num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [DateTime dateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind dateTimeKind](/reference/runtime/qsys-runtime/date-time-data-kind.html), [DateTimeFormat dateTimeFormat](/reference/datagate/datagate-common/date-time-format.html))

RPG's MOVE. Moves right a int4 (int) to a datetime with given format and separators.

```cs
DateTime MoveRight(int num, DateTime dateTime, DateTimeDataKind dateTimeKind, DateTimeFormat dateTimeFormat)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | num | int value of the source number.
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | dateTime | Date, Time, Timestamp.
| [DateTimeDataKind](/reference/runtime/qsys-runtime/date-time-data-kind.html) | dateTimeKind | DateTime Kind.
| [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html) | dateTimeFormat | DateTime Format.

#### Returns

| Type | Description
| --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | The resulting DateTime value of the operation.

### DateTime MoveRight([int num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [IFixedDateTime dateTime](/reference/runtime/qsys-runtime/i-fixed-date-time.html))

RPG's MOVE. Moves right a int4 (int) to a datetime with given format and separators.

```cs
DateTime MoveRight(int num, IFixedDateTime dateTime)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | num | int value of the source number.
| [IFixedDateTime](/reference/runtime/qsys-runtime/i-fixed-date-time.html) | dateTime | Date, Time, Timestamp.

#### Returns

| Type | Description
| --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | The resulting DateTime value of the operation.

### DateTime MoveRight([long num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [DateTime dateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind dateTimeKind](/reference/runtime/qsys-runtime/date-time-data-kind.html), [DateTimeFormat dateTimeFormat](/reference/datagate/datagate-common/date-time-format.html))

RPG's MOVE. Moves right a int8 (long) to a datetime with given format and separators.

```cs
DateTime MoveRight(long num, DateTime dateTime, DateTimeDataKind dateTimeKind, DateTimeFormat dateTimeFormat)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | num | long value of the source number.
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | dateTime | Date, Time, Timestamp.
| [DateTimeDataKind](/reference/runtime/qsys-runtime/date-time-data-kind.html) | dateTimeKind | DateTime Kind.
| [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html) | dateTimeFormat | DateTime Format.

#### Returns

| Type | Description
| --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | The resulting DateTime value of the operation.

### DateTime MoveRight([long num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [IFixedDateTime dateTime](/reference/runtime/qsys-runtime/i-fixed-date-time.html))

RPG's MOVE. Moves right a int8 (long) to a datetime with given format and separators.

```cs
DateTime MoveRight(long num, IFixedDateTime dateTime)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | num | long value of the source number.
| [IFixedDateTime](/reference/runtime/qsys-runtime/i-fixed-date-time.html) | dateTime | Date, Time, Timestamp.

#### Returns

| Type | Description
| --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | The resulting DateTime value of the operation.

### decimal MoveRight([short num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [decimal targetOperand](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [int targetOperandDig](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int targetOperandDec](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVE. Moves right an int2 (short) to a decimal.

```cs
decimal MoveRight(short num, decimal targetOperand, int targetOperandDig, int targetOperandDec)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | num | short value of the source number.
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | targetOperand | targetOperand represents what is currently in the target.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetOperandDig | number of digits in the targetOperand.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetOperandDec | number of decimal places in the targetOperand.

#### Returns

| Type | Description
| --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | The resulting decimal value of the operation.

### decimal MoveRight([int num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [decimal targetOperand](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [int targetOperandDig](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int targetOperandDec](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVE. Moves right an int4 (int) to a decimal.

```cs
decimal MoveRight(int num, decimal targetOperand, int targetOperandDig, int targetOperandDec)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | num | int value of the source number.
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | targetOperand | targetOperand represents what is currently in the target.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetOperandDig | number of digits in the targetOperand.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetOperandDec | number of decimal places in the targetOperand.

#### Returns

| Type | Description
| --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | The resulting decimal value of the operation.

### decimal MoveRight([long num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [decimal targetOperand](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [int targetOperandDig](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int targetOperandDec](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVE. Moves right an int8 (long) to a decimal.

```cs
decimal MoveRight(long num, decimal targetOperand, int targetOperandDig, int targetOperandDec)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | num | long value of the source number.
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | targetOperand | targetOperand represents what is currently in the target.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetOperandDig | number of digits in the targetOperand.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetOperandDec | number of decimal places in the targetOperand.

#### Returns

| Type | Description
| --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | The resulting decimal value of the operation.

### string MoveRight([short num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [string targetOperand](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

RPG's MOVE. Moves right int2 (short) to a string.

```cs
string MoveRight(short num, string targetOperand)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | num | short value of the source number.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | targetOperand | targetOperand represents what is currently in the target.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The resulting string value of the operation.

### string MoveRight([int num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [string targetOperand](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

RPG's MOVE. Moves right int4 (int) to a string.

```cs
string MoveRight(int num, string targetOperand)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | num | int value of the source number.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | targetOperand | targetOperand represents what is currently in the target.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The resulting string value of the operation.

### string MoveRight([long num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [string targetOperand](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

RPG's MOVE. Moves right int8 (long) to a string.

```cs
string MoveRight(long num, string targetOperand)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | num | long value of the source number.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | targetOperand | targetOperand represents what is currently in the target.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The resulting string value of the operation.

### int MoveRight([short num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int targetOperand](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVE. Moves right an int2 (short) to an int4 (int).

```cs
int MoveRight(short num, int targetOperand)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | num | short value of the source.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetOperand | targetOperand represents what is currently in the target.

#### Returns

| Type | Description
| --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | The resulting int value of the operation.

### long MoveRight([short num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [long targetOperand](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVE. Moves right an int2 (short) to an int8 (long).

```cs
long MoveRight(short num, long targetOperand)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | num | long value of the source.
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | targetOperand | targetOperand represents what is currently in the target.

#### Returns

| Type | Description
| --- | ---
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | The resulting long value of the operation.

### long MoveRight([int num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [long targetOperand](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVE. Moves right an int4 (int) to an int8 (long).

```cs
long MoveRight(int num, long targetOperand)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | num | int value of the source.
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | targetOperand | targetOperand represents what is currently in the target.

#### Returns

| Type | Description
| --- | ---
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | The resulting long value of the operation.

### short MoveRight([int num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [short targetOperand](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVE. Moves right an int4 (int) to an int2 (short).

```cs
short MoveRight(int num, short targetOperand)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | num | int value of the source.
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | targetOperand | targetOperand represents what is currently in the target.

#### Returns

| Type | Description
| --- | ---
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | The resulting short value of the operation.

### short MoveRight([long num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [short targetOperand](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVE. Moves right an int8 (long) to an int2 (short).

```cs
short MoveRight(long num, short targetOperand)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | num | long value of the source.
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | targetOperand | targetOperand represents what is currently in the target.

#### Returns

| Type | Description
| --- | ---
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | The resulting short value of the operation.

### int MoveRight([long num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int targetOperand](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVE. Moves right an int8 (long) to an int4 (int).

```cs
int MoveRight(long num, int targetOperand)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | num | long value of the source.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetOperand | targetOperand represents what is currently in the target.

#### Returns

| Type | Description
| --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | The resulting int value of the operation.

### short MoveRight([short num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [short targetOperand](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVE. Moves right an int2 (short) to an int2 (short), this is actually the same as assignment.

```cs
short MoveRight(short num, short targetOperand)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | num | short value of the source.
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | targetOperand | targetOperand represents what is currently in the target.

#### Returns

| Type | Description
| --- | ---
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | The resulting short value of the operation.

### int MoveRight([int num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int targetOperand](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVE. Moves right an int4 (int) to an int4 (int), this is actually the same as assignment.

```cs
int MoveRight(int num, int targetOperand)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | num | int value of the source.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetOperand | targetOperand represents what is currently in the target.

#### Returns

| Type | Description
| --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | The resulting int value of the operation.

### long MoveRight([long num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [long targetOperand](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVE. Moves right an int8 (long) to an int8 (long), this is actually the same as assignment.

```cs
long MoveRight(long num, long targetOperand)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | num | long value of the source.
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | targetOperand | targetOperand represents what is currently in the target.

#### Returns

| Type | Description
| --- | ---
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | The resulting long value of the operation.

### char MoveRightToChar([short num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVE. Moves right a short into a character.

```cs
char MoveRightToChar(short num)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | num | The short value to move.

#### Returns

| Type | Description
| --- | ---
| [Char](https://docs.microsoft.com/en-us/dotnet/api/system.char) | The rightmost byte of the short value as a character.

### char MoveRightToChar([int num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVE. Moves right a int into a character.

```cs
char MoveRightToChar(int num)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | num | The int value to move.

#### Returns

| Type | Description
| --- | ---
| [Char](https://docs.microsoft.com/en-us/dotnet/api/system.char) | The rightmost byte of the int value as a character.

### char MoveRightToChar([long num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVE. Moves right a long into a character.

```cs
char MoveRightToChar(long num)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | num | The long value to move.

#### Returns

| Type | Description
| --- | ---
| [Char](https://docs.microsoft.com/en-us/dotnet/api/system.char) | The rightmost byte of the long value as a character.

### DateTime MoveRightWithPad([short num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [DateTime dateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind dateTimeKind](/reference/runtime/qsys-runtime/date-time-data-kind.html), [DateTimeFormat dateTimeFormat](/reference/datagate/datagate-common/date-time-format.html))

RPG's MOVE. Moves right a int2 (short) to a datetime with given format and separators with pad.

```cs
DateTime MoveRightWithPad(short num, DateTime dateTime, DateTimeDataKind dateTimeKind, DateTimeFormat dateTimeFormat)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | num | short value of the source number.
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | dateTime | Date, Time, Timestamp.
| [DateTimeDataKind](/reference/runtime/qsys-runtime/date-time-data-kind.html) | dateTimeKind | DateTime Kind.
| [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html) | dateTimeFormat | DateTime Format.

#### Returns

| Type | Description
| --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | The resulting DateTime value of the operation.

### DateTime MoveRightWithPad([short num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [IFixedDateTime dateTime](/reference/runtime/qsys-runtime/i-fixed-date-time.html))

RPG's MOVE. Moves right a int2 (short) to a datetime with given format and separators with pad.

```cs
DateTime MoveRightWithPad(short num, IFixedDateTime dateTime)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | num | short value of the source number.
| [IFixedDateTime](/reference/runtime/qsys-runtime/i-fixed-date-time.html) | dateTime | Date, Time, Timestamp.

#### Returns

| Type | Description
| --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | The resulting DateTime value of the operation.

### DateTime MoveRightWithPad([int num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [DateTime dateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind dateTimeKind](/reference/runtime/qsys-runtime/date-time-data-kind.html), [DateTimeFormat dateTimeFormat](/reference/datagate/datagate-common/date-time-format.html))

RPG's MOVE. Moves right a int4 (int) to a datetime with given format and separators with pad.

```cs
DateTime MoveRightWithPad(int num, DateTime dateTime, DateTimeDataKind dateTimeKind, DateTimeFormat dateTimeFormat)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | num | int value of the source number.
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | dateTime | Date, Time, Timestamp.
| [DateTimeDataKind](/reference/runtime/qsys-runtime/date-time-data-kind.html) | dateTimeKind | DateTime Kind.
| [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html) | dateTimeFormat | DateTime Format.

#### Returns

| Type | Description
| --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | The resulting DateTime value of the operation.

### DateTime MoveRightWithPad([int num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [IFixedDateTime dateTime](/reference/runtime/qsys-runtime/i-fixed-date-time.html))

RPG's MOVE. Moves right a int4 (int) to a datetime with given format and separators with pad.

```cs
DateTime MoveRightWithPad(int num, IFixedDateTime dateTime)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | num | int value of the source number.
| [IFixedDateTime](/reference/runtime/qsys-runtime/i-fixed-date-time.html) | dateTime | Date, Time, Timestamp.

#### Returns

| Type | Description
| --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | The resulting DateTime value of the operation.

### DateTime MoveRightWithPad([long num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [DateTime dateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind dateTimeKind](/reference/runtime/qsys-runtime/date-time-data-kind.html), [DateTimeFormat dateTimeFormat](/reference/datagate/datagate-common/date-time-format.html))

RPG's MOVE. Moves right a int8 (long) to a datetime with given format and separators with pad.

```cs
DateTime MoveRightWithPad(long num, DateTime dateTime, DateTimeDataKind dateTimeKind, DateTimeFormat dateTimeFormat)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | num | long value of the source number.
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | dateTime | Date, Time, Timestamp.
| [DateTimeDataKind](/reference/runtime/qsys-runtime/date-time-data-kind.html) | dateTimeKind | DateTime Kind.
| [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html) | dateTimeFormat | DateTime Format.

#### Returns

| Type | Description
| --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | The resulting DateTime value of the operation.

### DateTime MoveRightWithPad([long num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [IFixedDateTime dateTime](/reference/runtime/qsys-runtime/i-fixed-date-time.html))

RPG's MOVE. Moves right a int8 (long) to a datetime with given format and separators with pad.

```cs
DateTime MoveRightWithPad(long num, IFixedDateTime dateTime)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | num | long value of the source number.
| [IFixedDateTime](/reference/runtime/qsys-runtime/i-fixed-date-time.html) | dateTime | Date, Time, Timestamp.

#### Returns

| Type | Description
| --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | The resulting DateTime value of the operation.

### decimal MoveRightWithPad([short num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [decimal targetOperand](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [int targetOperandDig](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int targetOperandDec](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVE. Moves right an int2 (short) to a decimal with pad.

```cs
decimal MoveRightWithPad(short num, decimal targetOperand, int targetOperandDig, int targetOperandDec)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | num | short value of the source number.
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | targetOperand | targetOperand represents what is currently in the target.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetOperandDig | number of digits in the targetOperand.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetOperandDec | number of decimal places in the targetOperand.

#### Returns

| Type | Description
| --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | The resulting decimal value of the operation.

### decimal MoveRightWithPad([int num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [decimal targetOperand](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [int targetOperandDig](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int targetOperandDec](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVE. Moves right an int4 (int) to a decimal with pad.

```cs
decimal MoveRightWithPad(int num, decimal targetOperand, int targetOperandDig, int targetOperandDec)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | num | int value of the source number.
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | targetOperand | targetOperand represents what is currently in the target.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetOperandDig | number of digits in the targetOperand.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetOperandDec | number of decimal places in the targetOperand.

#### Returns

| Type | Description
| --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | The resulting decimal value of the operation.

### decimal MoveRightWithPad([long num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [decimal targetOperand](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [int targetOperandDig](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int targetOperandDec](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVE. Moves right an int8 (long) to a decimal with pad.

```cs
decimal MoveRightWithPad(long num, decimal targetOperand, int targetOperandDig, int targetOperandDec)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | num | long value of the source number.
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | targetOperand | targetOperand represents what is currently in the target.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetOperandDig | number of digits in the targetOperand.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetOperandDec | number of decimal places in the targetOperand.

#### Returns

| Type | Description
| --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | The resulting decimal value of the operation.

### string MoveRightWithPad([short num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [string targetOperand](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

RPG's MOVE. Moves right int2 (short) to a string with pad.

```cs
string MoveRightWithPad(short num, string targetOperand)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | num | short value of the source number.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | targetOperand | targetOperand represents what is currently in the target.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The resulting string value of the operation.

### string MoveRightWithPad([int num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [string targetOperand](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

RPG's MOVE. Moves right int4 (int) to a string with pad.

```cs
string MoveRightWithPad(int num, string targetOperand)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | num | int value of the source number.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | targetOperand | targetOperand represents what is currently in the target.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The resulting string value of the operation.

### string MoveRightWithPad([long num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [string targetOperand](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

RPG's MOVE. Moves right int8 (long) to a string with pad.

```cs
string MoveRightWithPad(long num, string targetOperand)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | num | long value of the source number.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | targetOperand | targetOperand represents what is currently in the target.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The resulting string value of the operation.

### int MoveRightWithPad([short num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int targetOperand](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVE. Moves right an int2 (short) to an int4 (int) with pad.

```cs
int MoveRightWithPad(short num, int targetOperand)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | num | short value of the source.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetOperand | targetOperand represents what is currently in the target.

#### Returns

| Type | Description
| --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | The resulting int value of the operation.

### long MoveRightWithPad([short num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [long targetOperand](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVE. Moves right an int2 (short) to an int8 (long) with pad.

```cs
long MoveRightWithPad(short num, long targetOperand)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | num | long value of the source.
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | targetOperand | targetOperand represents what is currently in the target.

#### Returns

| Type | Description
| --- | ---
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | The resulting long value of the operation.

### long MoveRightWithPad([int num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [long targetOperand](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVE. Moves right an int4 (int) to an int8 (long) with pad.

```cs
long MoveRightWithPad(int num, long targetOperand)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | num | int value of the source.
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | targetOperand | targetOperand represents what is currently in the target.

#### Returns

| Type | Description
| --- | ---
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | The resulting long value of the operation.

### short Sum([Int16\[\] array](https://docs.microsoft.com/en-us/dotnet/api/system.int16))

Returns the added values of each element in the array.

```cs
short Sum(Int16[] array)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int16\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | array | The array whose elements will be summed.

#### Returns

| Type | Description
| --- | ---
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | The added value of every element in the array.

### int Sum([Int32\[\] array](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

Returns the added values of each element in the array.

```cs
int Sum(Int32[] array)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | array | The array whose elements will be summed.

#### Returns

| Type | Description
| --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | The added value of every element in the array.

### long Sum([Int64\[\] array](https://docs.microsoft.com/en-us/dotnet/api/system.int64))

Returns the added values of each element in the array.

```cs
long Sum(Int64[] array)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int64\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | array | The array whose elements will be summed.

#### Returns

| Type | Description
| --- | ---
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | The added value of every element in the array.

### bool TestTime([short num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [DateTimeDataKind kind](/reference/runtime/qsys-runtime/date-time-data-kind.html), [DateTimeFormat format](/reference/datagate/datagate-common/date-time-format.html))

Tests whether a short contains a valid date/time/timestamp value. 

```cs
bool TestTime(short num, DateTimeDataKind kind, DateTimeFormat format)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | num | The short number to test.
| [DateTimeDataKind](/reference/runtime/qsys-runtime/date-time-data-kind.html) | kind | whether the number represents a date, time, or timestamp.
| [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html) | format | The date/time/timestamp format in which the number is.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | True if the number represents a valid date/time/timestamp value in the given format. False otherwise.

### bool TestTime([int num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [DateTimeDataKind kind](/reference/runtime/qsys-runtime/date-time-data-kind.html), [DateTimeFormat format](/reference/datagate/datagate-common/date-time-format.html))

Tests whether an int number contains a valid date/time/timestamp value. 

```cs
bool TestTime(int num, DateTimeDataKind kind, DateTimeFormat format)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | num | The int number to test.
| [DateTimeDataKind](/reference/runtime/qsys-runtime/date-time-data-kind.html) | kind | whether the number represents a date, time, or timestamp.
| [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html) | format | The date/time/timestamp format in which the number is.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | True if the number represents a valid date/time/timestamp value in the given format. False otherwise.

### bool TestTime([long num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [DateTimeDataKind kind](/reference/runtime/qsys-runtime/date-time-data-kind.html), [DateTimeFormat format](/reference/datagate/datagate-common/date-time-format.html))

Tests whether a long number contains a valid date/time/timestamp value. 

```cs
bool TestTime(long num, DateTimeDataKind kind, DateTimeFormat format)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | num | The long number to test.
| [DateTimeDataKind](/reference/runtime/qsys-runtime/date-time-data-kind.html) | kind | whether the number represents a date, time, or timestamp.
| [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html) | format | The date/time/timestamp format in which the number is.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | True if the number represents a valid date/time/timestamp value in the given format. False otherwise.

### DateTime ToDate([int source](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [DateTimeFormat format](/reference/datagate/datagate-common/date-time-format.html))

ToDate summary.

```cs
DateTime ToDate(int source, DateTimeFormat format)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | source | ToDate source param.
| [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html) | format | ToDate format param.

#### Returns

| Type | Description
| --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | ToDate returns.

### DateTime ToDate([short source](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [DateTimeFormat format](/reference/datagate/datagate-common/date-time-format.html))

ToDate summary.

```cs
DateTime ToDate(short source, DateTimeFormat format)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | source | ToDate source param.
| [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html) | format | ToDate format param.

#### Returns

| Type | Description
| --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | returns param.

### DateTime ToDate([long source](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [DateTimeFormat format](/reference/datagate/datagate-common/date-time-format.html))

ToDate summary.

```cs
DateTime ToDate(long source, DateTimeFormat format)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | source | ToDate source param.
| [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html) | format | ToDate format param.

#### Returns

| Type | Description
| --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | ToDate returns.

### decimal ToFixedDecimal([int num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int digits](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int decimals](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Adjusts the digits and decimal positions of a fixed decimal number using Away From Zero rounding.

```cs
decimal ToFixedDecimal(int num, int digits, int decimals)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | num |  The decimal number to round up.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | digits | The desired number of digits.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | decimals | The desired number of decimal positions.

#### Returns

| Type | Description
| --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | The decimal equivalent of num, adjusted to the given number of digits and decimal positions..

### decimal ToFixedDecimalRounded([int num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int digits](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int decimals](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Adjusts the digits and decimal positions of a fixed decimal number using Away From Zero rounding.

```cs
decimal ToFixedDecimalRounded(int num, int digits, int decimals)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | num |  The decimal number to round up.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | digits | The desired number of digits.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | decimals | The desired number of decimal positions.

#### Returns

| Type | Description
| --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | The decimal equivalent of num, adjusted to the given number of digits and decimal positions..

### string ToStringByte([byte num](https://docs.microsoft.com/en-us/dotnet/api/system.byte))

Returns as a string the char equivalent of a byte number.

```cs
string ToStringByte(byte num)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Byte](https://docs.microsoft.com/en-us/dotnet/api/system.byte) | num | The short number to convert.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The string resulting from interpreting the byte value as a character.

### string ToStringInt([int num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Returns as a string the char equivalent of a int number.

```cs
string ToStringInt(int num)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | num | The int number to convert.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The string resulting from interpreting the bytes of the int value as characters.

### string ToStringLong([long num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Returns as a string the char equivalentof a long number.

```cs
string ToStringLong(long num)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | num | The long number to convert.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The string resulting from interpreting the bytes of the long value as characters.

### string ToStringShort([short num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Returns as a string the char equivalent of a short number.

```cs
string ToStringShort(short num)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | num | The short number to convert.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The string resulting from interpreting the bytes of the short value as characters.

### DateTime ToTime([int source](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [DateTimeFormat format](/reference/datagate/datagate-common/date-time-format.html))

ToTime summary.

```cs
DateTime ToTime(int source, DateTimeFormat format)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | source | ToTime source param.
| [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html) | format | ToTime format param.

#### Returns

| Type | Description
| --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | ToTime returns.

### DateTime ToTime([short source](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [DateTimeFormat format](/reference/datagate/datagate-common/date-time-format.html))

ToTime summary.

```cs
DateTime ToTime(short source, DateTimeFormat format)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | source | ToTime source param.
| [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html) | format | ToTime format param.

#### Returns

| Type | Description
| --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | ToTime returns.

### DateTime ToTime([long source](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [DateTimeFormat format](/reference/datagate/datagate-common/date-time-format.html))

ToTime summary.

```cs
DateTime ToTime(long source, DateTimeFormat format)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | source | ToTime source param.
| [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html) | format | ToTime format param.

#### Returns

| Type | Description
| --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | ToTime returns.

### DateTime ToTimestamp([int source](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

ToTimestamp summary.

```cs
DateTime ToTimestamp(int source)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | source | ToTimestamp sourceparam.

#### Returns

| Type | Description
| --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | ToTimestamp returns.

### DateTime ToTimestamp([short source](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

ToTimestamp summary.

```cs
DateTime ToTimestamp(short source)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | source | ToTimestamp source param.

#### Returns

| Type | Description
| --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | ToTimestamp returns.

### DateTime ToTimestamp([long source](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

ToTimestamp summary.

```cs
DateTime ToTimestamp(long source)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | source | ToTimestamp source param.

#### Returns

| Type | Description
| --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | ToTimestamp returns
