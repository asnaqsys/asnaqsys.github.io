---
title: IntegerMethods Class
---

Contains extension methods for handling RPG operations and conversions for Integer (2, 4, and 8-byte long) values.

**Namespace:** ASNA.QSys.Runtime <br/>
**Assembly:** ASNA.QSys.Runtime

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> IntegerMethods

<br>
<br>

## Remarks

Contains extension methods for handling RPG operations and conversions for Integer (2, 4, and 8-byte long) values.

[//]: # ($$TODO: Complete the Remarks section.)

<br>
<br>

## Methods

| Type | Name | Description | Return Description 
| --- | --- | --- | --- 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [EditWord](#editwordint16-string)([Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | EditWord summary. | EditWord returns.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [EditWord](#editwordint32-string)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | EditWord summary. | EditWord returns.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [EditWord](#editwordint64-string)([Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | EditWord summary. | EditWord returns.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | [Equals](https://docs.microsoft.com/en-us/dotnet/api/system.object.equals)([Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | Determines whether the specified object is equal to the current object.<br>(Inherited from [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | true if the specified object is equal to the current object; otherwise, false.
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [Finalize](https://docs.microsoft.com/en-us/dotnet/api/system.object.finalize)() | Allows an object to try to free resources and perform other cleanup operations before it is reclaimed by garbage collection.<br>(Inherited from [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | [GetHashCode](https://docs.microsoft.com/en-us/dotnet/api/system.object.gethashcode)() | Serves as the default hash function.<br>(Inherited from [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | A hash code for the current object.
| [Type](https://docs.microsoft.com/en-us/dotnet/api/system.type) | [GetType](https://docs.microsoft.com/en-us/dotnet/api/system.object.gettype)() | Gets the Type of the current instance.<br>(Inherited from [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | The exact runtime type of the current instance.
| [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) | [MemberwiseClone](https://docs.microsoft.com/en-us/dotnet/api/system.object.memberwiseclone)() | Creates a shallow copy of the current Object.<br>(Inherited from [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | A shallow copy of the current Object.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [MoveLeft](#moveleftint16-datetime-datetimedatakind-datetimeformat)([Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16), [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind](/reference/asna-qsys-runtime/classes/date-time-data-kind.html), [DateTimeFormat](/reference/datagate-client/date-time-format-enumeration.html)) | RPG's MOVEL. Moves left a int2 (short) to a datetime with given format and separators. | The resulting DateTime value of the operation.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [MoveLeft](#moveleftint16-ifixeddatetime)([Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16), [IFixedDateTime](/reference/asna-qsys-runtime/classes/i-fixed-date-time.html)) | RPG's MOVEL. Moves left a int2 (short) to a datetime with given format and separators. | The resulting DateTime value of the operation.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [MoveLeft](#moveleftint32-datetime-datetimedatakind-datetimeformat)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind](/reference/asna-qsys-runtime/classes/date-time-data-kind.html), [DateTimeFormat](/reference/datagate-client/date-time-format-enumeration.html)) | RPG's MOVEL. Moves left a int4 (int) to a datetime with given format and separators. | The resulting DateTime value of the operation.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [MoveLeft](#moveleftint64-string)([Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | RPG's MOVEL. Moves left int8 (long) to a string. | The resulting string value of the operation.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [MoveLeft](#moveleftint16-int32)([Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's MOVEL. Moves left an int2 (short) to an int4 (int). | The resulting int value of the operation.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [MoveLeft](#moveleftint16-int64)([Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16), [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64)) | RPG's MOVEL. Moves left an int2 (short) to an int8 (long). | The resulting long value of the operation.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [MoveLeft](#moveleftint32-int64)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64)) | RPG's MOVEL. Moves left an int4 (int) to an int8 (long). | The resulting long value of the operation.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [MoveLeft](#moveleftint32-int16)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16)) | RPG's MOVEL. Moves left an int4 (int) to an int2 (short). | The resulting short value of the operation.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [MoveLeft](#moveleftint64-int16)([Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64), [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16)) | RPG's MOVEL. Moves left an int8 (long) to an int2 (short). | The resulting short value of the operation.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [MoveLeft](#moveleftint64-int32)([Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's MOVEL. Moves left an int8 (long) to an int4 (int). | The resulting int value of the operation.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [MoveLeft](#moveleftint16-int16)([Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16), [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16)) | RPG's MOVEL. Moves left an int2 (short) to an int2 (short), this is actually the same as assignment. | The resulting short value of the operation.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [MoveLeft](#moveleftint32-int32)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's MOVEL. Moves left an int4 (int) to an int4 (int), this is actually the same as assignment. | The resulting int value of the operation.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [MoveLeft](#moveleftint64-int64)([Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64), [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64)) | RPG's MOVEL. Moves left an int8 (long) to an int8 (long), this is actually the same as assignment. | The resulting long value of the operation.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [MoveLeft](#moveleftint32-ifixeddatetime)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [IFixedDateTime](/reference/asna-qsys-runtime/classes/i-fixed-date-time.html)) | RPG's MOVEL. Moves left a int4 (int) to a datetime with given format and separators. | The resulting DateTime value of the operation.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [MoveLeft](#moveleftint64-datetime-datetimedatakind-datetimeformat)([Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64), [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind](/reference/asna-qsys-runtime/classes/date-time-data-kind.html), [DateTimeFormat](/reference/datagate-client/date-time-format-enumeration.html)) | RPG's MOVE. Moves right a int8 (long) to a datetime with given format and separators. | The resulting DateTime value of the operation.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [MoveLeft](#moveleftint64-ifixeddatetime)([Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64), [IFixedDateTime](/reference/asna-qsys-runtime/classes/i-fixed-date-time.html)) | RPG's MOVE. Moves right a int8 (long) to a datetime with given format and separators. | The resulting DateTime value of the operation.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [MoveLeft](#moveleftint16-decimal-int32-int32)([Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16), [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's MOVEL. Moves left an int2 (short) to a decimal. | The resulting decimal value of the operation.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [MoveLeft](#moveleftint32-decimal-int32-int32)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's MOVEL. Moves left an int4 (int) to a decimal. | The resulting decimal value of the operation.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [MoveLeft](#moveleftint64-decimal-int32-int32)([Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64), [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's MOVEL. Moves left an int8 (long) to a decimal. | The resulting decimal value of the operation.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [MoveLeft](#moveleftint16-string)([Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | RPG's MOVEL. Moves left int2 (short) to a string. | The resulting string value of the operation.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [MoveLeft](#moveleftint32-string)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | RPG's MOVEL. Moves left int4 (int) to a string. | The resulting string value of the operation.
| [Char](https://docs.microsoft.com/en-us/dotnet/api/system.char) | [MoveLeftToChar](#movelefttocharint16)([Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16)) | RPG's MOVEL. Moves left a short into a character. | The leftmost byte of the short value as a character.
| [Char](https://docs.microsoft.com/en-us/dotnet/api/system.char) | [MoveLeftToChar](#movelefttocharint32)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's MOVEL. Moves left a int into a character. | The leftmost byte of the int value as a character.
| [Char](https://docs.microsoft.com/en-us/dotnet/api/system.char) | [MoveLeftToChar](#movelefttocharint64)([Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64)) | RPG's MOVEL. Moves left a long into a character. | The leftmost byte of the long value as a character.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [MoveLeftWithPad](#moveleftwithpadint16-datetime-datetimedatakind-datetimeformat)([Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16), [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind](/reference/asna-qsys-runtime/classes/date-time-data-kind.html), [DateTimeFormat](/reference/datagate-client/date-time-format-enumeration.html)) | RPG's MOVEL. Moves left a int2 (short) to a datetime with given format and separators with pad. | The resulting DateTime value of the operation.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [MoveLeftWithPad](#moveleftwithpadint16-ifixeddatetime)([Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16), [IFixedDateTime](/reference/asna-qsys-runtime/classes/i-fixed-date-time.html)) | RPG's MOVEL. Moves left a int2 (short) to a datetime with given format and separators with pad. | The resulting DateTime value of the operation.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [MoveLeftWithPad](#moveleftwithpadint32-datetime-datetimedatakind-datetimeformat)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind](/reference/asna-qsys-runtime/classes/date-time-data-kind.html), [DateTimeFormat](/reference/datagate-client/date-time-format-enumeration.html)) | RPG's MOVEL. Moves left a int4 (int) to a datetime with given format and separators with pad. | The resulting DateTime value of the operation.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [MoveLeftWithPad](#moveleftwithpadint64-string)([Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | RPG's MOVEL. Moves left int8 (long) to a string with pad. | The resulting string value of the operation.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [MoveLeftWithPad](#moveleftwithpadint16-int32)([Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's MOVEL. Moves left an int2 (short) to an int4 (int) with pad. | The resulting int value of the operation.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [MoveLeftWithPad](#moveleftwithpadint16-int64)([Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16), [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64)) | RPG's MOVEL. Moves left an int2 (short) to an int8 (long) with pad. | The resulting long value of the operation.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [MoveLeftWithPad](#moveleftwithpadint32-int64)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64)) | RPG's MOVEL. Moves left an int4 (int) to an int8 (long) with pad. | The resulting long value of the operation.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [MoveLeftWithPad](#moveleftwithpadint32-ifixeddatetime)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [IFixedDateTime](/reference/asna-qsys-runtime/classes/i-fixed-date-time.html)) | RPG's MOVEL. Moves left a int4 (int) to a datetime with given format and separators with pad. | The resulting DateTime value of the operation.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [MoveLeftWithPad](#moveleftwithpadint64-datetime-datetimedatakind-datetimeformat)([Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64), [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind](/reference/asna-qsys-runtime/classes/date-time-data-kind.html), [DateTimeFormat](/reference/datagate-client/date-time-format-enumeration.html)) | RPG's MOVE. Moves right a int8 (long) to a datetime with given format and separators with pad. | The resulting DateTime value of the operation.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [MoveLeftWithPad](#moveleftwithpadint64-ifixeddatetime)([Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64), [IFixedDateTime](/reference/asna-qsys-runtime/classes/i-fixed-date-time.html)) | RPG's MOVE. Moves right a int8 (long) to a datetime with given format and separators with pad. | The resulting DateTime value of the operation.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [MoveLeftWithPad](#moveleftwithpadint16-decimal-int32-int32)([Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16), [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's MOVEL. Moves left an int2 (short) to a decimal with pad. | The resulting decimal value of the operation.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [MoveLeftWithPad](#moveleftwithpadint32-decimal-int32-int32)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's MOVEL. Moves left an int4 (int) to a decimal with pad. | The resulting decimal value of the operation.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [MoveLeftWithPad](#moveleftwithpadint64-decimal-int32-int32)([Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64), [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's MOVEL. Moves left an int8 (long) to a decimal with pad. | The resulting decimal value of the operation.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [MoveLeftWithPad](#moveleftwithpadint16-string)([Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | RPG's MOVEL. Moves left int2 (short) to a string with pad. | The resulting string value of the operation.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [MoveLeftWithPad](#moveleftwithpadint32-string)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | RPG's MOVEL. Moves left int4 (int) to a string with pad. | The resulting string value of the operation.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [MoveRight](#moverightint16-datetime-datetimedatakind-datetimeformat)([Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16), [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind](/reference/asna-qsys-runtime/classes/date-time-data-kind.html), [DateTimeFormat](/reference/datagate-client/date-time-format-enumeration.html)) | RPG's MOVE. Moves right a int2 (short) to a datetime with given format and separators. | The resulting DateTime value of the operation.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [MoveRight](#moverightint16-ifixeddatetime)([Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16), [IFixedDateTime](/reference/asna-qsys-runtime/classes/i-fixed-date-time.html)) | RPG's MOVE. Moves right a int2 (short) to a datetime with given format and separators. | The resulting DateTime value of the operation.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [MoveRight](#moverightint32-datetime-datetimedatakind-datetimeformat)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind](/reference/asna-qsys-runtime/classes/date-time-data-kind.html), [DateTimeFormat](/reference/datagate-client/date-time-format-enumeration.html)) | RPG's MOVE. Moves right a int4 (int) to a datetime with given format and separators. | The resulting DateTime value of the operation.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [MoveRight](#moverightint64-string)([Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | RPG's MOVE. Moves right int8 (long) to a string. | The resulting string value of the operation.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [MoveRight](#moverightint16-int32)([Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's MOVE. Moves right an int2 (short) to an int4 (int). | The resulting int value of the operation.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [MoveRight](#moverightint16-int64)([Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16), [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64)) | RPG's MOVE. Moves right an int2 (short) to an int8 (long). | The resulting long value of the operation.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [MoveRight](#moverightint32-int64)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64)) | RPG's MOVE. Moves right an int4 (int) to an int8 (long). | The resulting long value of the operation.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [MoveRight](#moverightint32-int16)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16)) | RPG's MOVE. Moves right an int4 (int) to an int2 (short). | The resulting short value of the operation.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [MoveRight](#moverightint64-int16)([Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64), [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16)) | RPG's MOVE. Moves right an int8 (long) to an int2 (short). | The resulting short value of the operation.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [MoveRight](#moverightint64-int32)([Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's MOVE. Moves right an int8 (long) to an int4 (int). | The resulting int value of the operation.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [MoveRight](#moverightint16-int16)([Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16), [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16)) | RPG's MOVE. Moves right an int2 (short) to an int2 (short), this is actually the same as assignment. | The resulting short value of the operation.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [MoveRight](#moverightint32-int32)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's MOVE. Moves right an int4 (int) to an int4 (int), this is actually the same as assignment. | The resulting int value of the operation.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [MoveRight](#moverightint64-int64)([Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64), [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64)) | RPG's MOVE. Moves right an int8 (long) to an int8 (long), this is actually the same as assignment. | The resulting long value of the operation.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [MoveRight](#moverightint32-ifixeddatetime)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [IFixedDateTime](/reference/asna-qsys-runtime/classes/i-fixed-date-time.html)) | RPG's MOVE. Moves right a int4 (int) to a datetime with given format and separators. | The resulting DateTime value of the operation.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [MoveRight](#moverightint64-datetime-datetimedatakind-datetimeformat)([Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64), [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind](/reference/asna-qsys-runtime/classes/date-time-data-kind.html), [DateTimeFormat](/reference/datagate-client/date-time-format-enumeration.html)) | RPG's MOVE. Moves right a int8 (long) to a datetime with given format and separators. | The resulting DateTime value of the operation.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [MoveRight](#moverightint64-ifixeddatetime)([Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64), [IFixedDateTime](/reference/asna-qsys-runtime/classes/i-fixed-date-time.html)) | RPG's MOVE. Moves right a int8 (long) to a datetime with given format and separators. | The resulting DateTime value of the operation.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [MoveRight](#moverightint16-decimal-int32-int32)([Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16), [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's MOVE. Moves right an int2 (short) to a decimal. | The resulting decimal value of the operation.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [MoveRight](#moverightint32-decimal-int32-int32)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's MOVE. Moves right an int4 (int) to a decimal. | The resulting decimal value of the operation.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [MoveRight](#moverightint64-decimal-int32-int32)([Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64), [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's MOVE. Moves right an int8 (long) to a decimal. | The resulting decimal value of the operation.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [MoveRight](#moverightint16-string)([Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | RPG's MOVE. Moves right int2 (short) to a string. | The resulting string value of the operation.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [MoveRight](#moverightint32-string)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | RPG's MOVE. Moves right int4 (int) to a string. | The resulting string value of the operation.
| [Char](https://docs.microsoft.com/en-us/dotnet/api/system.char) | [MoveRightToChar](#moverighttocharint16)([Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16)) | RPG's MOVE. Moves right a short into a character. | The rightmost byte of the short value as a character.
| [Char](https://docs.microsoft.com/en-us/dotnet/api/system.char) | [MoveRightToChar](#moverighttocharint32)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's MOVE. Moves right a int into a character. | The rightmost byte of the int value as a character.
| [Char](https://docs.microsoft.com/en-us/dotnet/api/system.char) | [MoveRightToChar](#moverighttocharint64)([Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64)) | RPG's MOVE. Moves right a long into a character. | The rightmost byte of the long value as a character.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [MoveRightWithPad](#moverightwithpadint16-datetime-datetimedatakind-datetimeformat)([Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16), [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind](/reference/asna-qsys-runtime/classes/date-time-data-kind.html), [DateTimeFormat](/reference/datagate-client/date-time-format-enumeration.html)) | RPG's MOVE. Moves right a int2 (short) to a datetime with given format and separators with pad. | The resulting DateTime value of the operation.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [MoveRightWithPad](#moverightwithpadint16-ifixeddatetime)([Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16), [IFixedDateTime](/reference/asna-qsys-runtime/classes/i-fixed-date-time.html)) | RPG's MOVE. Moves right a int2 (short) to a datetime with given format and separators with pad. | The resulting DateTime value of the operation.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [MoveRightWithPad](#moverightwithpadint32-datetime-datetimedatakind-datetimeformat)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind](/reference/asna-qsys-runtime/classes/date-time-data-kind.html), [DateTimeFormat](/reference/datagate-client/date-time-format-enumeration.html)) | RPG's MOVE. Moves right a int4 (int) to a datetime with given format and separators with pad. | The resulting DateTime value of the operation.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [MoveRightWithPad](#moverightwithpadint64-string)([Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | RPG's MOVE. Moves right int8 (long) to a string with pad. | The resulting string value of the operation.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [MoveRightWithPad](#moverightwithpadint16-int32)([Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's MOVE. Moves right an int2 (short) to an int4 (int) with pad. | The resulting int value of the operation.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [MoveRightWithPad](#moverightwithpadint16-int64)([Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16), [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64)) | RPG's MOVE. Moves right an int2 (short) to an int8 (long) with pad. | The resulting long value of the operation.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [MoveRightWithPad](#moverightwithpadint32-int64)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64)) | RPG's MOVE. Moves right an int4 (int) to an int8 (long) with pad. | The resulting long value of the operation.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [MoveRightWithPad](#moverightwithpadint32-ifixeddatetime)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [IFixedDateTime](/reference/asna-qsys-runtime/classes/i-fixed-date-time.html)) | RPG's MOVE. Moves right a int4 (int) to a datetime with given format and separators with pad. | The resulting DateTime value of the operation.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [MoveRightWithPad](#moverightwithpadint64-datetime-datetimedatakind-datetimeformat)([Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64), [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind](/reference/asna-qsys-runtime/classes/date-time-data-kind.html), [DateTimeFormat](/reference/datagate-client/date-time-format-enumeration.html)) | RPG's MOVE. Moves right a int8 (long) to a datetime with given format and separators with pad. | The resulting DateTime value of the operation.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [MoveRightWithPad](#moverightwithpadint64-ifixeddatetime)([Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64), [IFixedDateTime](/reference/asna-qsys-runtime/classes/i-fixed-date-time.html)) | RPG's MOVE. Moves right a int8 (long) to a datetime with given format and separators with pad. | The resulting DateTime value of the operation.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [MoveRightWithPad](#moverightwithpadint16-decimal-int32-int32)([Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16), [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's MOVE. Moves right an int2 (short) to a decimal with pad. | The resulting decimal value of the operation.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [MoveRightWithPad](#moverightwithpadint32-decimal-int32-int32)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's MOVE. Moves right an int4 (int) to a decimal with pad. | The resulting decimal value of the operation.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [MoveRightWithPad](#moverightwithpadint64-decimal-int32-int32)([Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64), [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's MOVE. Moves right an int8 (long) to a decimal with pad. | The resulting decimal value of the operation.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [MoveRightWithPad](#moverightwithpadint16-string)([Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | RPG's MOVE. Moves right int2 (short) to a string with pad. | The resulting string value of the operation.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [MoveRightWithPad](#moverightwithpadint32-string)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | RPG's MOVE. Moves right int4 (int) to a string with pad. | The resulting string value of the operation.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | [ReferenceEquals](https://docs.microsoft.com/en-us/dotnet/api/system.object.referenceequals)([Object](https://docs.microsoft.com/en-us/dotnet/api/system.object), [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | Determines whether the specified Object instances are the same instance.<br>(Inherited from [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | true if objA is the same instance as objB or if both are null; otherwise, false.
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | [SetHiLoEq](#sethiloeqint16-indicator-indicator-indicator)([Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16), [Indicator](/reference/asna-qsys-runtime/classes/indicator.html), [Indicator](/reference/asna-qsys-runtime/classes/indicator.html), [Indicator](/reference/asna-qsys-runtime/classes/indicator.html)) | Sets the HI, LO, and EQ flags passed in, based on the value of num. | The same value that was passed in in num.
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | [SetHiLoEq](#sethiloeqint32-indicator-indicator-indicator)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Indicator](/reference/asna-qsys-runtime/classes/indicator.html), [Indicator](/reference/asna-qsys-runtime/classes/indicator.html), [Indicator](/reference/asna-qsys-runtime/classes/indicator.html)) | Sets the HI, LO, and EQ flags passed in, based on the value of num. | The same value that was passed in in num.
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | [SetHiLoEq](#sethiloeqint64-indicator-indicator-indicator)([Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64), [Indicator](/reference/asna-qsys-runtime/classes/indicator.html), [Indicator](/reference/asna-qsys-runtime/classes/indicator.html), [Indicator](/reference/asna-qsys-runtime/classes/indicator.html)) | Sets the HI, LO, and EQ flags passed in, based on the value of num. | The same value that was passed in in num.
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | [Sum](#sumint16[])([Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16)) | Returns the added values of each element in the array. | The added value of every element in the array.
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | [Sum](#sumint32[])([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Returns the added values of each element in the array. | The added value of every element in the array.
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | [Sum](#sumint64[])([Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64)) | Returns the added values of each element in the array. | The added value of every element in the array.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | [TestTime](#testtimeint16-datetimedatakind-datetimeformat)([Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16), [DateTimeDataKind](/reference/asna-qsys-runtime/classes/date-time-data-kind.html), [DateTimeFormat](/reference/datagate-client/date-time-format-enumeration.html)) | Tests whether a short contains a valid date/time/timestamp value. | True if the number represents a valid date/time/timestamp value in the given format. False otherwise.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | [TestTime](#testtimeint32-datetimedatakind-datetimeformat)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [DateTimeDataKind](/reference/asna-qsys-runtime/classes/date-time-data-kind.html), [DateTimeFormat](/reference/datagate-client/date-time-format-enumeration.html)) | Tests whether an int number contains a valid date/time/timestamp value. | True if the number represents a valid date/time/timestamp value in the given format. False otherwise.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | [TestTime](#testtimeint64-datetimedatakind-datetimeformat)([Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64), [DateTimeDataKind](/reference/asna-qsys-runtime/classes/date-time-data-kind.html), [DateTimeFormat](/reference/datagate-client/date-time-format-enumeration.html)) | Tests whether a long number contains a valid date/time/timestamp value. | True if the number represents a valid date/time/timestamp value in the given format. False otherwise.
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | [ToDate](#todateint32-datetimeformat)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [DateTimeFormat](/reference/datagate-client/date-time-format-enumeration.html)) | ToDate summary. | ToDate returns.
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | [ToDate](#todateint16-datetimeformat)([Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16), [DateTimeFormat](/reference/datagate-client/date-time-format-enumeration.html)) | ToDate summary. | returns param.
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | [ToDate](#todateint64-datetimeformat)([Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64), [DateTimeFormat](/reference/datagate-client/date-time-format-enumeration.html)) | ToDate summary. | ToDate returns.
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | [ToFixedDecimal](#tofixeddecimalint32-int32-int32)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Adjusts the digits and decimal positions of a fixed decimal number using Away From Zero rounding. | The decimal equivalent of num, adjusted to the given number of digits and decimal positions..
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | [ToFixedDecimalRounded](#tofixeddecimalroundedint32-int32-int32)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Adjusts the digits and decimal positions of a fixed decimal number using Away From Zero rounding. | The decimal equivalent of num, adjusted to the given number of digits and decimal positions..
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | [ToString](https://docs.microsoft.com/en-us/dotnet/api/system.object.tostring)() | Returns a string that represents the current object.<br>(Inherited from [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | A string that represents the current object.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [ToStringByte](#tostringbytebyte)([Byte](https://docs.microsoft.com/en-us/dotnet/api/system.byte)) | Returns as a string the char equivalent of a byte number. | The string resulting from interpreting the byte value as a character.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [ToStringInt](#tostringintint32)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Returns as a string the char equivalent of a int number. | The string resulting from interpreting the bytes of the int value as characters.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [ToStringLong](#tostringlongint64)([Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64)) | Returns as a string the char equivalentof a long number. | The string resulting from interpreting the bytes of the long value as characters.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [ToStringShort](#tostringshortint16)([Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16)) | Returns as a string the char equivalent of a short number. | The string resulting from interpreting the bytes of the short value as characters.
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | [ToTime](#totimeint32-datetimeformat)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [DateTimeFormat](/reference/datagate-client/date-time-format-enumeration.html)) | ToTime summary. | ToTime returns.
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | [ToTime](#totimeint16-datetimeformat)([Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16), [DateTimeFormat](/reference/datagate-client/date-time-format-enumeration.html)) | ToTime summary. | ToTime returns.
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | [ToTime](#totimeint64-datetimeformat)([Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64), [DateTimeFormat](/reference/datagate-client/date-time-format-enumeration.html)) | ToTime summary. | ToTime returns.
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | [ToTimestamp](#totimestampint32)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | ToTimestamp summary. | ToTimestamp returns.
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | [ToTimestamp](#totimestampint16)([Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16)) | ToTimestamp summary. | ToTimestamp returns.
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | [ToTimestamp](#totimestampint64)([Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64)) | ToTimestamp summary. | ToTimestamp returns

<br>
<br>

### EditWord([Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

EditWord summary.

```cs
EditWord(Int16 num, String editwordString);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | num | EditWord num param. 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | editwordString | EditWord editwordString param. 

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

EditWord returns.


<br>
<br>

### EditWord([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

EditWord summary.

```cs
EditWord(Int32 num, String editwordString);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | num | EditWord num param. 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | editwordString | EditWord editwordString param. 

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

EditWord returns.


<br>
<br>

### EditWord([Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

EditWord summary.

```cs
EditWord(Int64 num, String editwordString);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | num | EditWord num param. 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | editwordString | EditWord editwordString param. 

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

EditWord returns.


<br>
<br>

### MoveLeft([Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16), [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind](/reference/asna-qsys-runtime/classes/date-time-data-kind.html), [DateTimeFormat](/reference/datagate-client/date-time-format-enumeration.html))

RPG's MOVEL. Moves left a int2 (short) to a datetime with given format and separators.

```cs
MoveLeft(Int16 num, DateTime dateTime, Runtime.DateTimeDataKind dateTimeKind, ASNA.DataGate.Common.DateTimeFormat dateTimeFormat);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | num | short value of the source number. 
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | dateTime | Date, Time, Timestamp. 
| [DateTimeDataKind](/reference/asna-qsys-runtime/classes/date-time-data-kind.html) | dateTimeKind | DateTime Kind. 
| [DateTimeFormat](/reference/datagate-client/date-time-format-enumeration.html) | dateTimeFormat | DateTime Format. 

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

The resulting DateTime value of the operation.


<br>
<br>

### MoveLeft([Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16), [IFixedDateTime](/reference/asna-qsys-runtime/classes/i-fixed-date-time.html))

RPG's MOVEL. Moves left a int2 (short) to a datetime with given format and separators.

```cs
MoveLeft(Int16 num, Runtime.IFixedDateTime dateTime);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | num | short value of the source number. 
| [IFixedDateTime](/reference/asna-qsys-runtime/classes/i-fixed-date-time.html) | dateTime | Date, Time, Timestamp. 

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

The resulting DateTime value of the operation.


<br>
<br>

### MoveLeft([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind](/reference/asna-qsys-runtime/classes/date-time-data-kind.html), [DateTimeFormat](/reference/datagate-client/date-time-format-enumeration.html))

RPG's MOVEL. Moves left a int4 (int) to a datetime with given format and separators.

```cs
MoveLeft(Int32 num, DateTime dateTime, Runtime.DateTimeDataKind dateTimeKind, ASNA.DataGate.Common.DateTimeFormat dateTimeFormat);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | num | int value of the source number. 
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | dateTime | Date, Time, Timestamp. 
| [DateTimeDataKind](/reference/asna-qsys-runtime/classes/date-time-data-kind.html) | dateTimeKind | DateTime Kind. 
| [DateTimeFormat](/reference/datagate-client/date-time-format-enumeration.html) | dateTimeFormat | DateTime Format. 

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

The resulting DateTime value of the operation.


<br>
<br>

### MoveLeft([Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

RPG's MOVEL. Moves left int8 (long) to a string.

```cs
MoveLeft(Int64 num, String targetOperand);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | num | long value of the source number. 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | targetOperand | targetOperand represents what is currently in the target. 

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

The resulting string value of the operation.


<br>
<br>

### MoveLeft([Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

RPG's MOVEL. Moves left an int2 (short) to an int4 (int).

```cs
MoveLeft(Int16 num, Int32 targetOperand);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | num | short value of the source. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetOperand | targetOperand represents what is currently in the target. 

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

The resulting int value of the operation.


<br>
<br>

### MoveLeft([Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16), [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64))

RPG's MOVEL. Moves left an int2 (short) to an int8 (long).

```cs
MoveLeft(Int16 num, Int64 targetOperand);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | num | long value of the source. 
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | targetOperand | targetOperand represents what is currently in the target. 

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

The resulting long value of the operation.


<br>
<br>

### MoveLeft([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64))

RPG's MOVEL. Moves left an int4 (int) to an int8 (long).

```cs
MoveLeft(Int32 num, Int64 targetOperand);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | num | int value of the source. 
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | targetOperand | targetOperand represents what is currently in the target. 

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

The resulting long value of the operation.


<br>
<br>

### MoveLeft([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16))

RPG's MOVEL. Moves left an int4 (int) to an int2 (short).

```cs
MoveLeft(Int32 num, Int16 targetOperand);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | num | int value of the source. 
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | targetOperand | targetOperand represents what is currently in the target. 

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

The resulting short value of the operation.


<br>
<br>

### MoveLeft([Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64), [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16))

RPG's MOVEL. Moves left an int8 (long) to an int2 (short).

```cs
MoveLeft(Int64 num, Int16 targetOperand);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | num | long value of the source. 
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | targetOperand | targetOperand represents what is currently in the target. 

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

The resulting short value of the operation.


<br>
<br>

### MoveLeft([Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

RPG's MOVEL. Moves left an int8 (long) to an int4 (int).

```cs
MoveLeft(Int64 num, Int32 targetOperand);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | num | long value of the source. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetOperand | targetOperand represents what is currently in the target. 

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

The resulting int value of the operation.


<br>
<br>

### MoveLeft([Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16), [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16))

RPG's MOVEL. Moves left an int2 (short) to an int2 (short), this is actually the same as assignment.

```cs
MoveLeft(Int16 num, Int16 targetOperand);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | num | short value of the source. 
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | targetOperand | targetOperand represents what is currently in the target. 

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

The resulting short value of the operation.


<br>
<br>

### MoveLeft([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

RPG's MOVEL. Moves left an int4 (int) to an int4 (int), this is actually the same as assignment.

```cs
MoveLeft(Int32 num, Int32 targetOperand);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | num | int value of the source. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetOperand | targetOperand represents what is currently in the target. 

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

The resulting int value of the operation.


<br>
<br>

### MoveLeft([Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64), [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64))

RPG's MOVEL. Moves left an int8 (long) to an int8 (long), this is actually the same as assignment.

```cs
MoveLeft(Int64 num, Int64 targetOperand);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | num | long value of the source. 
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | targetOperand | targetOperand represents what is currently in the target. 

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

The resulting long value of the operation.


<br>
<br>

### MoveLeft([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [IFixedDateTime](/reference/asna-qsys-runtime/classes/i-fixed-date-time.html))

RPG's MOVEL. Moves left a int4 (int) to a datetime with given format and separators.

```cs
MoveLeft(Int32 num, Runtime.IFixedDateTime dateTime);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | num | int value of the source number. 
| [IFixedDateTime](/reference/asna-qsys-runtime/classes/i-fixed-date-time.html) | dateTime | Date, Time, Timestamp. 

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

The resulting DateTime value of the operation.


<br>
<br>

### MoveLeft([Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64), [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind](/reference/asna-qsys-runtime/classes/date-time-data-kind.html), [DateTimeFormat](/reference/datagate-client/date-time-format-enumeration.html))

RPG's MOVE. Moves right a int8 (long) to a datetime with given format and separators.

```cs
MoveLeft(Int64 num, DateTime dateTime, Runtime.DateTimeDataKind dateTimeKind, ASNA.DataGate.Common.DateTimeFormat dateTimeFormat);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | num | long value of the source number. 
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | dateTime | Date, Time, Timestamp. 
| [DateTimeDataKind](/reference/asna-qsys-runtime/classes/date-time-data-kind.html) | dateTimeKind | DateTime Kind. 
| [DateTimeFormat](/reference/datagate-client/date-time-format-enumeration.html) | dateTimeFormat | DateTime Format. 

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

The resulting DateTime value of the operation.


<br>
<br>

### MoveLeft([Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64), [IFixedDateTime](/reference/asna-qsys-runtime/classes/i-fixed-date-time.html))

RPG's MOVE. Moves right a int8 (long) to a datetime with given format and separators.

```cs
MoveLeft(Int64 num, Runtime.IFixedDateTime dateTime);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | num | long value of the source number. 
| [IFixedDateTime](/reference/asna-qsys-runtime/classes/i-fixed-date-time.html) | dateTime | Date, Time, Timestamp. 

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

The resulting DateTime value of the operation.


<br>
<br>

### MoveLeft([Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16), [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

RPG's MOVEL. Moves left an int2 (short) to a decimal.

```cs
MoveLeft(Int16 num, Decimal targetOperand, Int32 targetOperandDig, Int32 targetOperandDec);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | num | short value of the source number. 
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | targetOperand | targetOperand represents what is currently in the target. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetOperandDig | number of digits in the targetOperand. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetOperandDec | number of decimal places in the targetOperand. 

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

The resulting decimal value of the operation.


<br>
<br>

### MoveLeft([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

RPG's MOVEL. Moves left an int4 (int) to a decimal.

```cs
MoveLeft(Int32 num, Decimal targetOperand, Int32 targetOperandDig, Int32 targetOperandDec);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | num | int value of the source number. 
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | targetOperand | targetOperand represents what is currently in the target. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetOperandDig | number of digits in the targetOperand. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetOperandDec | number of decimal places in the targetOperand. 

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

The resulting decimal value of the operation.


<br>
<br>

### MoveLeft([Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64), [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

RPG's MOVEL. Moves left an int8 (long) to a decimal.

```cs
MoveLeft(Int64 num, Decimal targetOperand, Int32 targetOperandDig, Int32 targetOperandDec);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | num | long value of the source number. 
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | targetOperand | targetOperand represents what is currently in the target. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetOperandDig | number of digits in the targetOperand. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetOperandDec | number of decimal places in the targetOperand. 

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

The resulting decimal value of the operation.


<br>
<br>

### MoveLeft([Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

RPG's MOVEL. Moves left int2 (short) to a string.

```cs
MoveLeft(Int16 num, String targetOperand);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | num | short value of the source number. 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | targetOperand | targetOperand represents what is currently in the target. 

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

The resulting string value of the operation.


<br>
<br>

### MoveLeft([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

RPG's MOVEL. Moves left int4 (int) to a string.

```cs
MoveLeft(Int32 num, String targetOperand);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | num | int value of the source number. 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | targetOperand | targetOperand represents what is currently in the target. 

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

The resulting string value of the operation.


<br>
<br>

### MoveLeftToChar([Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16))

RPG's MOVEL. Moves left a short into a character.

```cs
MoveLeftToChar(Int16 num);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | num | The short value to move. 

#### Returns

[Char](https://docs.microsoft.com/en-us/dotnet/api/system.char)

The leftmost byte of the short value as a character.


<br>
<br>

### MoveLeftToChar([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

RPG's MOVEL. Moves left a int into a character.

```cs
MoveLeftToChar(Int32 num);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | num | The int value to move. 

#### Returns

[Char](https://docs.microsoft.com/en-us/dotnet/api/system.char)

The leftmost byte of the int value as a character.


<br>
<br>

### MoveLeftToChar([Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64))

RPG's MOVEL. Moves left a long into a character.

```cs
MoveLeftToChar(Int64 num);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | num | The long value to move. 

#### Returns

[Char](https://docs.microsoft.com/en-us/dotnet/api/system.char)

The leftmost byte of the long value as a character.


<br>
<br>

### MoveLeftWithPad([Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16), [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind](/reference/asna-qsys-runtime/classes/date-time-data-kind.html), [DateTimeFormat](/reference/datagate-client/date-time-format-enumeration.html))

RPG's MOVEL. Moves left a int2 (short) to a datetime with given format and separators with pad.

```cs
MoveLeftWithPad(Int16 num, DateTime dateTime, Runtime.DateTimeDataKind dateTimeKind, ASNA.DataGate.Common.DateTimeFormat dateTimeFormat);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | num | short value of the source number. 
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | dateTime | Date, Time, Timestamp. 
| [DateTimeDataKind](/reference/asna-qsys-runtime/classes/date-time-data-kind.html) | dateTimeKind | DateTime Kind. 
| [DateTimeFormat](/reference/datagate-client/date-time-format-enumeration.html) | dateTimeFormat | DateTime Format. 

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

The resulting DateTime value of the operation.


<br>
<br>

### MoveLeftWithPad([Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16), [IFixedDateTime](/reference/asna-qsys-runtime/classes/i-fixed-date-time.html))

RPG's MOVEL. Moves left a int2 (short) to a datetime with given format and separators with pad.

```cs
MoveLeftWithPad(Int16 num, Runtime.IFixedDateTime dateTime);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | num | short value of the source number. 
| [IFixedDateTime](/reference/asna-qsys-runtime/classes/i-fixed-date-time.html) | dateTime | Date, Time, Timestamp. 

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

The resulting DateTime value of the operation.


<br>
<br>

### MoveLeftWithPad([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind](/reference/asna-qsys-runtime/classes/date-time-data-kind.html), [DateTimeFormat](/reference/datagate-client/date-time-format-enumeration.html))

RPG's MOVEL. Moves left a int4 (int) to a datetime with given format and separators with pad.

```cs
MoveLeftWithPad(Int32 num, DateTime dateTime, Runtime.DateTimeDataKind dateTimeKind, ASNA.DataGate.Common.DateTimeFormat dateTimeFormat);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | num | int value of the source number. 
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | dateTime | Date, Time, Timestamp. 
| [DateTimeDataKind](/reference/asna-qsys-runtime/classes/date-time-data-kind.html) | dateTimeKind | DateTime Kind. 
| [DateTimeFormat](/reference/datagate-client/date-time-format-enumeration.html) | dateTimeFormat | DateTime Format. 

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

The resulting DateTime value of the operation.


<br>
<br>

### MoveLeftWithPad([Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

RPG's MOVEL. Moves left int8 (long) to a string with pad.

```cs
MoveLeftWithPad(Int64 num, String targetOperand);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | num | long value of the source number. 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | targetOperand | targetOperand represents what is currently in the target. 

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

The resulting string value of the operation.


<br>
<br>

### MoveLeftWithPad([Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

RPG's MOVEL. Moves left an int2 (short) to an int4 (int) with pad.

```cs
MoveLeftWithPad(Int16 num, Int32 targetOperand);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | num | short value of the source. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetOperand | targetOperand represents what is currently in the target. 

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

The resulting int value of the operation.


<br>
<br>

### MoveLeftWithPad([Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16), [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64))

RPG's MOVEL. Moves left an int2 (short) to an int8 (long) with pad.

```cs
MoveLeftWithPad(Int16 num, Int64 targetOperand);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | num | short value of the source. 
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | targetOperand | targetOperand represents what is currently in the target. 

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

The resulting long value of the operation.


<br>
<br>

### MoveLeftWithPad([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64))

RPG's MOVEL. Moves left an int4 (int) to an int8 (long) with pad.

```cs
MoveLeftWithPad(Int32 num, Int64 targetOperand);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | num | int value of the source. 
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | targetOperand | targetOperand represents what is currently in the target. 

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

The resulting long value of the operation.


<br>
<br>

### MoveLeftWithPad([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [IFixedDateTime](/reference/asna-qsys-runtime/classes/i-fixed-date-time.html))

RPG's MOVEL. Moves left a int4 (int) to a datetime with given format and separators with pad.

```cs
MoveLeftWithPad(Int32 num, Runtime.IFixedDateTime dateTime);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | num | int value of the source number. 
| [IFixedDateTime](/reference/asna-qsys-runtime/classes/i-fixed-date-time.html) | dateTime | Date, Time, Timestamp. 

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

The resulting DateTime value of the operation.


<br>
<br>

### MoveLeftWithPad([Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64), [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind](/reference/asna-qsys-runtime/classes/date-time-data-kind.html), [DateTimeFormat](/reference/datagate-client/date-time-format-enumeration.html))

RPG's MOVE. Moves right a int8 (long) to a datetime with given format and separators with pad.

```cs
MoveLeftWithPad(Int64 num, DateTime dateTime, Runtime.DateTimeDataKind dateTimeKind, ASNA.DataGate.Common.DateTimeFormat dateTimeFormat);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | num | long value of the source number. 
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | dateTime | Date, Time, Timestamp. 
| [DateTimeDataKind](/reference/asna-qsys-runtime/classes/date-time-data-kind.html) | dateTimeKind | DateTime Kind. 
| [DateTimeFormat](/reference/datagate-client/date-time-format-enumeration.html) | dateTimeFormat | DateTime Format. 

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

The resulting DateTime value of the operation.


<br>
<br>

### MoveLeftWithPad([Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64), [IFixedDateTime](/reference/asna-qsys-runtime/classes/i-fixed-date-time.html))

RPG's MOVE. Moves right a int8 (long) to a datetime with given format and separators with pad.

```cs
MoveLeftWithPad(Int64 num, Runtime.IFixedDateTime dateTime);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | num | long value of the source number. 
| [IFixedDateTime](/reference/asna-qsys-runtime/classes/i-fixed-date-time.html) | dateTime | Date, Time, Timestamp. 

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

The resulting DateTime value of the operation.


<br>
<br>

### MoveLeftWithPad([Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16), [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

RPG's MOVEL. Moves left an int2 (short) to a decimal with pad.

```cs
MoveLeftWithPad(Int16 num, Decimal targetOperand, Int32 targetOperandDig, Int32 targetOperandDec);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | num | short value of the source number. 
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | targetOperand | targetOperand represents what is currently in the target. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetOperandDig | number of digits in the targetOperand. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetOperandDec | number of decimal places in the targetOperand. 

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

The resulting decimal value of the operation.


<br>
<br>

### MoveLeftWithPad([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

RPG's MOVEL. Moves left an int4 (int) to a decimal with pad.

```cs
MoveLeftWithPad(Int32 num, Decimal targetOperand, Int32 targetOperandDig, Int32 targetOperandDec);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | num | int value of the source number. 
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | targetOperand | targetOperand represents what is currently in the target. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetOperandDig | number of digits in the targetOperand. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetOperandDec | number of decimal places in the targetOperand. 

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

The resulting decimal value of the operation.


<br>
<br>

### MoveLeftWithPad([Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64), [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

RPG's MOVEL. Moves left an int8 (long) to a decimal with pad.

```cs
MoveLeftWithPad(Int64 num, Decimal targetOperand, Int32 targetOperandDig, Int32 targetOperandDec);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | num | long value of the source number. 
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | targetOperand | targetOperand represents what is currently in the target. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetOperandDig | number of digits in the targetOperand. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetOperandDec | number of decimal places in the targetOperand. 

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

The resulting decimal value of the operation.


<br>
<br>

### MoveLeftWithPad([Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

RPG's MOVEL. Moves left int2 (short) to a string with pad.

```cs
MoveLeftWithPad(Int16 num, String targetOperand);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | num | short value of the source number. 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | targetOperand | targetOperand represents what is currently in the target. 

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

The resulting string value of the operation.


<br>
<br>

### MoveLeftWithPad([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

RPG's MOVEL. Moves left int4 (int) to a string with pad.

```cs
MoveLeftWithPad(Int32 num, String targetOperand);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | num | int value of the source number. 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | targetOperand | targetOperand represents what is currently in the target. 

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

The resulting string value of the operation.


<br>
<br>

### MoveRight([Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16), [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind](/reference/asna-qsys-runtime/classes/date-time-data-kind.html), [DateTimeFormat](/reference/datagate-client/date-time-format-enumeration.html))

RPG's MOVE. Moves right a int2 (short) to a datetime with given format and separators.

```cs
MoveRight(Int16 num, DateTime dateTime, Runtime.DateTimeDataKind dateTimeKind, ASNA.DataGate.Common.DateTimeFormat dateTimeFormat);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | num | short value of the source number. 
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | dateTime | Date, Time, Timestamp. 
| [DateTimeDataKind](/reference/asna-qsys-runtime/classes/date-time-data-kind.html) | dateTimeKind | DateTime Kind. 
| [DateTimeFormat](/reference/datagate-client/date-time-format-enumeration.html) | dateTimeFormat | DateTime Format. 

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

The resulting DateTime value of the operation.


<br>
<br>

### MoveRight([Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16), [IFixedDateTime](/reference/asna-qsys-runtime/classes/i-fixed-date-time.html))

RPG's MOVE. Moves right a int2 (short) to a datetime with given format and separators.

```cs
MoveRight(Int16 num, Runtime.IFixedDateTime dateTime);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | num | short value of the source number. 
| [IFixedDateTime](/reference/asna-qsys-runtime/classes/i-fixed-date-time.html) | dateTime | Date, Time, Timestamp. 

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

The resulting DateTime value of the operation.


<br>
<br>

### MoveRight([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind](/reference/asna-qsys-runtime/classes/date-time-data-kind.html), [DateTimeFormat](/reference/datagate-client/date-time-format-enumeration.html))

RPG's MOVE. Moves right a int4 (int) to a datetime with given format and separators.

```cs
MoveRight(Int32 num, DateTime dateTime, Runtime.DateTimeDataKind dateTimeKind, ASNA.DataGate.Common.DateTimeFormat dateTimeFormat);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | num | int value of the source number. 
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | dateTime | Date, Time, Timestamp. 
| [DateTimeDataKind](/reference/asna-qsys-runtime/classes/date-time-data-kind.html) | dateTimeKind | DateTime Kind. 
| [DateTimeFormat](/reference/datagate-client/date-time-format-enumeration.html) | dateTimeFormat | DateTime Format. 

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

The resulting DateTime value of the operation.


<br>
<br>

### MoveRight([Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

RPG's MOVE. Moves right int8 (long) to a string.

```cs
MoveRight(Int64 num, String targetOperand);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | num | long value of the source number. 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | targetOperand | targetOperand represents what is currently in the target. 

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

The resulting string value of the operation.


<br>
<br>

### MoveRight([Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

RPG's MOVE. Moves right an int2 (short) to an int4 (int).

```cs
MoveRight(Int16 num, Int32 targetOperand);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | num | short value of the source. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetOperand | targetOperand represents what is currently in the target. 

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

The resulting int value of the operation.


<br>
<br>

### MoveRight([Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16), [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64))

RPG's MOVE. Moves right an int2 (short) to an int8 (long).

```cs
MoveRight(Int16 num, Int64 targetOperand);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | num | long value of the source. 
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | targetOperand | targetOperand represents what is currently in the target. 

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

The resulting long value of the operation.


<br>
<br>

### MoveRight([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64))

RPG's MOVE. Moves right an int4 (int) to an int8 (long).

```cs
MoveRight(Int32 num, Int64 targetOperand);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | num | int value of the source. 
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | targetOperand | targetOperand represents what is currently in the target. 

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

The resulting long value of the operation.


<br>
<br>

### MoveRight([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16))

RPG's MOVE. Moves right an int4 (int) to an int2 (short).

```cs
MoveRight(Int32 num, Int16 targetOperand);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | num | int value of the source. 
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | targetOperand | targetOperand represents what is currently in the target. 

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

The resulting short value of the operation.


<br>
<br>

### MoveRight([Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64), [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16))

RPG's MOVE. Moves right an int8 (long) to an int2 (short).

```cs
MoveRight(Int64 num, Int16 targetOperand);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | num | long value of the source. 
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | targetOperand | targetOperand represents what is currently in the target. 

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

The resulting short value of the operation.


<br>
<br>

### MoveRight([Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

RPG's MOVE. Moves right an int8 (long) to an int4 (int).

```cs
MoveRight(Int64 num, Int32 targetOperand);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | num | long value of the source. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetOperand | targetOperand represents what is currently in the target. 

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

The resulting int value of the operation.


<br>
<br>

### MoveRight([Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16), [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16))

RPG's MOVE. Moves right an int2 (short) to an int2 (short), this is actually the same as assignment.

```cs
MoveRight(Int16 num, Int16 targetOperand);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | num | short value of the source. 
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | targetOperand | targetOperand represents what is currently in the target. 

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

The resulting short value of the operation.


<br>
<br>

### MoveRight([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

RPG's MOVE. Moves right an int4 (int) to an int4 (int), this is actually the same as assignment.

```cs
MoveRight(Int32 num, Int32 targetOperand);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | num | int value of the source. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetOperand | targetOperand represents what is currently in the target. 

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

The resulting int value of the operation.


<br>
<br>

### MoveRight([Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64), [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64))

RPG's MOVE. Moves right an int8 (long) to an int8 (long), this is actually the same as assignment.

```cs
MoveRight(Int64 num, Int64 targetOperand);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | num | long value of the source. 
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | targetOperand | targetOperand represents what is currently in the target. 

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

The resulting long value of the operation.


<br>
<br>

### MoveRight([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [IFixedDateTime](/reference/asna-qsys-runtime/classes/i-fixed-date-time.html))

RPG's MOVE. Moves right a int4 (int) to a datetime with given format and separators.

```cs
MoveRight(Int32 num, Runtime.IFixedDateTime dateTime);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | num | int value of the source number. 
| [IFixedDateTime](/reference/asna-qsys-runtime/classes/i-fixed-date-time.html) | dateTime | Date, Time, Timestamp. 

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

The resulting DateTime value of the operation.


<br>
<br>

### MoveRight([Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64), [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind](/reference/asna-qsys-runtime/classes/date-time-data-kind.html), [DateTimeFormat](/reference/datagate-client/date-time-format-enumeration.html))

RPG's MOVE. Moves right a int8 (long) to a datetime with given format and separators.

```cs
MoveRight(Int64 num, DateTime dateTime, Runtime.DateTimeDataKind dateTimeKind, ASNA.DataGate.Common.DateTimeFormat dateTimeFormat);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | num | long value of the source number. 
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | dateTime | Date, Time, Timestamp. 
| [DateTimeDataKind](/reference/asna-qsys-runtime/classes/date-time-data-kind.html) | dateTimeKind | DateTime Kind. 
| [DateTimeFormat](/reference/datagate-client/date-time-format-enumeration.html) | dateTimeFormat | DateTime Format. 

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

The resulting DateTime value of the operation.


<br>
<br>

### MoveRight([Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64), [IFixedDateTime](/reference/asna-qsys-runtime/classes/i-fixed-date-time.html))

RPG's MOVE. Moves right a int8 (long) to a datetime with given format and separators.

```cs
MoveRight(Int64 num, Runtime.IFixedDateTime dateTime);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | num | long value of the source number. 
| [IFixedDateTime](/reference/asna-qsys-runtime/classes/i-fixed-date-time.html) | dateTime | Date, Time, Timestamp. 

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

The resulting DateTime value of the operation.


<br>
<br>

### MoveRight([Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16), [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

RPG's MOVE. Moves right an int2 (short) to a decimal.

```cs
MoveRight(Int16 num, Decimal targetOperand, Int32 targetOperandDig, Int32 targetOperandDec);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | num | short value of the source number. 
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | targetOperand | targetOperand represents what is currently in the target. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetOperandDig | number of digits in the targetOperand. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetOperandDec | number of decimal places in the targetOperand. 

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

The resulting decimal value of the operation.


<br>
<br>

### MoveRight([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

RPG's MOVE. Moves right an int4 (int) to a decimal.

```cs
MoveRight(Int32 num, Decimal targetOperand, Int32 targetOperandDig, Int32 targetOperandDec);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | num | int value of the source number. 
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | targetOperand | targetOperand represents what is currently in the target. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetOperandDig | number of digits in the targetOperand. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetOperandDec | number of decimal places in the targetOperand. 

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

The resulting decimal value of the operation.


<br>
<br>

### MoveRight([Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64), [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

RPG's MOVE. Moves right an int8 (long) to a decimal.

```cs
MoveRight(Int64 num, Decimal targetOperand, Int32 targetOperandDig, Int32 targetOperandDec);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | num | long value of the source number. 
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | targetOperand | targetOperand represents what is currently in the target. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetOperandDig | number of digits in the targetOperand. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetOperandDec | number of decimal places in the targetOperand. 

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

The resulting decimal value of the operation.


<br>
<br>

### MoveRight([Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

RPG's MOVE. Moves right int2 (short) to a string.

```cs
MoveRight(Int16 num, String targetOperand);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | num | short value of the source number. 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | targetOperand | targetOperand represents what is currently in the target. 

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

The resulting string value of the operation.


<br>
<br>

### MoveRight([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

RPG's MOVE. Moves right int4 (int) to a string.

```cs
MoveRight(Int32 num, String targetOperand);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | num | int value of the source number. 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | targetOperand | targetOperand represents what is currently in the target. 

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

The resulting string value of the operation.


<br>
<br>

### MoveRightToChar([Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16))

RPG's MOVE. Moves right a short into a character.

```cs
MoveRightToChar(Int16 num);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | num | The short value to move. 

#### Returns

[Char](https://docs.microsoft.com/en-us/dotnet/api/system.char)

The rightmost byte of the short value as a character.


<br>
<br>

### MoveRightToChar([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

RPG's MOVE. Moves right a int into a character.

```cs
MoveRightToChar(Int32 num);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | num | The int value to move. 

#### Returns

[Char](https://docs.microsoft.com/en-us/dotnet/api/system.char)

The rightmost byte of the int value as a character.


<br>
<br>

### MoveRightToChar([Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64))

RPG's MOVE. Moves right a long into a character.

```cs
MoveRightToChar(Int64 num);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | num | The long value to move. 

#### Returns

[Char](https://docs.microsoft.com/en-us/dotnet/api/system.char)

The rightmost byte of the long value as a character.


<br>
<br>

### MoveRightWithPad([Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16), [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind](/reference/asna-qsys-runtime/classes/date-time-data-kind.html), [DateTimeFormat](/reference/datagate-client/date-time-format-enumeration.html))

RPG's MOVE. Moves right a int2 (short) to a datetime with given format and separators with pad.

```cs
MoveRightWithPad(Int16 num, DateTime dateTime, Runtime.DateTimeDataKind dateTimeKind, ASNA.DataGate.Common.DateTimeFormat dateTimeFormat);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | num | short value of the source number. 
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | dateTime | Date, Time, Timestamp. 
| [DateTimeDataKind](/reference/asna-qsys-runtime/classes/date-time-data-kind.html) | dateTimeKind | DateTime Kind. 
| [DateTimeFormat](/reference/datagate-client/date-time-format-enumeration.html) | dateTimeFormat | DateTime Format. 

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

The resulting DateTime value of the operation.


<br>
<br>

### MoveRightWithPad([Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16), [IFixedDateTime](/reference/asna-qsys-runtime/classes/i-fixed-date-time.html))

RPG's MOVE. Moves right a int2 (short) to a datetime with given format and separators with pad.

```cs
MoveRightWithPad(Int16 num, Runtime.IFixedDateTime dateTime);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | num | short value of the source number. 
| [IFixedDateTime](/reference/asna-qsys-runtime/classes/i-fixed-date-time.html) | dateTime | Date, Time, Timestamp. 

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

The resulting DateTime value of the operation.


<br>
<br>

### MoveRightWithPad([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind](/reference/asna-qsys-runtime/classes/date-time-data-kind.html), [DateTimeFormat](/reference/datagate-client/date-time-format-enumeration.html))

RPG's MOVE. Moves right a int4 (int) to a datetime with given format and separators with pad.

```cs
MoveRightWithPad(Int32 num, DateTime dateTime, Runtime.DateTimeDataKind dateTimeKind, ASNA.DataGate.Common.DateTimeFormat dateTimeFormat);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | num | int value of the source number. 
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | dateTime | Date, Time, Timestamp. 
| [DateTimeDataKind](/reference/asna-qsys-runtime/classes/date-time-data-kind.html) | dateTimeKind | DateTime Kind. 
| [DateTimeFormat](/reference/datagate-client/date-time-format-enumeration.html) | dateTimeFormat | DateTime Format. 

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

The resulting DateTime value of the operation.


<br>
<br>

### MoveRightWithPad([Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

RPG's MOVE. Moves right int8 (long) to a string with pad.

```cs
MoveRightWithPad(Int64 num, String targetOperand);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | num | long value of the source number. 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | targetOperand | targetOperand represents what is currently in the target. 

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

The resulting string value of the operation.


<br>
<br>

### MoveRightWithPad([Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

RPG's MOVE. Moves right an int2 (short) to an int4 (int) with pad.

```cs
MoveRightWithPad(Int16 num, Int32 targetOperand);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | num | short value of the source. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetOperand | targetOperand represents what is currently in the target. 

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

The resulting int value of the operation.


<br>
<br>

### MoveRightWithPad([Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16), [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64))

RPG's MOVE. Moves right an int2 (short) to an int8 (long) with pad.

```cs
MoveRightWithPad(Int16 num, Int64 targetOperand);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | num | long value of the source. 
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | targetOperand | targetOperand represents what is currently in the target. 

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

The resulting long value of the operation.


<br>
<br>

### MoveRightWithPad([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64))

RPG's MOVE. Moves right an int4 (int) to an int8 (long) with pad.

```cs
MoveRightWithPad(Int32 num, Int64 targetOperand);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | num | int value of the source. 
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | targetOperand | targetOperand represents what is currently in the target. 

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

The resulting long value of the operation.


<br>
<br>

### MoveRightWithPad([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [IFixedDateTime](/reference/asna-qsys-runtime/classes/i-fixed-date-time.html))

RPG's MOVE. Moves right a int4 (int) to a datetime with given format and separators with pad.

```cs
MoveRightWithPad(Int32 num, Runtime.IFixedDateTime dateTime);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | num | int value of the source number. 
| [IFixedDateTime](/reference/asna-qsys-runtime/classes/i-fixed-date-time.html) | dateTime | Date, Time, Timestamp. 

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

The resulting DateTime value of the operation.


<br>
<br>

### MoveRightWithPad([Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64), [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind](/reference/asna-qsys-runtime/classes/date-time-data-kind.html), [DateTimeFormat](/reference/datagate-client/date-time-format-enumeration.html))

RPG's MOVE. Moves right a int8 (long) to a datetime with given format and separators with pad.

```cs
MoveRightWithPad(Int64 num, DateTime dateTime, Runtime.DateTimeDataKind dateTimeKind, ASNA.DataGate.Common.DateTimeFormat dateTimeFormat);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | num | long value of the source number. 
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | dateTime | Date, Time, Timestamp. 
| [DateTimeDataKind](/reference/asna-qsys-runtime/classes/date-time-data-kind.html) | dateTimeKind | DateTime Kind. 
| [DateTimeFormat](/reference/datagate-client/date-time-format-enumeration.html) | dateTimeFormat | DateTime Format. 

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

The resulting DateTime value of the operation.


<br>
<br>

### MoveRightWithPad([Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64), [IFixedDateTime](/reference/asna-qsys-runtime/classes/i-fixed-date-time.html))

RPG's MOVE. Moves right a int8 (long) to a datetime with given format and separators with pad.

```cs
MoveRightWithPad(Int64 num, Runtime.IFixedDateTime dateTime);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | num | long value of the source number. 
| [IFixedDateTime](/reference/asna-qsys-runtime/classes/i-fixed-date-time.html) | dateTime | Date, Time, Timestamp. 

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

The resulting DateTime value of the operation.


<br>
<br>

### MoveRightWithPad([Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16), [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

RPG's MOVE. Moves right an int2 (short) to a decimal with pad.

```cs
MoveRightWithPad(Int16 num, Decimal targetOperand, Int32 targetOperandDig, Int32 targetOperandDec);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | num | short value of the source number. 
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | targetOperand | targetOperand represents what is currently in the target. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetOperandDig | number of digits in the targetOperand. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetOperandDec | number of decimal places in the targetOperand. 

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

The resulting decimal value of the operation.


<br>
<br>

### MoveRightWithPad([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

RPG's MOVE. Moves right an int4 (int) to a decimal with pad.

```cs
MoveRightWithPad(Int32 num, Decimal targetOperand, Int32 targetOperandDig, Int32 targetOperandDec);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | num | int value of the source number. 
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | targetOperand | targetOperand represents what is currently in the target. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetOperandDig | number of digits in the targetOperand. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetOperandDec | number of decimal places in the targetOperand. 

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

The resulting decimal value of the operation.


<br>
<br>

### MoveRightWithPad([Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64), [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

RPG's MOVE. Moves right an int8 (long) to a decimal with pad.

```cs
MoveRightWithPad(Int64 num, Decimal targetOperand, Int32 targetOperandDig, Int32 targetOperandDec);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | num | long value of the source number. 
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | targetOperand | targetOperand represents what is currently in the target. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetOperandDig | number of digits in the targetOperand. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetOperandDec | number of decimal places in the targetOperand. 

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

The resulting decimal value of the operation.


<br>
<br>

### MoveRightWithPad([Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

RPG's MOVE. Moves right int2 (short) to a string with pad.

```cs
MoveRightWithPad(Int16 num, String targetOperand);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | num | short value of the source number. 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | targetOperand | targetOperand represents what is currently in the target. 

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

The resulting string value of the operation.


<br>
<br>

### MoveRightWithPad([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

RPG's MOVE. Moves right int4 (int) to a string with pad.

```cs
MoveRightWithPad(Int32 num, String targetOperand);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | num | int value of the source number. 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | targetOperand | targetOperand represents what is currently in the target. 

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

The resulting string value of the operation.


<br>
<br>

### SetHiLoEq([Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16), [Indicator](/reference/asna-qsys-runtime/classes/indicator.html), [Indicator](/reference/asna-qsys-runtime/classes/indicator.html), [Indicator](/reference/asna-qsys-runtime/classes/indicator.html))

Sets the HI, LO, and EQ flags passed in, based on the value of num.

```cs
SetHiLoEq(Int16 num, out ASNA.QSys.Runtime.Indicator hi, out ASNA.QSys.Runtime.Indicator lo, out ASNA.QSys.Runtime.Indicator eq);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | num | The number to test. 
| [Indicator](/reference/asna-qsys-runtime/classes/indicator.html) | hi | The greater-than-zero flag. 
| [Indicator](/reference/asna-qsys-runtime/classes/indicator.html) | lo | The less-than-zero flag. 
| [Indicator](/reference/asna-qsys-runtime/classes/indicator.html) | eq | The equal flag. 

#### Returns

[Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16)

The same value that was passed in in num.


<br>
<br>

### SetHiLoEq([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Indicator](/reference/asna-qsys-runtime/classes/indicator.html), [Indicator](/reference/asna-qsys-runtime/classes/indicator.html), [Indicator](/reference/asna-qsys-runtime/classes/indicator.html))

Sets the HI, LO, and EQ flags passed in, based on the value of num.

```cs
SetHiLoEq(Int32 num, out ASNA.QSys.Runtime.Indicator hi, out ASNA.QSys.Runtime.Indicator lo, out ASNA.QSys.Runtime.Indicator eq);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | num | The number to test. 
| [Indicator](/reference/asna-qsys-runtime/classes/indicator.html) | hi | The greater-than-zero flag. 
| [Indicator](/reference/asna-qsys-runtime/classes/indicator.html) | lo | The less-than-zero flag. 
| [Indicator](/reference/asna-qsys-runtime/classes/indicator.html) | eq | The equal flag. 

#### Returns

[Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16)

The same value that was passed in in num.


<br>
<br>

### SetHiLoEq([Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64), [Indicator](/reference/asna-qsys-runtime/classes/indicator.html), [Indicator](/reference/asna-qsys-runtime/classes/indicator.html), [Indicator](/reference/asna-qsys-runtime/classes/indicator.html))

Sets the HI, LO, and EQ flags passed in, based on the value of num.

```cs
SetHiLoEq(Int64 num, out ASNA.QSys.Runtime.Indicator hi, out ASNA.QSys.Runtime.Indicator lo, out ASNA.QSys.Runtime.Indicator eq);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | num | The number to test. 
| [Indicator](/reference/asna-qsys-runtime/classes/indicator.html) | hi | The greater-than-zero flag. 
| [Indicator](/reference/asna-qsys-runtime/classes/indicator.html) | lo | The less-than-zero flag. 
| [Indicator](/reference/asna-qsys-runtime/classes/indicator.html) | eq | The equal flag. 

#### Returns

[Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16)

The same value that was passed in in num.


<br>
<br>

### Sum([Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16))

Returns the added values of each element in the array.

```cs
Sum(Int16[] array);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | array | The array whose elements will be summed. 

#### Returns

[Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16)

The added value of every element in the array.


<br>
<br>

### Sum([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

Returns the added values of each element in the array.

```cs
Sum(Int32[] array);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | array | The array whose elements will be summed. 

#### Returns

[Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16)

The added value of every element in the array.


<br>
<br>

### Sum([Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64))

Returns the added values of each element in the array.

```cs
Sum(Int64[] array);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | array | The array whose elements will be summed. 

#### Returns

[Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16)

The added value of every element in the array.


<br>
<br>

### TestTime([Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16), [DateTimeDataKind](/reference/asna-qsys-runtime/classes/date-time-data-kind.html), [DateTimeFormat](/reference/datagate-client/date-time-format-enumeration.html))

Tests whether a short contains a valid date/time/timestamp value.

```cs
TestTime(Int16 num, Runtime.DateTimeDataKind kind, ASNA.DataGate.Common.DateTimeFormat format);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | num | The short number to test. 
| [DateTimeDataKind](/reference/asna-qsys-runtime/classes/date-time-data-kind.html) | kind | whether the number represents a date, time, or timestamp. 
| [DateTimeFormat](/reference/datagate-client/date-time-format-enumeration.html) | format | The date/time/timestamp format in which the number is. 

#### Returns

[Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)

True if the number represents a valid date/time/timestamp value in the given format. False otherwise.


<br>
<br>

### TestTime([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [DateTimeDataKind](/reference/asna-qsys-runtime/classes/date-time-data-kind.html), [DateTimeFormat](/reference/datagate-client/date-time-format-enumeration.html))

Tests whether an int number contains a valid date/time/timestamp value.

```cs
TestTime(Int32 num, Runtime.DateTimeDataKind kind, ASNA.DataGate.Common.DateTimeFormat format);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | num | The int number to test. 
| [DateTimeDataKind](/reference/asna-qsys-runtime/classes/date-time-data-kind.html) | kind | whether the number represents a date, time, or timestamp. 
| [DateTimeFormat](/reference/datagate-client/date-time-format-enumeration.html) | format | The date/time/timestamp format in which the number is. 

#### Returns

[Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)

True if the number represents a valid date/time/timestamp value in the given format. False otherwise.


<br>
<br>

### TestTime([Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64), [DateTimeDataKind](/reference/asna-qsys-runtime/classes/date-time-data-kind.html), [DateTimeFormat](/reference/datagate-client/date-time-format-enumeration.html))

Tests whether a long number contains a valid date/time/timestamp value.

```cs
TestTime(Int64 num, Runtime.DateTimeDataKind kind, ASNA.DataGate.Common.DateTimeFormat format);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | num | The long number to test. 
| [DateTimeDataKind](/reference/asna-qsys-runtime/classes/date-time-data-kind.html) | kind | whether the number represents a date, time, or timestamp. 
| [DateTimeFormat](/reference/datagate-client/date-time-format-enumeration.html) | format | The date/time/timestamp format in which the number is. 

#### Returns

[Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)

True if the number represents a valid date/time/timestamp value in the given format. False otherwise.


<br>
<br>

### ToDate([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [DateTimeFormat](/reference/datagate-client/date-time-format-enumeration.html))

ToDate summary.

```cs
ToDate(Int32 source, ASNA.DataGate.Common.DateTimeFormat format);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | source | ToDate source param. 
| [DateTimeFormat](/reference/datagate-client/date-time-format-enumeration.html) | format | ToDate format param. 

#### Returns

[DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime)

ToDate returns.


<br>
<br>

### ToDate([Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16), [DateTimeFormat](/reference/datagate-client/date-time-format-enumeration.html))

ToDate summary.

```cs
ToDate(Int16 source, ASNA.DataGate.Common.DateTimeFormat format);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | source | ToDate source param. 
| [DateTimeFormat](/reference/datagate-client/date-time-format-enumeration.html) | format | ToDate format param. 

#### Returns

[DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime)

returns param.


<br>
<br>

### ToDate([Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64), [DateTimeFormat](/reference/datagate-client/date-time-format-enumeration.html))

ToDate summary.

```cs
ToDate(Int64 source, ASNA.DataGate.Common.DateTimeFormat format);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | source | ToDate source param. 
| [DateTimeFormat](/reference/datagate-client/date-time-format-enumeration.html) | format | ToDate format param. 

#### Returns

[DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime)

ToDate returns.


<br>
<br>

### ToFixedDecimal([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

Adjusts the digits and decimal positions of a fixed decimal number using Away From Zero rounding.

```cs
ToFixedDecimal(Int32 num, Int32 digits, Int32 decimals);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | num |  The decimal number to round up. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | digits | The desired number of digits. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | decimals | The desired number of decimal positions. 

#### Returns

[Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal)

The decimal equivalent of num, adjusted to the given number of digits and decimal positions..


<br>
<br>

### ToFixedDecimalRounded([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

Adjusts the digits and decimal positions of a fixed decimal number using Away From Zero rounding.

```cs
ToFixedDecimalRounded(Int32 num, Int32 digits, Int32 decimals);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | num |  The decimal number to round up. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | digits | The desired number of digits. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | decimals | The desired number of decimal positions. 

#### Returns

[Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal)

The decimal equivalent of num, adjusted to the given number of digits and decimal positions..


<br>
<br>

### ToStringByte([Byte](https://docs.microsoft.com/en-us/dotnet/api/system.byte))

Returns as a string the char equivalent of a byte number.

```cs
ToStringByte(Byte num);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Byte](https://docs.microsoft.com/en-us/dotnet/api/system.byte) | num | The short number to convert. 

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

The string resulting from interpreting the byte value as a character.


<br>
<br>

### ToStringInt([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

Returns as a string the char equivalent of a int number.

```cs
ToStringInt(Int32 num);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | num | The int number to convert. 

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

The string resulting from interpreting the bytes of the int value as characters.


<br>
<br>

### ToStringLong([Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64))

Returns as a string the char equivalentof a long number.

```cs
ToStringLong(Int64 num);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | num | The long number to convert. 

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

The string resulting from interpreting the bytes of the long value as characters.


<br>
<br>

### ToStringShort([Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16))

Returns as a string the char equivalent of a short number.

```cs
ToStringShort(Int16 num);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | num | The short number to convert. 

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

The string resulting from interpreting the bytes of the short value as characters.


<br>
<br>

### ToTime([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [DateTimeFormat](/reference/datagate-client/date-time-format-enumeration.html))

ToTime summary.

```cs
ToTime(Int32 source, ASNA.DataGate.Common.DateTimeFormat format);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | source | ToTime source param. 
| [DateTimeFormat](/reference/datagate-client/date-time-format-enumeration.html) | format | ToTime format param. 

#### Returns

[DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime)

ToTime returns.


<br>
<br>

### ToTime([Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16), [DateTimeFormat](/reference/datagate-client/date-time-format-enumeration.html))

ToTime summary.

```cs
ToTime(Int16 source, ASNA.DataGate.Common.DateTimeFormat format);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | source | ToTime source param. 
| [DateTimeFormat](/reference/datagate-client/date-time-format-enumeration.html) | format | ToTime format param. 

#### Returns

[DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime)

ToTime returns.


<br>
<br>

### ToTime([Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64), [DateTimeFormat](/reference/datagate-client/date-time-format-enumeration.html))

ToTime summary.

```cs
ToTime(Int64 source, ASNA.DataGate.Common.DateTimeFormat format);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | source | ToTime source param. 
| [DateTimeFormat](/reference/datagate-client/date-time-format-enumeration.html) | format | ToTime format param. 

#### Returns

[DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime)

ToTime returns.


<br>
<br>

### ToTimestamp([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

ToTimestamp summary.

```cs
ToTimestamp(Int32 source);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | source | ToTimestamp sourceparam. 

#### Returns

[DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime)

ToTimestamp returns.


<br>
<br>

### ToTimestamp([Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16))

ToTimestamp summary.

```cs
ToTimestamp(Int16 source);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | source | ToTimestamp source param. 

#### Returns

[DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime)

ToTimestamp returns.


<br>
<br>

### ToTimestamp([Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64))

ToTimestamp summary.

```cs
ToTimestamp(Int64 source);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | source | ToTimestamp source param. 

#### Returns

[DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime)

ToTimestamp returns


<br>
<br>

