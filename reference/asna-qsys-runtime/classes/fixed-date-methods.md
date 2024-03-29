---
title: FixedDateMethods Class
---

Contains extension methods for handling RPG operations for FixedDate values.

**Namespace:** ASNA.QSys.Runtime <br/>
**Assembly:** ASNA.QSys.Runtime

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> FixedDateMethods

<br>
<br>

## Remarks

Contains extension methods for handling RPG operations for FixedDate values.

[//]: # ($$TODO: Complete the Remarks section.)

<br>
<br>

## Methods

| Type | Name | Description | Return Description 
| --- | --- | --- | --- 
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [AddDuration&lt;T,U&gt;](#addduration&lt;t,u&gt;fixeddate(<t>-<t>)-double-durationcode)([FixedDate](/reference/asna-qsys-runtime/classes/fixed-date.html)([&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics),[&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics)), [Double](https://learn.microsoft.com/en-us/dotnet/api/system.double?view=net-8.0), [DurationCode](/reference/asna-qsys-runtime/date-time-ops-duration-code.html)) | Adds a duration span to a date or a timestamp value. | The resulting Date or Timestamp value after adding to it the given duration.
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [AddDurationToTime&lt;T,U&gt;](#adddurationtotime&lt;t,u&gt;fixeddate(<t>-<t>)-double-durationcode)([FixedDate](/reference/asna-qsys-runtime/classes/fixed-date.html)([&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics),[&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics)), [Double](https://learn.microsoft.com/en-us/dotnet/api/system.double?view=net-8.0), [DurationCode](/reference/asna-qsys-runtime/date-time-ops-duration-code.html)) | Adds a duration span to a time value. | The resulting Time value after adding to it the given duration.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | [Equals](https://docs.microsoft.com/en-us/dotnet/api/system.object.equals)([Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | Determines whether the specified object is equal to the current object.<br>(Inherited from [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | true if the specified object is equal to the current object; otherwise, false.
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [Finalize](https://docs.microsoft.com/en-us/dotnet/api/system.object.finalize)() | Allows an object to try to free resources and perform other cleanup operations before it is reclaimed by garbage collection.<br>(Inherited from [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | [GetHashCode](https://docs.microsoft.com/en-us/dotnet/api/system.object.gethashcode)() | Serves as the default hash function.<br>(Inherited from [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | A hash code for the current object.
| [Type](https://docs.microsoft.com/en-us/dotnet/api/system.type) | [GetType](https://docs.microsoft.com/en-us/dotnet/api/system.object.gettype)() | Gets the Type of the current instance.<br>(Inherited from [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | The exact runtime type of the current instance.
| [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) | [MemberwiseClone](https://docs.microsoft.com/en-us/dotnet/api/system.object.memberwiseclone)() | Creates a shallow copy of the current Object.<br>(Inherited from [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | A shallow copy of the current Object.
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [MoveLeft&lt;T,U,V,S&gt;](#moveleft&lt;t,u,v,s&gt;fixeddate(<t>-<t>)-fixeddecimal(<t-u>-<t-u-v>))([FixedDate](/reference/asna-qsys-runtime/classes/fixed-date.html)([&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics),[&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics)), [FixedDecimal](/reference/asna-qsys-runtime/classes/fixed-decimal.html)([&lt;T,U&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics),[&lt;T,U,V&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics))) | RPG's MOVEL. Moves left a fixed date to decimal. | The resulting decimal value of the operation.
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [MoveLeft&lt;T,U,V,S&gt;](#moveleft&lt;t,u,v,s&gt;fixeddate(<t>-<t>)-datetimeformat-fixeddecimal(<t-u>-<t-u-v>))([FixedDate](/reference/asna-qsys-runtime/classes/fixed-date.html)([&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics),[&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics)), [DateTimeFormat](/reference/datagate-client/date-time-format-enumeration.html), [FixedDecimal](/reference/asna-qsys-runtime/classes/fixed-decimal.html)([&lt;T,U&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics),[&lt;T,U,V&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics))) | RPG's MOVEL. Moves left a fixed date to decimal. | The resulting decimal value of the operation.
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [MoveLeft&lt;T,U&gt;](#moveleft&lt;t,u&gt;fixeddate(<t>-<t>)-string)([FixedDate](/reference/asna-qsys-runtime/classes/fixed-date.html)([&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics),[&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics)), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | RPG's MOVEL. Moves left a fixed date to string. | The resulting string value of the operation.
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [MoveLeft&lt;T,U&gt;](#moveleft&lt;t,u&gt;fixeddate(<t>-<t>)-int16)([FixedDate](/reference/asna-qsys-runtime/classes/fixed-date.html)([&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics),[&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics)), [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16)) | RPG's MOVEL. Moves left a fixed date into a int2 (short). | The resulting short value of the operation.
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [MoveLeft&lt;T,U&gt;](#moveleft&lt;t,u&gt;fixeddate(<t>-<t>)-datetimeformat-int16)([FixedDate](/reference/asna-qsys-runtime/classes/fixed-date.html)([&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics),[&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics)), [DateTimeFormat](/reference/datagate-client/date-time-format-enumeration.html), [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16)) | RPG's MOVEL. Moves left a fixed date into a int2 (short). | The resulting short value of the operation.
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [MoveLeft&lt;T,U&gt;](#moveleft&lt;t,u&gt;fixeddate(<t>-<t>)-int32)([FixedDate](/reference/asna-qsys-runtime/classes/fixed-date.html)([&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics),[&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics)), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's MOVEL. Moves left a fixed date into a int4 (int). | The resulting int value of the operation.
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [MoveLeft&lt;T,U&gt;](#moveleft&lt;t,u&gt;fixeddate(<t>-<t>)-datetimeformat-int32)([FixedDate](/reference/asna-qsys-runtime/classes/fixed-date.html)([&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics),[&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics)), [DateTimeFormat](/reference/datagate-client/date-time-format-enumeration.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's MOVEL. Moves left a fixed date into a int4 (int). | The resulting int value of the operation.
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [MoveLeft&lt;T,U&gt;](#moveleft&lt;t,u&gt;fixeddate(<t>-<t>)-int64)([FixedDate](/reference/asna-qsys-runtime/classes/fixed-date.html)([&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics),[&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics)), [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64)) | RPG's MOVEL. Moves left a fixed date into a int8 (long). | The resulting long value of the operation.
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [MoveLeft&lt;T,U&gt;](#moveleft&lt;t,u&gt;fixeddate(<t>-<t>)-datetimeformat-int64)([FixedDate](/reference/asna-qsys-runtime/classes/fixed-date.html)([&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics),[&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics)), [DateTimeFormat](/reference/datagate-client/date-time-format-enumeration.html), [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64)) | RPG's MOVEL. Moves left a fixed date into a int8 (long). | The resulting long value of the operation.
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [MoveLeftToChar&lt;T,U&gt;](#movelefttochar&lt;t,u&gt;fixeddate(<t>-<t>))([FixedDate](/reference/asna-qsys-runtime/classes/fixed-date.html)([&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics),[&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics))) | RPG's MOVEL. Moves left a date, time, timestamp in the given format to a char value. | The first character in the string representation of the DateTime value.
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [MoveLeftWithPad&lt;T,U,V,S&gt;](#moveleftwithpad&lt;t,u,v,s&gt;fixeddate(<t>-<t>)-fixeddecimal(<t-u>-<t-u-v>))([FixedDate](/reference/asna-qsys-runtime/classes/fixed-date.html)([&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics),[&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics)), [FixedDecimal](/reference/asna-qsys-runtime/classes/fixed-decimal.html)([&lt;T,U&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics),[&lt;T,U,V&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics))) | RPG's MOVEL. Moves left a fixed date to decimal with pad. | The resulting decimal value of the operation.
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [MoveLeftWithPad&lt;T,U,V,S&gt;](#moveleftwithpad&lt;t,u,v,s&gt;fixeddate(<t>-<t>)-datetimeformat-fixeddecimal(<t-u>-<t-u-v>))([FixedDate](/reference/asna-qsys-runtime/classes/fixed-date.html)([&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics),[&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics)), [DateTimeFormat](/reference/datagate-client/date-time-format-enumeration.html), [FixedDecimal](/reference/asna-qsys-runtime/classes/fixed-decimal.html)([&lt;T,U&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics),[&lt;T,U,V&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics))) | RPG's MOVEL. Moves left a fixed date to decimal with pad. | The resulting decimal value of the operation.
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [MoveLeftWithPad&lt;T,U&gt;](#moveleftwithpad&lt;t,u&gt;fixeddate(<t>-<t>)-string)([FixedDate](/reference/asna-qsys-runtime/classes/fixed-date.html)([&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics),[&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics)), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | RPG's MOVEL. Moves left a fixed date to string with pad. | The resulting string value of the operation.
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [MoveLeftWithPad&lt;T,U&gt;](#moveleftwithpad&lt;t,u&gt;fixeddate(<t>-<t>)-int16)([FixedDate](/reference/asna-qsys-runtime/classes/fixed-date.html)([&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics),[&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics)), [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16)) | RPG's MOVE. Moves right a fixed date into a int2 (short) with pad. | The resulting short value of the operation.
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [MoveLeftWithPad&lt;T,U&gt;](#moveleftwithpad&lt;t,u&gt;fixeddate(<t>-<t>)-datetimeformat-int16)([FixedDate](/reference/asna-qsys-runtime/classes/fixed-date.html)([&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics),[&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics)), [DateTimeFormat](/reference/datagate-client/date-time-format-enumeration.html), [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16)) | RPG's MOVE. Moves right a fixed date into a int2 (short) with pad. | The resulting short value of the operation.
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [MoveLeftWithPad&lt;T,U&gt;](#moveleftwithpad&lt;t,u&gt;fixeddate(<t>-<t>)-int32)([FixedDate](/reference/asna-qsys-runtime/classes/fixed-date.html)([&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics),[&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics)), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's MOVEL. Moves left a fixed date into a int4 (int). | The resulting int value of the operation.
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [MoveLeftWithPad&lt;T,U&gt;](#moveleftwithpad&lt;t,u&gt;fixeddate(<t>-<t>)-datetimeformat-int32)([FixedDate](/reference/asna-qsys-runtime/classes/fixed-date.html)([&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics),[&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics)), [DateTimeFormat](/reference/datagate-client/date-time-format-enumeration.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's MOVEL. Moves left a fixed date into a int4 (int). | The resulting int value of the operation.
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [MoveLeftWithPad&lt;T,U&gt;](#moveleftwithpad&lt;t,u&gt;fixeddate(<t>-<t>)-int64)([FixedDate](/reference/asna-qsys-runtime/classes/fixed-date.html)([&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics),[&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics)), [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64)) | RPG's MOVEL. Moves left a fixed date into a int8 (long). | The resulting long value of the operation.
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [MoveLeftWithPad&lt;T,U&gt;](#moveleftwithpad&lt;t,u&gt;fixeddate(<t>-<t>)-datetimeformat-int64)([FixedDate](/reference/asna-qsys-runtime/classes/fixed-date.html)([&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics),[&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics)), [DateTimeFormat](/reference/datagate-client/date-time-format-enumeration.html), [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64)) | RPG's MOVEL. Moves left a fixed date into a int8 (long). | The resulting long value of the operation.
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [MoveRight&lt;T,U,V,S&gt;](#moveright&lt;t,u,v,s&gt;fixeddate(<t>-<t>)-fixeddecimal(<t-u>-<t-u-v>))([FixedDate](/reference/asna-qsys-runtime/classes/fixed-date.html)([&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics),[&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics)), [FixedDecimal](/reference/asna-qsys-runtime/classes/fixed-decimal.html)([&lt;T,U&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics),[&lt;T,U,V&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics))) | RPG's MOVE. Moves right a fixed date to decimal. | The resulting decimal value of the operation.
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [MoveRight&lt;T,U,V,S&gt;](#moveright&lt;t,u,v,s&gt;fixeddate(<t>-<t>)-datetimeformat-fixeddecimal(<t-u>-<t-u-v>))([FixedDate](/reference/asna-qsys-runtime/classes/fixed-date.html)([&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics),[&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics)), [DateTimeFormat](/reference/datagate-client/date-time-format-enumeration.html), [FixedDecimal](/reference/asna-qsys-runtime/classes/fixed-decimal.html)([&lt;T,U&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics),[&lt;T,U,V&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics))) | RPG's MOVE. Moves right a fixed date to decimal. | The resulting decimal value of the operation.
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [MoveRight&lt;T,U&gt;](#moveright&lt;t,u&gt;fixeddate(<t>-<t>)-string)([FixedDate](/reference/asna-qsys-runtime/classes/fixed-date.html)([&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics),[&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics)), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | RPG's MOVE. Moves right a fixed date to string. | The resulting string value of the operation.
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [MoveRight&lt;T,U&gt;](#moveright&lt;t,u&gt;fixeddate(<t>-<t>)-int16)([FixedDate](/reference/asna-qsys-runtime/classes/fixed-date.html)([&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics),[&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics)), [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16)) | RPG's MOVE. Moves right a fixed date into a int2 (short). | The resulting short value of the operation.
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [MoveRight&lt;T,U&gt;](#moveright&lt;t,u&gt;fixeddate(<t>-<t>)-datetimeformat-int16)([FixedDate](/reference/asna-qsys-runtime/classes/fixed-date.html)([&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics),[&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics)), [DateTimeFormat](/reference/datagate-client/date-time-format-enumeration.html), [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16)) | RPG's MOVE. Moves right a fixed date into a int2 (short). | The resulting short value of the operation.
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [MoveRight&lt;T,U&gt;](#moveright&lt;t,u&gt;fixeddate(<t>-<t>)-int32)([FixedDate](/reference/asna-qsys-runtime/classes/fixed-date.html)([&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics),[&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics)), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's MOVE. Moves right a fixed date into a int4 (int). | The resulting int value of the operation.
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [MoveRight&lt;T,U&gt;](#moveright&lt;t,u&gt;fixeddate(<t>-<t>)-datetimeformat-int32)([FixedDate](/reference/asna-qsys-runtime/classes/fixed-date.html)([&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics),[&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics)), [DateTimeFormat](/reference/datagate-client/date-time-format-enumeration.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's MOVE. Moves right a fixed date into a int4 (int). | The resulting int value of the operation.
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [MoveRight&lt;T,U&gt;](#moveright&lt;t,u&gt;fixeddate(<t>-<t>)-int64)([FixedDate](/reference/asna-qsys-runtime/classes/fixed-date.html)([&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics),[&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics)), [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64)) | RPG's MOVE. Moves right a fixed date into a int8 (long). | The resulting long value of the operation.
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [MoveRight&lt;T,U&gt;](#moveright&lt;t,u&gt;fixeddate(<t>-<t>)-datetimeformat-int64)([FixedDate](/reference/asna-qsys-runtime/classes/fixed-date.html)([&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics),[&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics)), [DateTimeFormat](/reference/datagate-client/date-time-format-enumeration.html), [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64)) | RPG's MOVE. Moves right a fixed date into a int8 (long). | The resulting long value of the operation.
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [MoveRightToChar&lt;T,U&gt;](#moverighttochar&lt;t,u&gt;fixeddate(<t>-<t>))([FixedDate](/reference/asna-qsys-runtime/classes/fixed-date.html)([&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics),[&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics))) | RPG's MOVE. Moves right a date in the given format to a char value. | The last character in the string representation of the DateTime value.
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [MoveRightWithPad&lt;T,U,V,S&gt;](#moverightwithpad&lt;t,u,v,s&gt;fixeddate(<t>-<t>)-fixeddecimal(<t-u>-<t-u-v>))([FixedDate](/reference/asna-qsys-runtime/classes/fixed-date.html)([&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics),[&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics)), [FixedDecimal](/reference/asna-qsys-runtime/classes/fixed-decimal.html)([&lt;T,U&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics),[&lt;T,U,V&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics))) | RPG's MOVE. Moves right a fixed date to decimal with pad. | The resulting decimal value of the operation.
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [MoveRightWithPad&lt;T,U,V,S&gt;](#moverightwithpad&lt;t,u,v,s&gt;fixeddate(<t>-<t>)-datetimeformat-fixeddecimal(<t-u>-<t-u-v>))([FixedDate](/reference/asna-qsys-runtime/classes/fixed-date.html)([&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics),[&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics)), [DateTimeFormat](/reference/datagate-client/date-time-format-enumeration.html), [FixedDecimal](/reference/asna-qsys-runtime/classes/fixed-decimal.html)([&lt;T,U&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics),[&lt;T,U,V&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics))) | RPG's MOVE. Moves right a fixed date to decimal with pad. | The resulting decimal value of the operation.
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [MoveRightWithPad&lt;T,U&gt;](#moverightwithpad&lt;t,u&gt;fixeddate(<t>-<t>)-string)([FixedDate](/reference/asna-qsys-runtime/classes/fixed-date.html)([&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics),[&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics)), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | RPG's MOVE. Moves right a fixed date to string with pad. | The resulting string value of the operation.
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [MoveRightWithPad&lt;T,U&gt;](#moverightwithpad&lt;t,u&gt;fixeddate(<t>-<t>)-int16)([FixedDate](/reference/asna-qsys-runtime/classes/fixed-date.html)([&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics),[&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics)), [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16)) | RPG's MOVE. Moves right a fixed date into a int2 (short) with pad. | The resulting short value of the operation.
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [MoveRightWithPad&lt;T,U&gt;](#moverightwithpad&lt;t,u&gt;fixeddate(<t>-<t>)-datetimeformat-int16)([FixedDate](/reference/asna-qsys-runtime/classes/fixed-date.html)([&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics),[&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics)), [DateTimeFormat](/reference/datagate-client/date-time-format-enumeration.html), [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16)) | RPG's MOVE. Moves right a fixed date into a int2 (short) with pad. | The resulting short value of the operation.
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [MoveRightWithPad&lt;T,U&gt;](#moverightwithpad&lt;t,u&gt;fixeddate(<t>-<t>)-int32)([FixedDate](/reference/asna-qsys-runtime/classes/fixed-date.html)([&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics),[&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics)), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's MOVE. Moves right a fixed date into a int4 (int) with pad. | The resulting int value of the operation.
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [MoveRightWithPad&lt;T,U&gt;](#moverightwithpad&lt;t,u&gt;fixeddate(<t>-<t>)-datetimeformat-int32)([FixedDate](/reference/asna-qsys-runtime/classes/fixed-date.html)([&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics),[&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics)), [DateTimeFormat](/reference/datagate-client/date-time-format-enumeration.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's MOVE. Moves right a fixed date into a int4 (int) with pad. | The resulting int value of the operation.
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [MoveRightWithPad&lt;T,U&gt;](#moverightwithpad&lt;t,u&gt;fixeddate(<t>-<t>)-int64)([FixedDate](/reference/asna-qsys-runtime/classes/fixed-date.html)([&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics),[&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics)), [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64)) | RPG's MOVE. Moves right a fixed date into a int8 (long) with pad. | The resulting long value of the operation.
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [MoveRightWithPad&lt;T,U&gt;](#moverightwithpad&lt;t,u&gt;fixeddate(<t>-<t>)-datetimeformat-int64)([FixedDate](/reference/asna-qsys-runtime/classes/fixed-date.html)([&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics),[&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics)), [DateTimeFormat](/reference/datagate-client/date-time-format-enumeration.html), [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64)) | RPG's MOVE. Moves right a fixed date into a int8 (long) with pad. | The resulting long value of the operation.
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [NormalizeYear&lt;T,U&gt;](#normalizeyear&lt;t,u&gt;fixeddate(<t>-<t>))([FixedDate](/reference/asna-qsys-runtime/classes/fixed-date.html)([&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics),[&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics))) | Turns a 4 digit year into a 2 digit year between 1940 and 2039 | The DateTime value with the year portion normalized.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | [ReferenceEquals](https://docs.microsoft.com/en-us/dotnet/api/system.object.referenceequals)([Object](https://docs.microsoft.com/en-us/dotnet/api/system.object), [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | Determines whether the specified Object instances are the same instance.<br>(Inherited from [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | true if objA is the same instance as objB or if both are null; otherwise, false.
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [SubtractDuration&lt;T,U&gt;](#subtractduration&lt;t,u&gt;fixeddate(<t>-<t>)-double-durationcode)([FixedDate](/reference/asna-qsys-runtime/classes/fixed-date.html)([&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics),[&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics)), [Double](https://learn.microsoft.com/en-us/dotnet/api/system.double?view=net-8.0), [DurationCode](/reference/asna-qsys-runtime/date-time-ops-duration-code.html)) | Subtracts a duration span from a date or a timestamp value. | The resulting Date or Timestamp value after subracting from it the given duration.
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [SubtractDurationFromTime&lt;T,U&gt;](#subtractdurationfromtime&lt;t,u&gt;fixeddate(<t>-<t>)-double-durationcode)([FixedDate](/reference/asna-qsys-runtime/classes/fixed-date.html)([&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics),[&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics)), [Double](https://learn.microsoft.com/en-us/dotnet/api/system.double?view=net-8.0), [DurationCode](/reference/asna-qsys-runtime/date-time-ops-duration-code.html)) | Subtracts a duration span from a time value. | The resulting Time value after subtracting from it the given duration.
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [TimestampToDate&lt;T,U&gt;](#timestamptodate&lt;t,u&gt;fixeddate(<t>-<t>))([FixedDate](/reference/asna-qsys-runtime/classes/fixed-date.html)([&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics),[&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics))) | Returns the Date portion of a timestamp. | The DateTime value containing the date portion of the timestamp argument.
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [ToDouble&lt;T,U&gt;](#todouble&lt;t,u&gt;fixeddate(<t>-<t>)-boolean)([FixedDate](/reference/asna-qsys-runtime/classes/fixed-date.html)([&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics),[&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics)), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Converts a fixed date value to double. | The Double number that results from the conversion.
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [ToFixedDecimal&lt;T,U&gt;](#tofixeddecimal&lt;t,u&gt;fixeddate(<t>-<t>)-int32-int32)([FixedDate](/reference/asna-qsys-runtime/classes/fixed-date.html)([&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics),[&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics)), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Converts a fixed date value to a decimal. | The decimal number that results from the conversion.
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [ToFloat&lt;T,U&gt;](#tofloat&lt;t,u&gt;fixeddate(<t>-<t>)-boolean)([FixedDate](/reference/asna-qsys-runtime/classes/fixed-date.html)([&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics),[&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics)), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Converts a fixed date value to float. | The Float number that results from the conversion.
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [ToInt16&lt;T,U&gt;](#toint16&lt;t,u&gt;fixeddate(<t>-<t>)-boolean)([FixedDate](/reference/asna-qsys-runtime/classes/fixed-date.html)([&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics),[&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics)), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Converts a fixed date value to int 16. | The Int16 number that results from the conversion.
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [ToInt32&lt;T,U&gt;](#toint32&lt;t,u&gt;fixeddate(<t>-<t>)-boolean)([FixedDate](/reference/asna-qsys-runtime/classes/fixed-date.html)([&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics),[&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics)), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Converts a fixed date value to int 32. | The Int32 number that results from the conversion.
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [ToInt64&lt;T,U&gt;](#toint64&lt;t,u&gt;fixeddate(<t>-<t>)-boolean)([FixedDate](/reference/asna-qsys-runtime/classes/fixed-date.html)([&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics),[&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics)), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Converts a fixed date value to int 64. | The Int64 number that results from the conversion.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | [ToString](https://docs.microsoft.com/en-us/dotnet/api/system.object.tostring)() | Returns a string that represents the current object.<br>(Inherited from [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | A string that represents the current object.

<br>
<br>

### AddDuration&lt;T,U&gt;([FixedDate](/reference/asna-qsys-runtime/classes/fixed-date.html)([&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics),[&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics)), [Double](https://learn.microsoft.com/en-us/dotnet/api/system.double?view=net-8.0), [DurationCode](/reference/asna-qsys-runtime/date-time-ops-duration-code.html))

Adds a duration span to a date or a timestamp value.

```cs
AddDuration<T,U>(Runtime.FixedDate(<T>, <T>) dateTime, Double duration, Runtime.DateTimeOps.DurationCode durationCode);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [FixedDate(&lt;T&gt;, &lt;T&gt;)](/reference/asna-qsys-runtime/fixed-date.html) | dateTime | .NET DateTime value. 
| [Double](https://learn.microsoft.com/en-us/dotnet/api/system.double?view=net-8.0) | duration | A double value representing duration. 
| [DurationCode](/reference/asna-qsys-runtime/date-time-ops-duration-code.html) | durationCode | Code determining what duration represents. 


<br>
<br>

### AddDurationToTime&lt;T,U&gt;([FixedDate](/reference/asna-qsys-runtime/classes/fixed-date.html)([&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics),[&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics)), [Double](https://learn.microsoft.com/en-us/dotnet/api/system.double?view=net-8.0), [DurationCode](/reference/asna-qsys-runtime/date-time-ops-duration-code.html))

Adds a duration span to a time value.

```cs
AddDurationToTime<T,U>(Runtime.FixedDate(<T>, <T>) dateTime, Double duration, Runtime.DateTimeOps.DurationCode durationCode);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [FixedDate(&lt;T&gt;, &lt;T&gt;)](/reference/asna-qsys-runtime/fixed-date.html) | dateTime | .NET DateTime value specifying a time value. 
| [Double](https://learn.microsoft.com/en-us/dotnet/api/system.double?view=net-8.0) | duration | A double value representing duration. 
| [DurationCode](/reference/asna-qsys-runtime/date-time-ops-duration-code.html) | durationCode | Code determining what duration represents. 


<br>
<br>

### MoveLeft&lt;T,U,V,S&gt;([FixedDate](/reference/asna-qsys-runtime/classes/fixed-date.html)([&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics),[&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics)), [FixedDecimal](/reference/asna-qsys-runtime/classes/fixed-decimal.html)([&lt;T,U&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics),[&lt;T,U,V&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics)))

RPG's MOVEL. Moves left a fixed date to decimal.

```cs
MoveLeft<T,U,V,S>(Runtime.FixedDate(<T>, <T>) fixedDate, Runtime.FixedDecimal(<T,U>, <T,U,V>) targetOperand);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [FixedDate(&lt;T&gt;, &lt;T&gt;)](/reference/asna-qsys-runtime/fixed-date.html) | fixedDate | FixedDate value. 
| [FixedDecimal(&lt;T,U&gt;, &lt;T,U,V&gt;)](/reference/asna-qsys-runtime/fixed-decimal.html) | targetOperand | The targetOperand decimal. 


<br>
<br>

### MoveLeft&lt;T,U,V,S&gt;([FixedDate](/reference/asna-qsys-runtime/classes/fixed-date.html)([&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics),[&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics)), [DateTimeFormat](/reference/datagate-client/date-time-format-enumeration.html), [FixedDecimal](/reference/asna-qsys-runtime/classes/fixed-decimal.html)([&lt;T,U&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics),[&lt;T,U,V&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics)))

RPG's MOVEL. Moves left a fixed date to decimal.

```cs
MoveLeft<T,U,V,S>(Runtime.FixedDate(<T>, <T>) fixedDate, ASNA.DataGate.Common.DateTimeFormat dateTimeFormat, Runtime.FixedDecimal(<T,U>, <T,U,V>) targetOperand);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [FixedDate(&lt;T&gt;, &lt;T&gt;)](/reference/asna-qsys-runtime/fixed-date.html) | fixedDate | FixedDate value. 
| [DateTimeFormat](/reference/datagate-client/date-time-format-enumeration.html) | dateTimeFormat | The date/time format expected for the result. 
| [FixedDecimal(&lt;T,U&gt;, &lt;T,U,V&gt;)](/reference/asna-qsys-runtime/fixed-decimal.html) | targetOperand | The targetOperand decimal. 


<br>
<br>

### MoveLeft&lt;T,U&gt;([FixedDate](/reference/asna-qsys-runtime/classes/fixed-date.html)([&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics),[&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics)), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

RPG's MOVEL. Moves left a fixed date to string.

```cs
MoveLeft<T,U>(Runtime.FixedDate(<T>, <T>) fixedDate, String targetOperand);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [FixedDate(&lt;T&gt;, &lt;T&gt;)](/reference/asna-qsys-runtime/fixed-date.html) | fixedDate | FixedDate value. 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | targetOperand | The targetOperand string. 


<br>
<br>

### MoveLeft&lt;T,U&gt;([FixedDate](/reference/asna-qsys-runtime/classes/fixed-date.html)([&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics),[&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics)), [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16))

RPG's MOVEL. Moves left a fixed date into a int2 (short).

```cs
MoveLeft<T,U>(Runtime.FixedDate(<T>, <T>) fixedDate, Int16 targetOperand);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [FixedDate(&lt;T&gt;, &lt;T&gt;)](/reference/asna-qsys-runtime/fixed-date.html) | fixedDate | FixedDate value. 
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | targetOperand | The short value target of the operation. 


<br>
<br>

### MoveLeft&lt;T,U&gt;([FixedDate](/reference/asna-qsys-runtime/classes/fixed-date.html)([&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics),[&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics)), [DateTimeFormat](/reference/datagate-client/date-time-format-enumeration.html), [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16))

RPG's MOVEL. Moves left a fixed date into a int2 (short).

```cs
MoveLeft<T,U>(Runtime.FixedDate(<T>, <T>) fixedDate, ASNA.DataGate.Common.DateTimeFormat dateTimeFormat, Int16 targetOperand);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [FixedDate(&lt;T&gt;, &lt;T&gt;)](/reference/asna-qsys-runtime/fixed-date.html) | fixedDate | FixedDate value. 
| [DateTimeFormat](/reference/datagate-client/date-time-format-enumeration.html) | dateTimeFormat | The date/time format expected for the result. 
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | targetOperand | The short value target of the operation. 


<br>
<br>

### MoveLeft&lt;T,U&gt;([FixedDate](/reference/asna-qsys-runtime/classes/fixed-date.html)([&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics),[&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics)), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

RPG's MOVEL. Moves left a fixed date into a int4 (int).

```cs
MoveLeft<T,U>(Runtime.FixedDate(<T>, <T>) fixedDate, Int32 targetOperand);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [FixedDate(&lt;T&gt;, &lt;T&gt;)](/reference/asna-qsys-runtime/fixed-date.html) | fixedDate | FixedDate value. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetOperand | The int value target of the operation. 


<br>
<br>

### MoveLeft&lt;T,U&gt;([FixedDate](/reference/asna-qsys-runtime/classes/fixed-date.html)([&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics),[&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics)), [DateTimeFormat](/reference/datagate-client/date-time-format-enumeration.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

RPG's MOVEL. Moves left a fixed date into a int4 (int).

```cs
MoveLeft<T,U>(Runtime.FixedDate(<T>, <T>) fixedDate, ASNA.DataGate.Common.DateTimeFormat dateTimeFormat, Int32 targetOperand);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [FixedDate(&lt;T&gt;, &lt;T&gt;)](/reference/asna-qsys-runtime/fixed-date.html) | fixedDate | FixedDate value. 
| [DateTimeFormat](/reference/datagate-client/date-time-format-enumeration.html) | dateTimeFormat | The date/time format expected for the result. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetOperand | The int value target of the operation. 


<br>
<br>

### MoveLeft&lt;T,U&gt;([FixedDate](/reference/asna-qsys-runtime/classes/fixed-date.html)([&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics),[&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics)), [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64))

RPG's MOVEL. Moves left a fixed date into a int8 (long).

```cs
MoveLeft<T,U>(Runtime.FixedDate(<T>, <T>) fixedDate, Int64 targetOperand);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [FixedDate(&lt;T&gt;, &lt;T&gt;)](/reference/asna-qsys-runtime/fixed-date.html) | fixedDate | FixedDate value. 
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | targetOperand | The long value target of the operation. 


<br>
<br>

### MoveLeft&lt;T,U&gt;([FixedDate](/reference/asna-qsys-runtime/classes/fixed-date.html)([&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics),[&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics)), [DateTimeFormat](/reference/datagate-client/date-time-format-enumeration.html), [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64))

RPG's MOVEL. Moves left a fixed date into a int8 (long).

```cs
MoveLeft<T,U>(Runtime.FixedDate(<T>, <T>) fixedDate, ASNA.DataGate.Common.DateTimeFormat dateTimeFormat, Int64 targetOperand);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [FixedDate(&lt;T&gt;, &lt;T&gt;)](/reference/asna-qsys-runtime/fixed-date.html) | fixedDate | FixedDate value. 
| [DateTimeFormat](/reference/datagate-client/date-time-format-enumeration.html) | dateTimeFormat | The date/time format expected for the result. 
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | targetOperand | The long value target of the operation. 


<br>
<br>

### MoveLeftToChar&lt;T,U&gt;([FixedDate](/reference/asna-qsys-runtime/classes/fixed-date.html)([&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics),[&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics)))

RPG's MOVEL. Moves left a date, time, timestamp in the given format to a char value.

```cs
MoveLeftToChar<T,U>(Runtime.FixedDate(<T>, <T>) fixedDate);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [FixedDate(&lt;T&gt;, &lt;T&gt;)](/reference/asna-qsys-runtime/fixed-date.html) | fixedDate | FixedDate value. 


<br>
<br>

### MoveLeftWithPad&lt;T,U,V,S&gt;([FixedDate](/reference/asna-qsys-runtime/classes/fixed-date.html)([&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics),[&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics)), [FixedDecimal](/reference/asna-qsys-runtime/classes/fixed-decimal.html)([&lt;T,U&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics),[&lt;T,U,V&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics)))

RPG's MOVEL. Moves left a fixed date to decimal with pad.

```cs
MoveLeftWithPad<T,U,V,S>(Runtime.FixedDate(<T>, <T>) fixedDate, Runtime.FixedDecimal(<T,U>, <T,U,V>) targetOperand);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [FixedDate(&lt;T&gt;, &lt;T&gt;)](/reference/asna-qsys-runtime/fixed-date.html) | fixedDate | FixedDate value. 
| [FixedDecimal(&lt;T,U&gt;, &lt;T,U,V&gt;)](/reference/asna-qsys-runtime/fixed-decimal.html) | targetOperand | The targetOperand decimal. 


<br>
<br>

### MoveLeftWithPad&lt;T,U,V,S&gt;([FixedDate](/reference/asna-qsys-runtime/classes/fixed-date.html)([&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics),[&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics)), [DateTimeFormat](/reference/datagate-client/date-time-format-enumeration.html), [FixedDecimal](/reference/asna-qsys-runtime/classes/fixed-decimal.html)([&lt;T,U&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics),[&lt;T,U,V&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics)))

RPG's MOVEL. Moves left a fixed date to decimal with pad.

```cs
MoveLeftWithPad<T,U,V,S>(Runtime.FixedDate(<T>, <T>) fixedDate, ASNA.DataGate.Common.DateTimeFormat dateTimeFormat, Runtime.FixedDecimal(<T,U>, <T,U,V>) targetOperand);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [FixedDate(&lt;T&gt;, &lt;T&gt;)](/reference/asna-qsys-runtime/fixed-date.html) | fixedDate | FixedDate value. 
| [DateTimeFormat](/reference/datagate-client/date-time-format-enumeration.html) | dateTimeFormat | The date/time format expected for the result. 
| [FixedDecimal(&lt;T,U&gt;, &lt;T,U,V&gt;)](/reference/asna-qsys-runtime/fixed-decimal.html) | targetOperand | The targetOperand decimal. 


<br>
<br>

### MoveLeftWithPad&lt;T,U&gt;([FixedDate](/reference/asna-qsys-runtime/classes/fixed-date.html)([&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics),[&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics)), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

RPG's MOVEL. Moves left a fixed date to string with pad.

```cs
MoveLeftWithPad<T,U>(Runtime.FixedDate(<T>, <T>) fixedDate, String targetOperand);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [FixedDate(&lt;T&gt;, &lt;T&gt;)](/reference/asna-qsys-runtime/fixed-date.html) | fixedDate | FixedDate value. 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | targetOperand | The targetOperand string. 


<br>
<br>

### MoveLeftWithPad&lt;T,U&gt;([FixedDate](/reference/asna-qsys-runtime/classes/fixed-date.html)([&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics),[&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics)), [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16))

RPG's MOVE. Moves right a fixed date into a int2 (short) with pad.

```cs
MoveLeftWithPad<T,U>(Runtime.FixedDate(<T>, <T>) fixedDate, Int16 targetOperand);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [FixedDate(&lt;T&gt;, &lt;T&gt;)](/reference/asna-qsys-runtime/fixed-date.html) | fixedDate | FixedDate value. 
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | targetOperand | The short value target of the operation. 


<br>
<br>

### MoveLeftWithPad&lt;T,U&gt;([FixedDate](/reference/asna-qsys-runtime/classes/fixed-date.html)([&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics),[&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics)), [DateTimeFormat](/reference/datagate-client/date-time-format-enumeration.html), [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16))

RPG's MOVE. Moves right a fixed date into a int2 (short) with pad.

```cs
MoveLeftWithPad<T,U>(Runtime.FixedDate(<T>, <T>) fixedDate, ASNA.DataGate.Common.DateTimeFormat dateTimeFormat, Int16 targetOperand);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [FixedDate(&lt;T&gt;, &lt;T&gt;)](/reference/asna-qsys-runtime/fixed-date.html) | fixedDate | FixedDate value. 
| [DateTimeFormat](/reference/datagate-client/date-time-format-enumeration.html) | dateTimeFormat | The date/time format expected for the result. 
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | targetOperand | The short value target of the operation. 


<br>
<br>

### MoveLeftWithPad&lt;T,U&gt;([FixedDate](/reference/asna-qsys-runtime/classes/fixed-date.html)([&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics),[&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics)), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

RPG's MOVEL. Moves left a fixed date into a int4 (int).

```cs
MoveLeftWithPad<T,U>(Runtime.FixedDate(<T>, <T>) fixedDate, Int32 targetOperand);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [FixedDate(&lt;T&gt;, &lt;T&gt;)](/reference/asna-qsys-runtime/fixed-date.html) | fixedDate | FixedDate value. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetOperand | The int value target of the operation. 


<br>
<br>

### MoveLeftWithPad&lt;T,U&gt;([FixedDate](/reference/asna-qsys-runtime/classes/fixed-date.html)([&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics),[&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics)), [DateTimeFormat](/reference/datagate-client/date-time-format-enumeration.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

RPG's MOVEL. Moves left a fixed date into a int4 (int).

```cs
MoveLeftWithPad<T,U>(Runtime.FixedDate(<T>, <T>) fixedDate, ASNA.DataGate.Common.DateTimeFormat dateTimeFormat, Int32 targetOperand);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [FixedDate(&lt;T&gt;, &lt;T&gt;)](/reference/asna-qsys-runtime/fixed-date.html) | fixedDate | FixedDate value. 
| [DateTimeFormat](/reference/datagate-client/date-time-format-enumeration.html) | dateTimeFormat | The date/time format expected for the result. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetOperand | The int value target of the operation. 


<br>
<br>

### MoveLeftWithPad&lt;T,U&gt;([FixedDate](/reference/asna-qsys-runtime/classes/fixed-date.html)([&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics),[&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics)), [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64))

RPG's MOVEL. Moves left a fixed date into a int8 (long).

```cs
MoveLeftWithPad<T,U>(Runtime.FixedDate(<T>, <T>) fixedDate, Int64 targetOperand);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [FixedDate(&lt;T&gt;, &lt;T&gt;)](/reference/asna-qsys-runtime/fixed-date.html) | fixedDate | FixedDate value. 
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | targetOperand | The long value target of the operation. 


<br>
<br>

### MoveLeftWithPad&lt;T,U&gt;([FixedDate](/reference/asna-qsys-runtime/classes/fixed-date.html)([&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics),[&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics)), [DateTimeFormat](/reference/datagate-client/date-time-format-enumeration.html), [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64))

RPG's MOVEL. Moves left a fixed date into a int8 (long).

```cs
MoveLeftWithPad<T,U>(Runtime.FixedDate(<T>, <T>) fixedDate, ASNA.DataGate.Common.DateTimeFormat dateTimeFormat, Int64 targetOperand);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [FixedDate(&lt;T&gt;, &lt;T&gt;)](/reference/asna-qsys-runtime/fixed-date.html) | fixedDate | FixedDate value. 
| [DateTimeFormat](/reference/datagate-client/date-time-format-enumeration.html) | dateTimeFormat | The date/time format expected for the result. 
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | targetOperand | The long value target of the operation. 


<br>
<br>

### MoveRight&lt;T,U,V,S&gt;([FixedDate](/reference/asna-qsys-runtime/classes/fixed-date.html)([&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics),[&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics)), [FixedDecimal](/reference/asna-qsys-runtime/classes/fixed-decimal.html)([&lt;T,U&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics),[&lt;T,U,V&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics)))

RPG's MOVE. Moves right a fixed date to decimal.

```cs
MoveRight<T,U,V,S>(Runtime.FixedDate(<T>, <T>) fixedDate, Runtime.FixedDecimal(<T,U>, <T,U,V>) targetOperand);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [FixedDate(&lt;T&gt;, &lt;T&gt;)](/reference/asna-qsys-runtime/fixed-date.html) | fixedDate | FixedDate value. 
| [FixedDecimal(&lt;T,U&gt;, &lt;T,U,V&gt;)](/reference/asna-qsys-runtime/fixed-decimal.html) | targetOperand | The targetOperand decimal. 


<br>
<br>

### MoveRight&lt;T,U,V,S&gt;([FixedDate](/reference/asna-qsys-runtime/classes/fixed-date.html)([&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics),[&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics)), [DateTimeFormat](/reference/datagate-client/date-time-format-enumeration.html), [FixedDecimal](/reference/asna-qsys-runtime/classes/fixed-decimal.html)([&lt;T,U&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics),[&lt;T,U,V&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics)))

RPG's MOVE. Moves right a fixed date to decimal.

```cs
MoveRight<T,U,V,S>(Runtime.FixedDate(<T>, <T>) fixedDate, ASNA.DataGate.Common.DateTimeFormat dateTimeFormat, Runtime.FixedDecimal(<T,U>, <T,U,V>) targetOperand);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [FixedDate(&lt;T&gt;, &lt;T&gt;)](/reference/asna-qsys-runtime/fixed-date.html) | fixedDate | FixedDate value. 
| [DateTimeFormat](/reference/datagate-client/date-time-format-enumeration.html) | dateTimeFormat | The date/time format expected for the result. 
| [FixedDecimal(&lt;T,U&gt;, &lt;T,U,V&gt;)](/reference/asna-qsys-runtime/fixed-decimal.html) | targetOperand | The targetOperand decimal. 


<br>
<br>

### MoveRight&lt;T,U&gt;([FixedDate](/reference/asna-qsys-runtime/classes/fixed-date.html)([&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics),[&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics)), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

RPG's MOVE. Moves right a fixed date to string.

```cs
MoveRight<T,U>(Runtime.FixedDate(<T>, <T>) fixedDate, String targetOperand);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [FixedDate(&lt;T&gt;, &lt;T&gt;)](/reference/asna-qsys-runtime/fixed-date.html) | fixedDate | FixedDate value. 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | targetOperand | The targetOperand string. 


<br>
<br>

### MoveRight&lt;T,U&gt;([FixedDate](/reference/asna-qsys-runtime/classes/fixed-date.html)([&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics),[&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics)), [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16))

RPG's MOVE. Moves right a fixed date into a int2 (short).

```cs
MoveRight<T,U>(Runtime.FixedDate(<T>, <T>) fixedDate, Int16 targetOperand);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [FixedDate(&lt;T&gt;, &lt;T&gt;)](/reference/asna-qsys-runtime/fixed-date.html) | fixedDate | FixedDate value. 
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | targetOperand | The short value target of the operation. 


<br>
<br>

### MoveRight&lt;T,U&gt;([FixedDate](/reference/asna-qsys-runtime/classes/fixed-date.html)([&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics),[&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics)), [DateTimeFormat](/reference/datagate-client/date-time-format-enumeration.html), [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16))

RPG's MOVE. Moves right a fixed date into a int2 (short).

```cs
MoveRight<T,U>(Runtime.FixedDate(<T>, <T>) fixedDate, ASNA.DataGate.Common.DateTimeFormat dateTimeFormat, Int16 targetOperand);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [FixedDate(&lt;T&gt;, &lt;T&gt;)](/reference/asna-qsys-runtime/fixed-date.html) | fixedDate | FixedDate value. 
| [DateTimeFormat](/reference/datagate-client/date-time-format-enumeration.html) | dateTimeFormat | The date/time format expected for the result. 
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | targetOperand | The short value target of the operation. 


<br>
<br>

### MoveRight&lt;T,U&gt;([FixedDate](/reference/asna-qsys-runtime/classes/fixed-date.html)([&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics),[&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics)), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

RPG's MOVE. Moves right a fixed date into a int4 (int).

```cs
MoveRight<T,U>(Runtime.FixedDate(<T>, <T>) fixedDate, Int32 targetOperand);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [FixedDate(&lt;T&gt;, &lt;T&gt;)](/reference/asna-qsys-runtime/fixed-date.html) | fixedDate | FixedDate value. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetOperand | The int value target of the operation. 


<br>
<br>

### MoveRight&lt;T,U&gt;([FixedDate](/reference/asna-qsys-runtime/classes/fixed-date.html)([&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics),[&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics)), [DateTimeFormat](/reference/datagate-client/date-time-format-enumeration.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

RPG's MOVE. Moves right a fixed date into a int4 (int).

```cs
MoveRight<T,U>(Runtime.FixedDate(<T>, <T>) fixedDate, ASNA.DataGate.Common.DateTimeFormat dateTimeFormat, Int32 targetOperand);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [FixedDate(&lt;T&gt;, &lt;T&gt;)](/reference/asna-qsys-runtime/fixed-date.html) | fixedDate | FixedDate value. 
| [DateTimeFormat](/reference/datagate-client/date-time-format-enumeration.html) | dateTimeFormat | The date/time format expected for the result. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetOperand | The int value target of the operation. 


<br>
<br>

### MoveRight&lt;T,U&gt;([FixedDate](/reference/asna-qsys-runtime/classes/fixed-date.html)([&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics),[&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics)), [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64))

RPG's MOVE. Moves right a fixed date into a int8 (long).

```cs
MoveRight<T,U>(Runtime.FixedDate(<T>, <T>) fixedDate, Int64 targetOperand);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [FixedDate(&lt;T&gt;, &lt;T&gt;)](/reference/asna-qsys-runtime/fixed-date.html) | fixedDate | FixedDate value. 
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | targetOperand | The long value target of the operation. 


<br>
<br>

### MoveRight&lt;T,U&gt;([FixedDate](/reference/asna-qsys-runtime/classes/fixed-date.html)([&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics),[&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics)), [DateTimeFormat](/reference/datagate-client/date-time-format-enumeration.html), [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64))

RPG's MOVE. Moves right a fixed date into a int8 (long).

```cs
MoveRight<T,U>(Runtime.FixedDate(<T>, <T>) fixedDate, ASNA.DataGate.Common.DateTimeFormat dateTimeFormat, Int64 targetOperand);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [FixedDate(&lt;T&gt;, &lt;T&gt;)](/reference/asna-qsys-runtime/fixed-date.html) | fixedDate | FixedDate value. 
| [DateTimeFormat](/reference/datagate-client/date-time-format-enumeration.html) | dateTimeFormat | The date/time format expected for the result. 
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | targetOperand | The long value target of the operation. 


<br>
<br>

### MoveRightToChar&lt;T,U&gt;([FixedDate](/reference/asna-qsys-runtime/classes/fixed-date.html)([&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics),[&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics)))

RPG's MOVE. Moves right a date in the given format to a char value.

```cs
MoveRightToChar<T,U>(Runtime.FixedDate(<T>, <T>) fixedDate);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [FixedDate(&lt;T&gt;, &lt;T&gt;)](/reference/asna-qsys-runtime/fixed-date.html) | fixedDate | FixedDate value. 


<br>
<br>

### MoveRightWithPad&lt;T,U,V,S&gt;([FixedDate](/reference/asna-qsys-runtime/classes/fixed-date.html)([&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics),[&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics)), [FixedDecimal](/reference/asna-qsys-runtime/classes/fixed-decimal.html)([&lt;T,U&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics),[&lt;T,U,V&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics)))

RPG's MOVE. Moves right a fixed date to decimal with pad.

```cs
MoveRightWithPad<T,U,V,S>(Runtime.FixedDate(<T>, <T>) fixedDate, Runtime.FixedDecimal(<T,U>, <T,U,V>) targetOperand);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [FixedDate(&lt;T&gt;, &lt;T&gt;)](/reference/asna-qsys-runtime/fixed-date.html) | fixedDate | FixedDate value. 
| [FixedDecimal(&lt;T,U&gt;, &lt;T,U,V&gt;)](/reference/asna-qsys-runtime/fixed-decimal.html) | targetOperand | The targetOperand decimal. 


<br>
<br>

### MoveRightWithPad&lt;T,U,V,S&gt;([FixedDate](/reference/asna-qsys-runtime/classes/fixed-date.html)([&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics),[&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics)), [DateTimeFormat](/reference/datagate-client/date-time-format-enumeration.html), [FixedDecimal](/reference/asna-qsys-runtime/classes/fixed-decimal.html)([&lt;T,U&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics),[&lt;T,U,V&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics)))

RPG's MOVE. Moves right a fixed date to decimal with pad.

```cs
MoveRightWithPad<T,U,V,S>(Runtime.FixedDate(<T>, <T>) fixedDate, ASNA.DataGate.Common.DateTimeFormat dateTimeFormat, Runtime.FixedDecimal(<T,U>, <T,U,V>) targetOperand);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [FixedDate(&lt;T&gt;, &lt;T&gt;)](/reference/asna-qsys-runtime/fixed-date.html) | fixedDate | FixedDate value. 
| [DateTimeFormat](/reference/datagate-client/date-time-format-enumeration.html) | dateTimeFormat | The date/time format expected for the result. 
| [FixedDecimal(&lt;T,U&gt;, &lt;T,U,V&gt;)](/reference/asna-qsys-runtime/fixed-decimal.html) | targetOperand | The targetOperand decimal. 


<br>
<br>

### MoveRightWithPad&lt;T,U&gt;([FixedDate](/reference/asna-qsys-runtime/classes/fixed-date.html)([&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics),[&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics)), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

RPG's MOVE. Moves right a fixed date to string with pad.

```cs
MoveRightWithPad<T,U>(Runtime.FixedDate(<T>, <T>) fixedDate, String targetOperand);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [FixedDate(&lt;T&gt;, &lt;T&gt;)](/reference/asna-qsys-runtime/fixed-date.html) | fixedDate | FixedDate value. 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | targetOperand | The targetOperand string. 


<br>
<br>

### MoveRightWithPad&lt;T,U&gt;([FixedDate](/reference/asna-qsys-runtime/classes/fixed-date.html)([&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics),[&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics)), [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16))

RPG's MOVE. Moves right a fixed date into a int2 (short) with pad.

```cs
MoveRightWithPad<T,U>(Runtime.FixedDate(<T>, <T>) fixedDate, Int16 targetOperand);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [FixedDate(&lt;T&gt;, &lt;T&gt;)](/reference/asna-qsys-runtime/fixed-date.html) | fixedDate | FixedDate value. 
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | targetOperand | The short value target of the operation. 


<br>
<br>

### MoveRightWithPad&lt;T,U&gt;([FixedDate](/reference/asna-qsys-runtime/classes/fixed-date.html)([&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics),[&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics)), [DateTimeFormat](/reference/datagate-client/date-time-format-enumeration.html), [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16))

RPG's MOVE. Moves right a fixed date into a int2 (short) with pad.

```cs
MoveRightWithPad<T,U>(Runtime.FixedDate(<T>, <T>) fixedDate, ASNA.DataGate.Common.DateTimeFormat dateTimeFormat, Int16 targetOperand);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [FixedDate(&lt;T&gt;, &lt;T&gt;)](/reference/asna-qsys-runtime/fixed-date.html) | fixedDate | FixedDate value. 
| [DateTimeFormat](/reference/datagate-client/date-time-format-enumeration.html) | dateTimeFormat | The date/time format expected for the result. 
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | targetOperand | The short value target of the operation. 


<br>
<br>

### MoveRightWithPad&lt;T,U&gt;([FixedDate](/reference/asna-qsys-runtime/classes/fixed-date.html)([&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics),[&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics)), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

RPG's MOVE. Moves right a fixed date into a int4 (int) with pad.

```cs
MoveRightWithPad<T,U>(Runtime.FixedDate(<T>, <T>) fixedDate, Int32 targetOperand);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [FixedDate(&lt;T&gt;, &lt;T&gt;)](/reference/asna-qsys-runtime/fixed-date.html) | fixedDate | FixedDate value. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetOperand | The int value target of the operation. 


<br>
<br>

### MoveRightWithPad&lt;T,U&gt;([FixedDate](/reference/asna-qsys-runtime/classes/fixed-date.html)([&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics),[&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics)), [DateTimeFormat](/reference/datagate-client/date-time-format-enumeration.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

RPG's MOVE. Moves right a fixed date into a int4 (int) with pad.

```cs
MoveRightWithPad<T,U>(Runtime.FixedDate(<T>, <T>) fixedDate, ASNA.DataGate.Common.DateTimeFormat dateTimeFormat, Int32 targetOperand);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [FixedDate(&lt;T&gt;, &lt;T&gt;)](/reference/asna-qsys-runtime/fixed-date.html) | fixedDate | FixedDate value. 
| [DateTimeFormat](/reference/datagate-client/date-time-format-enumeration.html) | dateTimeFormat | The date/time format expected for the result. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetOperand | The int value target of the operation. 


<br>
<br>

### MoveRightWithPad&lt;T,U&gt;([FixedDate](/reference/asna-qsys-runtime/classes/fixed-date.html)([&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics),[&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics)), [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64))

RPG's MOVE. Moves right a fixed date into a int8 (long) with pad.

```cs
MoveRightWithPad<T,U>(Runtime.FixedDate(<T>, <T>) fixedDate, Int64 targetOperand);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [FixedDate(&lt;T&gt;, &lt;T&gt;)](/reference/asna-qsys-runtime/fixed-date.html) | fixedDate | FixedDate value. 
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | targetOperand | The long value target of the operation. 


<br>
<br>

### MoveRightWithPad&lt;T,U&gt;([FixedDate](/reference/asna-qsys-runtime/classes/fixed-date.html)([&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics),[&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics)), [DateTimeFormat](/reference/datagate-client/date-time-format-enumeration.html), [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64))

RPG's MOVE. Moves right a fixed date into a int8 (long) with pad.

```cs
MoveRightWithPad<T,U>(Runtime.FixedDate(<T>, <T>) fixedDate, ASNA.DataGate.Common.DateTimeFormat dateTimeFormat, Int64 targetOperand);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [FixedDate(&lt;T&gt;, &lt;T&gt;)](/reference/asna-qsys-runtime/fixed-date.html) | fixedDate | FixedDate value. 
| [DateTimeFormat](/reference/datagate-client/date-time-format-enumeration.html) | dateTimeFormat | The date/time format expected for the result. 
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | targetOperand | The long value target of the operation. 


<br>
<br>

### NormalizeYear&lt;T,U&gt;([FixedDate](/reference/asna-qsys-runtime/classes/fixed-date.html)([&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics),[&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics)))

Turns a 4 digit year into a 2 digit year between 1940 and 2039

```cs
NormalizeYear<T,U>(Runtime.FixedDate(<T>, <T>) fixedDate);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [FixedDate(&lt;T&gt;, &lt;T&gt;)](/reference/asna-qsys-runtime/fixed-date.html) | fixedDate | FixedDate value. 


<br>
<br>

### SubtractDuration&lt;T,U&gt;([FixedDate](/reference/asna-qsys-runtime/classes/fixed-date.html)([&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics),[&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics)), [Double](https://learn.microsoft.com/en-us/dotnet/api/system.double?view=net-8.0), [DurationCode](/reference/asna-qsys-runtime/date-time-ops-duration-code.html))

Subtracts a duration span from a date or a timestamp value.

```cs
SubtractDuration<T,U>(Runtime.FixedDate(<T>, <T>) dateTime, Double duration, Runtime.DateTimeOps.DurationCode durationCode);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [FixedDate(&lt;T&gt;, &lt;T&gt;)](/reference/asna-qsys-runtime/fixed-date.html) | dateTime | .NET DateTime value. 
| [Double](https://learn.microsoft.com/en-us/dotnet/api/system.double?view=net-8.0) | duration | A double value representing duration. 
| [DurationCode](/reference/asna-qsys-runtime/date-time-ops-duration-code.html) | durationCode | Code determining what duration represents. 


<br>
<br>

### SubtractDurationFromTime&lt;T,U&gt;([FixedDate](/reference/asna-qsys-runtime/classes/fixed-date.html)([&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics),[&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics)), [Double](https://learn.microsoft.com/en-us/dotnet/api/system.double?view=net-8.0), [DurationCode](/reference/asna-qsys-runtime/date-time-ops-duration-code.html))

Subtracts a duration span from a time value.

```cs
SubtractDurationFromTime<T,U>(Runtime.FixedDate(<T>, <T>) dateTime, Double duration, Runtime.DateTimeOps.DurationCode durationCode);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [FixedDate(&lt;T&gt;, &lt;T&gt;)](/reference/asna-qsys-runtime/fixed-date.html) | dateTime | .NET DateTime value specifying a time value. 
| [Double](https://learn.microsoft.com/en-us/dotnet/api/system.double?view=net-8.0) | duration | A double value representing duration. 
| [DurationCode](/reference/asna-qsys-runtime/date-time-ops-duration-code.html) | durationCode | Code determining what duration represents. 


<br>
<br>

### TimestampToDate&lt;T,U&gt;([FixedDate](/reference/asna-qsys-runtime/classes/fixed-date.html)([&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics),[&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics)))

Returns the Date portion of a timestamp.

```cs
TimestampToDate<T,U>(Runtime.FixedDate(<T>, <T>) fixedDate);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [FixedDate(&lt;T&gt;, &lt;T&gt;)](/reference/asna-qsys-runtime/fixed-date.html) | fixedDate | The timestamp value. 


<br>
<br>

### ToDouble&lt;T,U&gt;([FixedDate](/reference/asna-qsys-runtime/classes/fixed-date.html)([&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics),[&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics)), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Converts a fixed date value to double.

```cs
ToDouble<T,U>(Runtime.FixedDate(<T>, <T>) fixedDate, Boolean throwOnOverflow);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [FixedDate(&lt;T&gt;, &lt;T&gt;)](/reference/asna-qsys-runtime/fixed-date.html) | fixedDate | .NET DateTime type. 
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | throwOnOverflow | Default is false. Pass true if a runtime exception is desired when the conversion doesn't fit. 


<br>
<br>

### ToFixedDecimal&lt;T,U&gt;([FixedDate](/reference/asna-qsys-runtime/classes/fixed-date.html)([&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics),[&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics)), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

Converts a fixed date value to a decimal.

```cs
ToFixedDecimal<T,U>(Runtime.FixedDate(<T>, <T>) fixedDate, Int32 digits, Int32 decimals);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [FixedDate(&lt;T&gt;, &lt;T&gt;)](/reference/asna-qsys-runtime/fixed-date.html) | fixedDate | FixedDate value. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | digits | number of digits in the targetOperand. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | decimals | number of decimal places in the targetOperand. 


<br>
<br>

### ToFloat&lt;T,U&gt;([FixedDate](/reference/asna-qsys-runtime/classes/fixed-date.html)([&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics),[&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics)), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Converts a fixed date value to float.

```cs
ToFloat<T,U>(Runtime.FixedDate(<T>, <T>) fixedDate, Boolean throwOnOverflow);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [FixedDate(&lt;T&gt;, &lt;T&gt;)](/reference/asna-qsys-runtime/fixed-date.html) | fixedDate | .NET DateTime type. 
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | throwOnOverflow | Default is false. Pass true if a runtime exception is desired when the conversion doesn't fit. 


<br>
<br>

### ToInt16&lt;T,U&gt;([FixedDate](/reference/asna-qsys-runtime/classes/fixed-date.html)([&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics),[&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics)), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Converts a fixed date value to int 16.

```cs
ToInt16<T,U>(Runtime.FixedDate(<T>, <T>) fixedDate, Boolean throwOnOverflow);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [FixedDate(&lt;T&gt;, &lt;T&gt;)](/reference/asna-qsys-runtime/fixed-date.html) | fixedDate | FixedDate value. 
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | throwOnOverflow | Default is false. Pass true if a runtime exception is desired when the conversion doesn't fit. 


<br>
<br>

### ToInt32&lt;T,U&gt;([FixedDate](/reference/asna-qsys-runtime/classes/fixed-date.html)([&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics),[&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics)), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Converts a fixed date value to int 32.

```cs
ToInt32<T,U>(Runtime.FixedDate(<T>, <T>) fixedDate, Boolean throwOnOverflow);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [FixedDate(&lt;T&gt;, &lt;T&gt;)](/reference/asna-qsys-runtime/fixed-date.html) | fixedDate | FixedDate value. 
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | throwOnOverflow | Default is false. Pass true if a runtime exception is desired when the conversion doesn't fit. 


<br>
<br>

### ToInt64&lt;T,U&gt;([FixedDate](/reference/asna-qsys-runtime/classes/fixed-date.html)([&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics),[&lt;T&gt;](https://learn.microsoft.com/en-us/dotnet/standard/generics)), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Converts a fixed date value to int 64.

```cs
ToInt64<T,U>(Runtime.FixedDate(<T>, <T>) fixedDate, Boolean throwOnOverflow);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [FixedDate(&lt;T&gt;, &lt;T&gt;)](/reference/asna-qsys-runtime/fixed-date.html) | fixedDate | FixedDate value. 
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | throwOnOverflow | Default is false. Pass true if a runtime exception is desired when the conversion doesn't fit. 


<br>
<br>

