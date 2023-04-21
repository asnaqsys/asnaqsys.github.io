---
title: DateTimeMethods Class
---

Contains extension methods for handling Date/Time/Timestamp conversions.

**Namespace:** ASNA.QSys.Runtime <br/>
**Assembly:** ASNA.QSys.Runtime

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> DateTimeMethods

<br>
<br>

## Remarks

Contains extension methods for handling Date/Time/Timestamp conversions.

[//]: # ($$TODO: Complete the Remarks section.)

<br>
<br>

## Methods

| Type | Name | Description | Return Description 
| --- | --- | --- | --- 
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | [AddDuration](#adddurationdatetime-double-durationcode)([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [Double]($$TODO-Double.html), [DurationCode](/reference/asna-qsys-runtime/date-time-ops-duration-code.html)) | Adds a duration span to a date or a timestamp value. | The resulting Date or Timestamp value after adding to it the given duration.
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | [AddDurationToTime](#adddurationtotimedatetime-double-durationcode)([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [Double]($$TODO-Double.html), [DurationCode](/reference/asna-qsys-runtime/date-time-ops-duration-code.html)) | Adds a duration span to a time value. | .
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | [Equals](https://docs.microsoft.com/en-us/dotnet/api/system.object.equals)([Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | Determines whether the specified object is equal to the current object.<br>(Inherited from [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | true if the specified object is equal to the current object; otherwise, false.
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [Finalize](https://docs.microsoft.com/en-us/dotnet/api/system.object.finalize)() | Allows an object to try to free resources and perform other cleanup operations before it is reclaimed by garbage collection.<br>(Inherited from [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | [GetFormatLength](#getformatlengthdatetimedatakind-datetimeformat-datetimeseparator)([DateTimeDataKind](/reference/asna-qsys-runtime/date-time-data-kind.html), [DateTimeFormat]($$TODO-ASNA.DataGate.Common.DateTimeFormat.html), [DateTimeSeparator](/reference/asna-qsys-runtime/classes/date-time-separator.html)) | Returns the length of the string representation of a date/time/timestamp type. | The computed length.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | [GetHashCode](https://docs.microsoft.com/en-us/dotnet/api/system.object.gethashcode)() | Serves as the default hash function.<br>(Inherited from [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | A hash code for the current object.
| [Type](https://docs.microsoft.com/en-us/dotnet/api/system.type) | [GetType](https://docs.microsoft.com/en-us/dotnet/api/system.object.gettype)() | Gets the Type of the current instance.<br>(Inherited from [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | The exact runtime type of the current instance.
| [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) | [MemberwiseClone](https://docs.microsoft.com/en-us/dotnet/api/system.object.memberwiseclone)() | Creates a shallow copy of the current Object.<br>(Inherited from [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | A shallow copy of the current Object.
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | [MergeDate](#mergedatedatetime-datetime)([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime)) | Merges a date into the date part of a timeStamp. | .NET DateTime value.
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | [MergeTime](#mergetimedatetime-datetime)([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime)) | Merges a time into the time part of a timeStamp. | .NET DateTime value.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [MoveLeft](#moveleftdatetime-datetimedatakind-datetimeformat-datetimeseparator-string)([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind](/reference/asna-qsys-runtime/date-time-data-kind.html), [DateTimeFormat]($$TODO-ASNA.DataGate.Common.DateTimeFormat.html), [DateTimeSeparator](/reference/asna-qsys-runtime/classes/date-time-separator.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | RPG's MOVEL. Moves left a DateTime to string. | The string resulting from the MOVEL operation of the dateTime with the given format and separator into the targetOperand string.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [MoveLeft](#moveleftdatetime-datetimedatakind-datetimeformat-decimal-int32-int32)([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind](/reference/asna-qsys-runtime/date-time-data-kind.html), [DateTimeFormat]($$TODO-ASNA.DataGate.Common.DateTimeFormat.html), [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's MOVEL. Moves left a DateTime to decimal. | returns a decimal value of the targetOperand.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [MoveLeft](#moveleftdatetime-datetimedatakind-datetimeformat-int16)([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind](/reference/asna-qsys-runtime/date-time-data-kind.html), [DateTimeFormat]($$TODO-ASNA.DataGate.Common.DateTimeFormat.html), [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16)) | RPG's MOVEL. Moves left a datetime into a int2 (short). | short int targetOperand of the move.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [MoveLeft](#moveleftdatetime-datetimedatakind-datetimeformat-int32)([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind](/reference/asna-qsys-runtime/date-time-data-kind.html), [DateTimeFormat]($$TODO-ASNA.DataGate.Common.DateTimeFormat.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's MOVEL. Moves left a datetime into a int4 (int). | int targetOperand of the move.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [MoveLeft](#moveleftdatetime-datetimedatakind-datetimeformat-int64)([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind](/reference/asna-qsys-runtime/date-time-data-kind.html), [DateTimeFormat]($$TODO-ASNA.DataGate.Common.DateTimeFormat.html), [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64)) | RPG's MOVEL. Moves left a datetime into a int8 (long). | long targetOperand of the move.
| [Char](https://docs.microsoft.com/en-us/dotnet/api/system.char) | [MoveLeftToChar](#movelefttochardatetime-datetimedatakind-datetimeformat)([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind](/reference/asna-qsys-runtime/date-time-data-kind.html), [DateTimeFormat]($$TODO-ASNA.DataGate.Common.DateTimeFormat.html)) | RPG's MOVEL. Moves left a date, time, timestamp in the given format to a char value. | .
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [MoveLeftWithPad](#moveleftwithpaddatetime-datetimedatakind-datetimeformat-datetimeseparator-string)([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind](/reference/asna-qsys-runtime/date-time-data-kind.html), [DateTimeFormat]($$TODO-ASNA.DataGate.Common.DateTimeFormat.html), [DateTimeSeparator](/reference/asna-qsys-runtime/classes/date-time-separator.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | RPG's MOVEL. Moves left a DateTime to string with pad. | The string resulting from the MOVEL operation of the dateTime with the given format and separator into the targetOperand string.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [MoveLeftWithPad](#moveleftwithpaddatetime-datetimedatakind-datetimeformat-decimal-int32-int32)([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind](/reference/asna-qsys-runtime/date-time-data-kind.html), [DateTimeFormat]($$TODO-ASNA.DataGate.Common.DateTimeFormat.html), [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's MOVEL. Moves left a DateTime to decimal with pad. | returns a decimal value of the targetOperand.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [MoveLeftWithPad](#moveleftwithpaddatetime-datetimedatakind-datetimeformat-int16)([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind](/reference/asna-qsys-runtime/date-time-data-kind.html), [DateTimeFormat]($$TODO-ASNA.DataGate.Common.DateTimeFormat.html), [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16)) | RPG's MOVE. Moves right a datetime into a int2 (short) with pad. | short int targetOperand of the move.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [MoveLeftWithPad](#moveleftwithpaddatetime-datetimedatakind-datetimeformat-int32)([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind](/reference/asna-qsys-runtime/date-time-data-kind.html), [DateTimeFormat]($$TODO-ASNA.DataGate.Common.DateTimeFormat.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's MOVEL. Moves left a datetime into a int4 (int). | int targetOperand of the move.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [MoveLeftWithPad](#moveleftwithpaddatetime-datetimedatakind-datetimeformat-int64)([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind](/reference/asna-qsys-runtime/date-time-data-kind.html), [DateTimeFormat]($$TODO-ASNA.DataGate.Common.DateTimeFormat.html), [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64)) | RPG's MOVEL. Moves left a datetime into a int8 (long). | long targetOperand of the move.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [MoveRight](#moverightdatetime-datetimedatakind-datetimeformat-datetimeseparator-string)([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind](/reference/asna-qsys-runtime/date-time-data-kind.html), [DateTimeFormat]($$TODO-ASNA.DataGate.Common.DateTimeFormat.html), [DateTimeSeparator](/reference/asna-qsys-runtime/classes/date-time-separator.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | RPG's MOVE. Moves right a DateTime to string. | The string resulting from the MOVE operation of the dateTime with the given format and separator into the targetOperand string.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [MoveRight](#moverightdatetime-datetimedatakind-datetimeformat-decimal-int32-int32)([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind](/reference/asna-qsys-runtime/date-time-data-kind.html), [DateTimeFormat]($$TODO-ASNA.DataGate.Common.DateTimeFormat.html), [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's MOVE. Moves right s DateTime to decimal. | The decimal number resulting from the MOVE operation of the dateTime with the given format and separator into the targetOperand number.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [MoveRight](#moverightdatetime-datetimedatakind-datetimeformat-int16)([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind](/reference/asna-qsys-runtime/date-time-data-kind.html), [DateTimeFormat]($$TODO-ASNA.DataGate.Common.DateTimeFormat.html), [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16)) | RPG's MOVE. Moves right a datetime into a int2 (short). | short int targetOperand of the move.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [MoveRight](#moverightdatetime-datetimedatakind-datetimeformat-int32)([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind](/reference/asna-qsys-runtime/date-time-data-kind.html), [DateTimeFormat]($$TODO-ASNA.DataGate.Common.DateTimeFormat.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's MOVE. Moves right a datetime into a int4 (int). | int targetOperand of the move.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [MoveRight](#moverightdatetime-datetimedatakind-datetimeformat-int64)([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind](/reference/asna-qsys-runtime/date-time-data-kind.html), [DateTimeFormat]($$TODO-ASNA.DataGate.Common.DateTimeFormat.html), [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64)) | RPG's MOVE. Moves right a datetime into a int8 (long). | long targetOperand of the move.
| [Char](https://docs.microsoft.com/en-us/dotnet/api/system.char) | [MoveRightToChar](#moverighttochardatetime-datetimedatakind-datetimeformat)([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind](/reference/asna-qsys-runtime/date-time-data-kind.html), [DateTimeFormat]($$TODO-ASNA.DataGate.Common.DateTimeFormat.html)) | RPG's MOVE. Moves right a date, time, timestamp in the given format to a char value. | .
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [MoveRightWithPad](#moverightwithpaddatetime-datetimedatakind-datetimeformat-datetimeseparator-string)([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind](/reference/asna-qsys-runtime/date-time-data-kind.html), [DateTimeFormat]($$TODO-ASNA.DataGate.Common.DateTimeFormat.html), [DateTimeSeparator](/reference/asna-qsys-runtime/classes/date-time-separator.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | RPG's MOVE. Moves right a DateTime to string with pad. | The string resulting from the MOVE operation of the dateTime with the given format and separator into the targetOperand string.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [MoveRightWithPad](#moverightwithpaddatetime-datetimedatakind-datetimeformat-decimal-int32-int32)([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind](/reference/asna-qsys-runtime/date-time-data-kind.html), [DateTimeFormat]($$TODO-ASNA.DataGate.Common.DateTimeFormat.html), [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's MOVE. Moves right a DateTime to decimal with pad. | The decimal number resulting from the MOVE operation of the dateTime with the given format and separator into the targetOperand number.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [MoveRightWithPad](#moverightwithpaddatetime-datetimedatakind-datetimeformat-int16)([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind](/reference/asna-qsys-runtime/date-time-data-kind.html), [DateTimeFormat]($$TODO-ASNA.DataGate.Common.DateTimeFormat.html), [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16)) | RPG's MOVE. Moves right a datetime into a int2 (short) with pad. | short int targetOperand of the move.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [MoveRightWithPad](#moverightwithpaddatetime-datetimedatakind-datetimeformat-int32)([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind](/reference/asna-qsys-runtime/date-time-data-kind.html), [DateTimeFormat]($$TODO-ASNA.DataGate.Common.DateTimeFormat.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's MOVE. Moves right a datetime into a int4 (int) with pad. | int targetOperand of the move.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [MoveRightWithPad](#moverightwithpaddatetime-datetimedatakind-datetimeformat-int64)([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind](/reference/asna-qsys-runtime/date-time-data-kind.html), [DateTimeFormat]($$TODO-ASNA.DataGate.Common.DateTimeFormat.html), [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64)) | RPG's MOVE. Moves right a datetime into a int8 (long) with pad. | long targetOperand of the move.
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | [NormalizeYear](#normalizeyeardatetime)([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime)) | Turns a 4 digit year into a 2 digit year between 1940 and 2039 | .NET DateTime value.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | [ReferenceEquals](https://docs.microsoft.com/en-us/dotnet/api/system.object.referenceequals)([Object](https://docs.microsoft.com/en-us/dotnet/api/system.object), [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | Determines whether the specified Object instances are the same instance.<br>(Inherited from [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | true if objA is the same instance as objB or if both are null; otherwise, false.
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | [SubtractDuration](#subtractdurationdatetime-double-durationcode)([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [Double]($$TODO-Double.html), [DurationCode](/reference/asna-qsys-runtime/date-time-ops-duration-code.html)) | Subtracts a duration span from a date or a timestamp value. | .
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | [SubtractDurationFromTime](#subtractdurationfromtimedatetime-double-durationcode)([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [Double]($$TODO-Double.html), [DurationCode](/reference/asna-qsys-runtime/date-time-ops-duration-code.html)) | Subtracts a duration span from a time value. | .
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | [TimestampToDate](#timestamptodatedatetime)([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime)) | Returns the Date portion of a timestamp. | The Date portion as a DateTime value.
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | [TimestampToTime](#timestamptotimedatetime)([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime)) | Returns the hours, minutes, and seconds of a timestamp. | The Time portion in hours, minutes, and seconds as a DateTime value.
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | [TimestampToUSATime](#timestamptousatimedatetime)([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime)) | Returns the hours and minutes of a timestamp. | The Time portion in hours and minutes only as a DateTime value.
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | [ToFixedDecimal](#tofixeddecimaldatetime-datetimedatakind-datetimeformat-int32-int32)([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind](/reference/asna-qsys-runtime/date-time-data-kind.html), [DateTimeFormat]($$TODO-ASNA.DataGate.Common.DateTimeFormat.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Converts a dateTime type, converts it to a decmial. | The decimal number that results from the conversion.
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | [ToFixedDecimal](#tofixeddecimaldatetime-datetimedatakind-datetimeformat)([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind](/reference/asna-qsys-runtime/date-time-data-kind.html), [DateTimeFormat]($$TODO-ASNA.DataGate.Common.DateTimeFormat.html)) | Converts a dateTime type to decimal. | The decimal number that results from the conversion.
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | [ToInt16](#toint16datetime-datetimedatakind-datetimeformat-boolean)([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind](/reference/asna-qsys-runtime/date-time-data-kind.html), [DateTimeFormat]($$TODO-ASNA.DataGate.Common.DateTimeFormat.html), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Converts a dateTime type to int 16. | The Int16 number that results from the conversion.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | [ToInt32](#toint32datetime-datetimedatakind-datetimeformat-boolean)([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind](/reference/asna-qsys-runtime/date-time-data-kind.html), [DateTimeFormat]($$TODO-ASNA.DataGate.Common.DateTimeFormat.html), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Converts a dateTime type to int 32. | The Int32 number that results from the conversion.
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | [ToInt64](#toint64datetime-datetimedatakind-datetimeformat-boolean)([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind](/reference/asna-qsys-runtime/date-time-data-kind.html), [DateTimeFormat]($$TODO-ASNA.DataGate.Common.DateTimeFormat.html), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Converts a dateTime type to int 64. | The Int64 number that results from the conversion.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [ToString](#tostringdatetime-datetimedatakind-datetimeformat-datetimeseparator)([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind](/reference/asna-qsys-runtime/date-time-data-kind.html), [DateTimeFormat]($$TODO-ASNA.DataGate.Common.DateTimeFormat.html), [DateTimeSeparator](/reference/asna-qsys-runtime/classes/date-time-separator.html)) | Converts a DateTime with the specified Kind and Format to a string using the specified separator. | A string representation of a DateTime in the given format using the specified separator.

<br>
<br>

### AddDuration([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [Double]($$TODO-Double.html), [DurationCode](/reference/asna-qsys-runtime/date-time-ops-duration-code.html))

Adds a duration span to a date or a timestamp value.

```cs
AddDuration(DateTime dateTime, Double duration, ASNA.QSys.Runtime.DateTimeOps.DurationCode durationCode);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | dateTime | .NET DateTime value. 
| [Double]($$TODO-Double.html) | duration | A double value representing duration. 
| [DurationCode](/reference/asna-qsys-runtime/date-time-ops-duration-code.html) | durationCode | Code determining what duration represents. 

#### Returns

[DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime)

The resulting Date or Timestamp value after adding to it the given duration.


<br>
<br>

### AddDurationToTime([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [Double]($$TODO-Double.html), [DurationCode](/reference/asna-qsys-runtime/date-time-ops-duration-code.html))

Adds a duration span to a time value.

```cs
AddDurationToTime(DateTime dateTime, Double duration, ASNA.QSys.Runtime.DateTimeOps.DurationCode durationCode);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | dateTime | .NET DateTime value specifying a time value. 
| [Double]($$TODO-Double.html) | duration | A double value representing duration. 
| [DurationCode](/reference/asna-qsys-runtime/date-time-ops-duration-code.html) | durationCode | Code determining what duration represents. 

#### Returns

[DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime)

.


<br>
<br>

### GetFormatLength([DateTimeDataKind](/reference/asna-qsys-runtime/date-time-data-kind.html), [DateTimeFormat]($$TODO-ASNA.DataGate.Common.DateTimeFormat.html), [DateTimeSeparator](/reference/asna-qsys-runtime/classes/date-time-separator.html))

Returns the length of the string representation of a date/time/timestamp type.

```cs
GetFormatLength(ASNA.QSys.Runtime.DateTimeDataKind kind, ASNA.DataGate.Common.DateTimeFormat format, ASNA.QSys.Runtime.DateTimeSeparator separator);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DateTimeDataKind](/reference/asna-qsys-runtime/date-time-data-kind.html) | kind | The kind of datetime type. 
| [DateTimeFormat]($$TODO-ASNA.DataGate.Common.DateTimeFormat.html) | format | The format of the type. 
| [DateTimeSeparator](/reference/asna-qsys-runtime/classes/date-time-separator.html) | separator | The datetime separator. 

#### Returns

[Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)

The computed length.


<br>
<br>

### MergeDate([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime))

Merges a date into the date part of a timeStamp.

```cs
MergeDate(DateTime timeStamp, DateTime date);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | timeStamp | timeStamp to be merged. 
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | date | date to merge. 

#### Returns

[DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime)

.NET DateTime value.


<br>
<br>

### MergeTime([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime))

Merges a time into the time part of a timeStamp.

```cs
MergeTime(DateTime timeStamp, DateTime time);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | timeStamp | timeStamp to be merged. 
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | time | time to merge. 

#### Returns

[DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime)

.NET DateTime value.


<br>
<br>

### MoveLeft([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind](/reference/asna-qsys-runtime/date-time-data-kind.html), [DateTimeFormat]($$TODO-ASNA.DataGate.Common.DateTimeFormat.html), [DateTimeSeparator](/reference/asna-qsys-runtime/classes/date-time-separator.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

RPG's MOVEL. Moves left a DateTime to string.

```cs
MoveLeft(DateTime dateTime, ASNA.QSys.Runtime.DateTimeDataKind dateTimeKind, ASNA.DataGate.Common.DateTimeFormat dateTimeFormat, ASNA.QSys.Runtime.DateTimeSeparator dateTimeSeparator, String targetOperand);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | dateTime | The date/time/timestamp value to move. 
| [DateTimeDataKind](/reference/asna-qsys-runtime/date-time-data-kind.html) | dateTimeKind | The DateTimeDataKind value that specifies whether it is a date, time, or timestamp. 
| [DateTimeFormat]($$TODO-ASNA.DataGate.Common.DateTimeFormat.html) | dateTimeFormat | The DateTimeFormat of the value. 
| [DateTimeSeparator](/reference/asna-qsys-runtime/classes/date-time-separator.html) | dateTimeSeparator | The DateTimeSeparator of the value. 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | targetOperand | The string value that is the target of the MOVEL. 

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

The string resulting from the MOVEL operation of the dateTime with the given format and separator into the targetOperand string.


<br>
<br>

### MoveLeft([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind](/reference/asna-qsys-runtime/date-time-data-kind.html), [DateTimeFormat]($$TODO-ASNA.DataGate.Common.DateTimeFormat.html), [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

RPG's MOVEL. Moves left a DateTime to decimal.

```cs
MoveLeft(DateTime dateTime, ASNA.QSys.Runtime.DateTimeDataKind dateTimeKind, ASNA.DataGate.Common.DateTimeFormat dateTimeFormat, Decimal targetOperand, Int32 digits, Int32 decimals);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | dateTime | .NET DateTime type. 
| [DateTimeDataKind](/reference/asna-qsys-runtime/date-time-data-kind.html) | dateTimeKind | The kind that the dateTime should be interpreted as. 
| [DateTimeFormat]($$TODO-ASNA.DataGate.Common.DateTimeFormat.html) | dateTimeFormat | The format of the dateTime. 
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | targetOperand | The targetOperand decimal. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | digits | The number of digits in the targetOperand. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | decimals | The number of decimal places in the targetOperand. 

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

returns a decimal value of the targetOperand.


<br>
<br>

### MoveLeft([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind](/reference/asna-qsys-runtime/date-time-data-kind.html), [DateTimeFormat]($$TODO-ASNA.DataGate.Common.DateTimeFormat.html), [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16))

RPG's MOVEL. Moves left a datetime into a int2 (short).

```cs
MoveLeft(DateTime dateTime, ASNA.QSys.Runtime.DateTimeDataKind dateTimeKind, ASNA.DataGate.Common.DateTimeFormat dateTimeFormat, Int16 targetOperand);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | dateTime | .NET DateTime type. 
| [DateTimeDataKind](/reference/asna-qsys-runtime/date-time-data-kind.html) | dateTimeKind | The kind that the dateTime should be interpreted as. 
| [DateTimeFormat]($$TODO-ASNA.DataGate.Common.DateTimeFormat.html) | dateTimeFormat | The format of the dateTime. 
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | targetOperand | short int value of the targetOperand. 

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

short int targetOperand of the move.


<br>
<br>

### MoveLeft([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind](/reference/asna-qsys-runtime/date-time-data-kind.html), [DateTimeFormat]($$TODO-ASNA.DataGate.Common.DateTimeFormat.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

RPG's MOVEL. Moves left a datetime into a int4 (int).

```cs
MoveLeft(DateTime dateTime, ASNA.QSys.Runtime.DateTimeDataKind dateTimeKind, ASNA.DataGate.Common.DateTimeFormat dateTimeFormat, Int32 targetOperand);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | dateTime | .NET DateTime type. 
| [DateTimeDataKind](/reference/asna-qsys-runtime/date-time-data-kind.html) | dateTimeKind | The kind that the dateTime should be interpreted as. 
| [DateTimeFormat]($$TODO-ASNA.DataGate.Common.DateTimeFormat.html) | dateTimeFormat | The format of the dateTime. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetOperand | int value of the targetOperand. 

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

int targetOperand of the move.


<br>
<br>

### MoveLeft([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind](/reference/asna-qsys-runtime/date-time-data-kind.html), [DateTimeFormat]($$TODO-ASNA.DataGate.Common.DateTimeFormat.html), [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64))

RPG's MOVEL. Moves left a datetime into a int8 (long).

```cs
MoveLeft(DateTime dateTime, ASNA.QSys.Runtime.DateTimeDataKind dateTimeKind, ASNA.DataGate.Common.DateTimeFormat dateTimeFormat, Int64 targetOperand);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | dateTime | .NET DateTime type. 
| [DateTimeDataKind](/reference/asna-qsys-runtime/date-time-data-kind.html) | dateTimeKind | The kind that the dateTime should be interpreted as. 
| [DateTimeFormat]($$TODO-ASNA.DataGate.Common.DateTimeFormat.html) | dateTimeFormat | The format of the dateTime. 
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | targetOperand | long value of the targetOperand. 

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

long targetOperand of the move.


<br>
<br>

### MoveLeftToChar([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind](/reference/asna-qsys-runtime/date-time-data-kind.html), [DateTimeFormat]($$TODO-ASNA.DataGate.Common.DateTimeFormat.html))

RPG's MOVEL. Moves left a date, time, timestamp in the given format to a char value.

```cs
MoveLeftToChar(DateTime dateTime, ASNA.QSys.Runtime.DateTimeDataKind dateTimeKind, ASNA.DataGate.Common.DateTimeFormat dateTimeFormat);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | dateTime | .NET DateTime type. 
| [DateTimeDataKind](/reference/asna-qsys-runtime/date-time-data-kind.html) | dateTimeKind | The kind that the dateTime should be interpreted as. 
| [DateTimeFormat]($$TODO-ASNA.DataGate.Common.DateTimeFormat.html) | dateTimeFormat | The format of the dateTime. 

#### Returns

[Char](https://docs.microsoft.com/en-us/dotnet/api/system.char)

.


<br>
<br>

### MoveLeftWithPad([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind](/reference/asna-qsys-runtime/date-time-data-kind.html), [DateTimeFormat]($$TODO-ASNA.DataGate.Common.DateTimeFormat.html), [DateTimeSeparator](/reference/asna-qsys-runtime/classes/date-time-separator.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

RPG's MOVEL. Moves left a DateTime to string with pad.

```cs
MoveLeftWithPad(DateTime dateTime, ASNA.QSys.Runtime.DateTimeDataKind dateTimeKind, ASNA.DataGate.Common.DateTimeFormat dateTimeFormat, ASNA.QSys.Runtime.DateTimeSeparator dateTimeSeparator, String targetOperand);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | dateTime | The date/time/timestamp value to move. 
| [DateTimeDataKind](/reference/asna-qsys-runtime/date-time-data-kind.html) | dateTimeKind | The DateTimeDataKind value that specifies whether it is a date, time, or timestamp. 
| [DateTimeFormat]($$TODO-ASNA.DataGate.Common.DateTimeFormat.html) | dateTimeFormat | The DateTimeFormat of the value. 
| [DateTimeSeparator](/reference/asna-qsys-runtime/classes/date-time-separator.html) | dateTimeSeparator | The DateTimeSeparator of the value. 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | targetOperand | The string value that is the target of the MOVEL. 

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

The string resulting from the MOVEL operation of the dateTime with the given format and separator into the targetOperand string.


<br>
<br>

### MoveLeftWithPad([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind](/reference/asna-qsys-runtime/date-time-data-kind.html), [DateTimeFormat]($$TODO-ASNA.DataGate.Common.DateTimeFormat.html), [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

RPG's MOVEL. Moves left a DateTime to decimal with pad.

```cs
MoveLeftWithPad(DateTime dateTime, ASNA.QSys.Runtime.DateTimeDataKind dateTimeKind, ASNA.DataGate.Common.DateTimeFormat dateTimeFormat, Decimal targetOperand, Int32 digits, Int32 decimals);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | dateTime | .NET DateTime type. 
| [DateTimeDataKind](/reference/asna-qsys-runtime/date-time-data-kind.html) | dateTimeKind | The kind that the dateTime should be interpreted as. 
| [DateTimeFormat]($$TODO-ASNA.DataGate.Common.DateTimeFormat.html) | dateTimeFormat | The format of the dateTime. 
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | targetOperand | The targetOperand decimal. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | digits | The number of digits in the targetOperand. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | decimals | The number of decimal places in the targetOperand. 

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

returns a decimal value of the targetOperand.


<br>
<br>

### MoveLeftWithPad([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind](/reference/asna-qsys-runtime/date-time-data-kind.html), [DateTimeFormat]($$TODO-ASNA.DataGate.Common.DateTimeFormat.html), [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16))

RPG's MOVE. Moves right a datetime into a int2 (short) with pad.

```cs
MoveLeftWithPad(DateTime dateTime, ASNA.QSys.Runtime.DateTimeDataKind dateTimeKind, ASNA.DataGate.Common.DateTimeFormat dateTimeFormat, Int16 targetOperand);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | dateTime | .NET DateTime type. 
| [DateTimeDataKind](/reference/asna-qsys-runtime/date-time-data-kind.html) | dateTimeKind | The kind that the dateTime should be interpreted as. 
| [DateTimeFormat]($$TODO-ASNA.DataGate.Common.DateTimeFormat.html) | dateTimeFormat | The format of the dateTime. 
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | targetOperand | short int value of the targetOperand. 

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

short int targetOperand of the move.


<br>
<br>

### MoveLeftWithPad([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind](/reference/asna-qsys-runtime/date-time-data-kind.html), [DateTimeFormat]($$TODO-ASNA.DataGate.Common.DateTimeFormat.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

RPG's MOVEL. Moves left a datetime into a int4 (int).

```cs
MoveLeftWithPad(DateTime dateTime, ASNA.QSys.Runtime.DateTimeDataKind dateTimeKind, ASNA.DataGate.Common.DateTimeFormat dateTimeFormat, Int32 targetOperand);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | dateTime | .NET DateTime type. 
| [DateTimeDataKind](/reference/asna-qsys-runtime/date-time-data-kind.html) | dateTimeKind | The kind that the dateTime should be interpreted as. 
| [DateTimeFormat]($$TODO-ASNA.DataGate.Common.DateTimeFormat.html) | dateTimeFormat | The format of the dateTime. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetOperand | int value of the targetOperand. 

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

int targetOperand of the move.


<br>
<br>

### MoveLeftWithPad([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind](/reference/asna-qsys-runtime/date-time-data-kind.html), [DateTimeFormat]($$TODO-ASNA.DataGate.Common.DateTimeFormat.html), [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64))

RPG's MOVEL. Moves left a datetime into a int8 (long).

```cs
MoveLeftWithPad(DateTime dateTime, ASNA.QSys.Runtime.DateTimeDataKind dateTimeKind, ASNA.DataGate.Common.DateTimeFormat dateTimeFormat, Int64 targetOperand);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | dateTime | .NET DateTime type. 
| [DateTimeDataKind](/reference/asna-qsys-runtime/date-time-data-kind.html) | dateTimeKind | The kind that the dateTime should be interpreted as. 
| [DateTimeFormat]($$TODO-ASNA.DataGate.Common.DateTimeFormat.html) | dateTimeFormat | The format of the dateTime. 
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | targetOperand | long value of the targetOperand. 

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

long targetOperand of the move.


<br>
<br>

### MoveRight([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind](/reference/asna-qsys-runtime/date-time-data-kind.html), [DateTimeFormat]($$TODO-ASNA.DataGate.Common.DateTimeFormat.html), [DateTimeSeparator](/reference/asna-qsys-runtime/classes/date-time-separator.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

RPG's MOVE. Moves right a DateTime to string.

```cs
MoveRight(DateTime dateTime, ASNA.QSys.Runtime.DateTimeDataKind dateTimeKind, ASNA.DataGate.Common.DateTimeFormat dateTimeFormat, ASNA.QSys.Runtime.DateTimeSeparator dateTimeSeparator, String targetOperand);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | dateTime | The date/time/timestamp value to move. 
| [DateTimeDataKind](/reference/asna-qsys-runtime/date-time-data-kind.html) | dateTimeKind | The DateTimeDataKind value that specifies whether it is a date, time, or timestamp. 
| [DateTimeFormat]($$TODO-ASNA.DataGate.Common.DateTimeFormat.html) | dateTimeFormat | The DateTimeFormat of the value. 
| [DateTimeSeparator](/reference/asna-qsys-runtime/classes/date-time-separator.html) | dateTimeSeparator | The DateTimeSeparator of the value. 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | targetOperand | The string value that is the target of the MOVE. 

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

The string resulting from the MOVE operation of the dateTime with the given format and separator into the targetOperand string.


<br>
<br>

### MoveRight([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind](/reference/asna-qsys-runtime/date-time-data-kind.html), [DateTimeFormat]($$TODO-ASNA.DataGate.Common.DateTimeFormat.html), [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

RPG's MOVE. Moves right s DateTime to decimal.

```cs
MoveRight(DateTime dateTime, ASNA.QSys.Runtime.DateTimeDataKind dateTimeKind, ASNA.DataGate.Common.DateTimeFormat dateTimeFormat, Decimal targetOperand, Int32 digits, Int32 decimals);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | dateTime | The date/time/timestamp value to move. 
| [DateTimeDataKind](/reference/asna-qsys-runtime/date-time-data-kind.html) | dateTimeKind | The DateTimeDataKind value that specifies whether it is a date, time, or timestamp. 
| [DateTimeFormat]($$TODO-ASNA.DataGate.Common.DateTimeFormat.html) | dateTimeFormat | The DateTimeFormat of the value. 
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | targetOperand | The decimal value that is the target of the MOVE. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | digits | The total number of digits in the decimal number. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | decimals | The number of decimal positions in the decimal number. 

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

The decimal number resulting from the MOVE operation of the dateTime with the given format and separator into the targetOperand number.


<br>
<br>

### MoveRight([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind](/reference/asna-qsys-runtime/date-time-data-kind.html), [DateTimeFormat]($$TODO-ASNA.DataGate.Common.DateTimeFormat.html), [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16))

RPG's MOVE. Moves right a datetime into a int2 (short).

```cs
MoveRight(DateTime dateTime, ASNA.QSys.Runtime.DateTimeDataKind dateTimeKind, ASNA.DataGate.Common.DateTimeFormat dateTimeFormat, Int16 targetOperand);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | dateTime | .NET DateTime type. 
| [DateTimeDataKind](/reference/asna-qsys-runtime/date-time-data-kind.html) | dateTimeKind | The kind that the dateTime should be interpreted as. 
| [DateTimeFormat]($$TODO-ASNA.DataGate.Common.DateTimeFormat.html) | dateTimeFormat | The format of the dateTime. 
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | targetOperand | short int value of the targetOperand. 

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

short int targetOperand of the move.


<br>
<br>

### MoveRight([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind](/reference/asna-qsys-runtime/date-time-data-kind.html), [DateTimeFormat]($$TODO-ASNA.DataGate.Common.DateTimeFormat.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

RPG's MOVE. Moves right a datetime into a int4 (int).

```cs
MoveRight(DateTime dateTime, ASNA.QSys.Runtime.DateTimeDataKind dateTimeKind, ASNA.DataGate.Common.DateTimeFormat dateTimeFormat, Int32 targetOperand);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | dateTime | .NET DateTime type. 
| [DateTimeDataKind](/reference/asna-qsys-runtime/date-time-data-kind.html) | dateTimeKind | The kind that the dateTime should be interpreted as. 
| [DateTimeFormat]($$TODO-ASNA.DataGate.Common.DateTimeFormat.html) | dateTimeFormat | The format of the dateTime. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetOperand | int value of the targetOperand. 

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

int targetOperand of the move.


<br>
<br>

### MoveRight([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind](/reference/asna-qsys-runtime/date-time-data-kind.html), [DateTimeFormat]($$TODO-ASNA.DataGate.Common.DateTimeFormat.html), [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64))

RPG's MOVE. Moves right a datetime into a int8 (long).

```cs
MoveRight(DateTime dateTime, ASNA.QSys.Runtime.DateTimeDataKind dateTimeKind, ASNA.DataGate.Common.DateTimeFormat dateTimeFormat, Int64 targetOperand);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | dateTime | .NET DateTime type. 
| [DateTimeDataKind](/reference/asna-qsys-runtime/date-time-data-kind.html) | dateTimeKind | The kind that the dateTime should be interpreted as. 
| [DateTimeFormat]($$TODO-ASNA.DataGate.Common.DateTimeFormat.html) | dateTimeFormat | The format of the dateTime. 
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | targetOperand | long value of the targetOperand. 

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

long targetOperand of the move.


<br>
<br>

### MoveRightToChar([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind](/reference/asna-qsys-runtime/date-time-data-kind.html), [DateTimeFormat]($$TODO-ASNA.DataGate.Common.DateTimeFormat.html))

RPG's MOVE. Moves right a date, time, timestamp in the given format to a char value.

```cs
MoveRightToChar(DateTime dateTime, ASNA.QSys.Runtime.DateTimeDataKind dateTimeKind, ASNA.DataGate.Common.DateTimeFormat dateTimeFormat);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | dateTime | .NET DateTime type. 
| [DateTimeDataKind](/reference/asna-qsys-runtime/date-time-data-kind.html) | dateTimeKind | The kind that the dateTime should be interpreted as. 
| [DateTimeFormat]($$TODO-ASNA.DataGate.Common.DateTimeFormat.html) | dateTimeFormat | The format of the dateTime. 

#### Returns

[Char](https://docs.microsoft.com/en-us/dotnet/api/system.char)

.


<br>
<br>

### MoveRightWithPad([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind](/reference/asna-qsys-runtime/date-time-data-kind.html), [DateTimeFormat]($$TODO-ASNA.DataGate.Common.DateTimeFormat.html), [DateTimeSeparator](/reference/asna-qsys-runtime/classes/date-time-separator.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

RPG's MOVE. Moves right a DateTime to string with pad.

```cs
MoveRightWithPad(DateTime dateTime, ASNA.QSys.Runtime.DateTimeDataKind dateTimeKind, ASNA.DataGate.Common.DateTimeFormat dateTimeFormat, ASNA.QSys.Runtime.DateTimeSeparator dateTimeSeparator, String targetOperand);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | dateTime | The date/time/timestamp value to move. 
| [DateTimeDataKind](/reference/asna-qsys-runtime/date-time-data-kind.html) | dateTimeKind | The DateTimeDataKind value that specifies whether it is a date, time, or timestamp. 
| [DateTimeFormat]($$TODO-ASNA.DataGate.Common.DateTimeFormat.html) | dateTimeFormat | The DateTimeFormat of the value. 
| [DateTimeSeparator](/reference/asna-qsys-runtime/classes/date-time-separator.html) | dateTimeSeparator | The DateTimeSeparator of the value. 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | targetOperand | The string value that is the target of the MOVE. 

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

The string resulting from the MOVE operation of the dateTime with the given format and separator into the targetOperand string.


<br>
<br>

### MoveRightWithPad([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind](/reference/asna-qsys-runtime/date-time-data-kind.html), [DateTimeFormat]($$TODO-ASNA.DataGate.Common.DateTimeFormat.html), [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

RPG's MOVE. Moves right a DateTime to decimal with pad.

```cs
MoveRightWithPad(DateTime dateTime, ASNA.QSys.Runtime.DateTimeDataKind dateTimeKind, ASNA.DataGate.Common.DateTimeFormat dateTimeFormat, Decimal targetOperand, Int32 digits, Int32 decimals);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | dateTime | The date/time/timestamp value to move. 
| [DateTimeDataKind](/reference/asna-qsys-runtime/date-time-data-kind.html) | dateTimeKind | The DateTimeDataKind value that specifies whether it is a date, time, or timestamp. 
| [DateTimeFormat]($$TODO-ASNA.DataGate.Common.DateTimeFormat.html) | dateTimeFormat | The DateTimeFormat of the value. 
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | targetOperand | The decimal value that is the target of the MOVE. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | digits | The total number of digits in the decimal number. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | decimals | The number of decimal positions in the decimal number. 

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

The decimal number resulting from the MOVE operation of the dateTime with the given format and separator into the targetOperand number.


<br>
<br>

### MoveRightWithPad([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind](/reference/asna-qsys-runtime/date-time-data-kind.html), [DateTimeFormat]($$TODO-ASNA.DataGate.Common.DateTimeFormat.html), [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16))

RPG's MOVE. Moves right a datetime into a int2 (short) with pad.

```cs
MoveRightWithPad(DateTime dateTime, ASNA.QSys.Runtime.DateTimeDataKind dateTimeKind, ASNA.DataGate.Common.DateTimeFormat dateTimeFormat, Int16 targetOperand);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | dateTime | .NET DateTime type. 
| [DateTimeDataKind](/reference/asna-qsys-runtime/date-time-data-kind.html) | dateTimeKind | The kind that the dateTime should be interpreted as. 
| [DateTimeFormat]($$TODO-ASNA.DataGate.Common.DateTimeFormat.html) | dateTimeFormat | The format of the dateTime. 
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | targetOperand | short int value of the targetOperand. 

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

short int targetOperand of the move.


<br>
<br>

### MoveRightWithPad([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind](/reference/asna-qsys-runtime/date-time-data-kind.html), [DateTimeFormat]($$TODO-ASNA.DataGate.Common.DateTimeFormat.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

RPG's MOVE. Moves right a datetime into a int4 (int) with pad.

```cs
MoveRightWithPad(DateTime dateTime, ASNA.QSys.Runtime.DateTimeDataKind dateTimeKind, ASNA.DataGate.Common.DateTimeFormat dateTimeFormat, Int32 targetOperand);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | dateTime | .NET DateTime type. 
| [DateTimeDataKind](/reference/asna-qsys-runtime/date-time-data-kind.html) | dateTimeKind | The kind that the dateTime should be interpreted as. 
| [DateTimeFormat]($$TODO-ASNA.DataGate.Common.DateTimeFormat.html) | dateTimeFormat | The format of the dateTime. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetOperand | int value of the targetOperand. 

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

int targetOperand of the move.


<br>
<br>

### MoveRightWithPad([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind](/reference/asna-qsys-runtime/date-time-data-kind.html), [DateTimeFormat]($$TODO-ASNA.DataGate.Common.DateTimeFormat.html), [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64))

RPG's MOVE. Moves right a datetime into a int8 (long) with pad.

```cs
MoveRightWithPad(DateTime dateTime, ASNA.QSys.Runtime.DateTimeDataKind dateTimeKind, ASNA.DataGate.Common.DateTimeFormat dateTimeFormat, Int64 targetOperand);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | dateTime | .NET DateTime type. 
| [DateTimeDataKind](/reference/asna-qsys-runtime/date-time-data-kind.html) | dateTimeKind | The kind that the dateTime should be interpreted as. 
| [DateTimeFormat]($$TODO-ASNA.DataGate.Common.DateTimeFormat.html) | dateTimeFormat | The format of the dateTime. 
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | targetOperand | long value of the targetOperand. 

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

long targetOperand of the move.


<br>
<br>

### NormalizeYear([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime))

Turns a 4 digit year into a 2 digit year between 1940 and 2039

```cs
NormalizeYear(DateTime dateTime);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | dateTime | .NET DateTime value. 

#### Returns

[DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime)

.NET DateTime value.


<br>
<br>

### SubtractDuration([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [Double]($$TODO-Double.html), [DurationCode](/reference/asna-qsys-runtime/date-time-ops-duration-code.html))

Subtracts a duration span from a date or a timestamp value.

```cs
SubtractDuration(DateTime dateTime, Double duration, ASNA.QSys.Runtime.DateTimeOps.DurationCode durationCode);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | dateTime | .NET DateTime type. 
| [Double]($$TODO-Double.html) | duration | A double value representing duration. 
| [DurationCode](/reference/asna-qsys-runtime/date-time-ops-duration-code.html) | durationCode | Code determining what duration represents. 

#### Returns

[DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime)

.


<br>
<br>

### SubtractDurationFromTime([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [Double]($$TODO-Double.html), [DurationCode](/reference/asna-qsys-runtime/date-time-ops-duration-code.html))

Subtracts a duration span from a time value.

```cs
SubtractDurationFromTime(DateTime dateTime, Double duration, ASNA.QSys.Runtime.DateTimeOps.DurationCode durationCode);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | dateTime | .NET DateTime value specifying a time value. 
| [Double]($$TODO-Double.html) | duration | A double value representing duration. 
| [DurationCode](/reference/asna-qsys-runtime/date-time-ops-duration-code.html) | durationCode | Code determining what duration represents. 

#### Returns

[DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime)

.


<br>
<br>

### TimestampToDate([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime))

Returns the Date portion of a timestamp.

```cs
TimestampToDate(DateTime timestamp);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | timestamp | The timestamp as a DateTime value. 

#### Returns

[DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime)

The Date portion as a DateTime value.


<br>
<br>

### TimestampToTime([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime))

Returns the hours, minutes, and seconds of a timestamp.

```cs
TimestampToTime(DateTime timestamp);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | timestamp | The timestamp as a DateTime value. 

#### Returns

[DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime)

The Time portion in hours, minutes, and seconds as a DateTime value.


<br>
<br>

### TimestampToUSATime([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime))

Returns the hours and minutes of a timestamp.

```cs
TimestampToUSATime(DateTime timestamp);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | timestamp | The timestamp as a DateTime value. 

#### Returns

[DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime)

The Time portion in hours and minutes only as a DateTime value.


<br>
<br>

### ToFixedDecimal([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind](/reference/asna-qsys-runtime/date-time-data-kind.html), [DateTimeFormat]($$TODO-ASNA.DataGate.Common.DateTimeFormat.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

Converts a dateTime type, converts it to a decmial.

```cs
ToFixedDecimal(DateTime dateTime, ASNA.QSys.Runtime.DateTimeDataKind dateTimeKind, ASNA.DataGate.Common.DateTimeFormat dateTimeFormat, Int32 digits, Int32 decimals);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | dateTime | .NET DateTime type. 
| [DateTimeDataKind](/reference/asna-qsys-runtime/date-time-data-kind.html) | dateTimeKind | The Kind of the DateTime being converted. 
| [DateTimeFormat]($$TODO-ASNA.DataGate.Common.DateTimeFormat.html) | dateTimeFormat | The Format of the DateTime being converted. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | digits | Number of digits in the targetOperand. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | decimals | Number of decimal places in the targetOperand. 

#### Returns

[Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal)

The decimal number that results from the conversion.


<br>
<br>

### ToFixedDecimal([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind](/reference/asna-qsys-runtime/date-time-data-kind.html), [DateTimeFormat]($$TODO-ASNA.DataGate.Common.DateTimeFormat.html))

Converts a dateTime type to decimal.

```cs
ToFixedDecimal(DateTime dateTime, ASNA.QSys.Runtime.DateTimeDataKind dateTimeKind, ASNA.DataGate.Common.DateTimeFormat dateTimeFormat);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | dateTime | .NET DateTime type. 
| [DateTimeDataKind](/reference/asna-qsys-runtime/date-time-data-kind.html) | dateTimeKind | The Kind of the DateTime being converted. 
| [DateTimeFormat]($$TODO-ASNA.DataGate.Common.DateTimeFormat.html) | dateTimeFormat | The Format of the DateTime being converted. 

#### Returns

[Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal)

The decimal number that results from the conversion.


<br>
<br>

### ToInt16([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind](/reference/asna-qsys-runtime/date-time-data-kind.html), [DateTimeFormat]($$TODO-ASNA.DataGate.Common.DateTimeFormat.html), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Converts a dateTime type to int 16.

```cs
ToInt16(DateTime dateTime, ASNA.QSys.Runtime.DateTimeDataKind dateTimeKind, ASNA.DataGate.Common.DateTimeFormat dateTimeFormat, Boolean throwOnOverflow);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | dateTime | .NET DateTime type. 
| [DateTimeDataKind](/reference/asna-qsys-runtime/date-time-data-kind.html) | dateTimeKind | The Kind of the DateTime being converted. 
| [DateTimeFormat]($$TODO-ASNA.DataGate.Common.DateTimeFormat.html) | dateTimeFormat | The Format of the DateTime being converted. 
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | throwOnOverflow | Default is false. Pass true if a runtime exception is desired when the conversion doesn't fit. 

#### Returns

[Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16)

The Int16 number that results from the conversion.


<br>
<br>

### ToInt32([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind](/reference/asna-qsys-runtime/date-time-data-kind.html), [DateTimeFormat]($$TODO-ASNA.DataGate.Common.DateTimeFormat.html), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Converts a dateTime type to int 32.

```cs
ToInt32(DateTime dateTime, ASNA.QSys.Runtime.DateTimeDataKind dateTimeKind, ASNA.DataGate.Common.DateTimeFormat dateTimeFormat, Boolean throwOnOverflow);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | dateTime | .NET DateTime type. 
| [DateTimeDataKind](/reference/asna-qsys-runtime/date-time-data-kind.html) | dateTimeKind | The Kind of the DateTime being converted. 
| [DateTimeFormat]($$TODO-ASNA.DataGate.Common.DateTimeFormat.html) | dateTimeFormat | The Format of the DateTime being converted. 
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | throwOnOverflow | Default is false. Pass true if a runtime exception is desired when the conversion doesn't fit. 

#### Returns

[Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)

The Int32 number that results from the conversion.


<br>
<br>

### ToInt64([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind](/reference/asna-qsys-runtime/date-time-data-kind.html), [DateTimeFormat]($$TODO-ASNA.DataGate.Common.DateTimeFormat.html), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Converts a dateTime type to int 64.

```cs
ToInt64(DateTime dateTime, ASNA.QSys.Runtime.DateTimeDataKind dateTimeKind, ASNA.DataGate.Common.DateTimeFormat dateTimeFormat, Boolean throwOnOverflow);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | dateTime | .NET DateTime type. 
| [DateTimeDataKind](/reference/asna-qsys-runtime/date-time-data-kind.html) | dateTimeKind | The Kind of the DateTime being converted. 
| [DateTimeFormat]($$TODO-ASNA.DataGate.Common.DateTimeFormat.html) | dateTimeFormat | The Format of the DateTime being converted. 
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | throwOnOverflow | Default is false. Pass true if a runtime exception is desired when the conversion doesn't fit. 

#### Returns

[Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64)

The Int64 number that results from the conversion.


<br>
<br>

### ToString([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind](/reference/asna-qsys-runtime/date-time-data-kind.html), [DateTimeFormat]($$TODO-ASNA.DataGate.Common.DateTimeFormat.html), [DateTimeSeparator](/reference/asna-qsys-runtime/classes/date-time-separator.html))

Converts a DateTime with the specified Kind and Format to a string using the specified separator.

```cs
ToString(DateTime dateTime, ASNA.QSys.Runtime.DateTimeDataKind dateTimeKind, ASNA.DataGate.Common.DateTimeFormat dateTimeFormat, ASNA.QSys.Runtime.DateTimeSeparator dateTimeSeparator);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | dateTime | .NET DateTime type. 
| [DateTimeDataKind](/reference/asna-qsys-runtime/date-time-data-kind.html) | dateTimeKind | The Kind of the DateTime being converted. 
| [DateTimeFormat]($$TODO-ASNA.DataGate.Common.DateTimeFormat.html) | dateTimeFormat | The Format of the DateTime being converted. 
| [DateTimeSeparator](/reference/asna-qsys-runtime/classes/date-time-separator.html) | dateTimeSeparator | The separator to use in the returned string. 

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

A string representation of a DateTime in the given format using the specified separator.


<br>
<br>

