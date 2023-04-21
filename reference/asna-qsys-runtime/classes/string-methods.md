---
title: StringMethods Class
---

Contains extension methods for handling string conversions.

**Namespace:** ASNA.QSys.Runtime <br/>
**Assembly:** ASNA.QSys.Runtime

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> StringMethods

<br>
<br>

## Remarks

Contains extension methods for handling string conversions.

[//]: # ($$TODO: Complete the Remarks section.)

<br>
<br>

## Methods

| Type | Name | Description | Return Description 
| --- | --- | --- | --- 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [AdjustEnd](#adjustendstring-int32)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Adjusts the end of a string. | .
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [AdjustStart](#adjuststartstring-int32)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Adjusts the start of a string. | .
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [AdjustVaryingLength](#adjustvaryinglengthstring-int32)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Trims the end of a variable length string if needed so the string is at most as long as limit. | .
| [Byte](https://docs.microsoft.com/en-us/dotnet/api/system.byte) | [BitOff](#bitoffbyte-string)([Byte](https://docs.microsoft.com/en-us/dotnet/api/system.byte), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | RPG's BITOFF. | Returns the result of bitoff mask being applied to the target.
| [Byte](https://docs.microsoft.com/en-us/dotnet/api/system.byte) | [BitOn](#bitonbyte-string)([Byte](https://docs.microsoft.com/en-us/dotnet/api/system.byte), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | RPG's BITON. | Returns the result of biton mask being applied to the target.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | [CheckCharacters](#checkcharactersstring-string-int32-int32-indicator)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Indicator](/reference/asna-qsys-runtime/classes/indicator.html)) | RPG's CHECK. Verifies that each character in a base string or array is among the characters in the comparator string. | Returns true if a mismatch is found.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | [CheckCharacters](#checkcharactersstring-string-int32-indicator)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Indicator](/reference/asna-qsys-runtime/classes/indicator.html)) | RPG's CHECK. Verifies that each character in a base string or array is among the characters in the comparator string. | Returns true if a mismatch is found.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | [CheckCharacters](#checkcharactersstring-string-int32-int32)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's CHECK. Verifies that each character in a base string or array is among the characters in the comparator string. | Returns true if a mismatch is found.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | [CheckCharacters](#checkcharactersstring-string-int32)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's CHECK. Verifies that each character in a base string or array is among the characters in the comparator string. | Returns true if a mismatch is found.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | [CheckCharacters](#checkcharactersstring-string-int32-array-indicator)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Array]($$TODO-Array.html), [Indicator](/reference/asna-qsys-runtime/classes/indicator.html)) | RPG's CHECK. Verifies that each character in a base string or array is among the characters in the comparator string. | Returns true if a mismatch is found.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | [CheckCharacters](#checkcharactersstring-string-int32-array)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Array]($$TODO-Array.html)) | RPG's CHECK. Verifies that each character in a base string or array is among the characters in the comparator string. | Returns true if a mismatch is found.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | [CheckCharactersReverse](#checkcharactersreversestring-string-int32-int32-indicator)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Indicator](/reference/asna-qsys-runtime/classes/indicator.html)) | RPG's CHECKR. Verifies that each character in a base string or array is among the characters in the comparator string. | Returns true if a mismatch is found.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | [CheckCharactersReverse](#checkcharactersreversestring-string-int32-indicator)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Indicator](/reference/asna-qsys-runtime/classes/indicator.html)) | RPG's CHECKR. Verifies that each character in a base string or array is among the characters in the comparator string. | Returns true if a mismatch is found.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | [CheckCharactersReverse](#checkcharactersreversestring-string-int32-int32)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's CHECKR. Verifies that each character in a base string or array is among the characters in the comparator string. | Returns true if a mismatch is found.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | [CheckCharactersReverse](#checkcharactersreversestring-string-int32)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's CHECKR. Verifies that each character in a base string or array is among the characters in the comparator string. | Returns true if a mismatch is found.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | [CheckCharactersReverse](#checkcharactersreversestring-string-int32-array-indicator)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Array]($$TODO-Array.html), [Indicator](/reference/asna-qsys-runtime/classes/indicator.html)) | RPG's CHECKR. Verifies that each character in a base string or array is among the characters in the comparator string. | Returns true if a mismatch is found.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | [CheckCharactersReverse](#checkcharactersreversestring-string-int32-array)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Array]($$TODO-Array.html)) | RPG's CHECKR. Verifies that each character in a base string or array is among the characters in the comparator string. | Returns true if a mismatch is found.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | [CheckPosition](#checkpositionstring-string)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | RPG's %CHECK. Verifies that each character in the baseString is among the characters in the comparator. | Returns the 1 based position of the first non-matched character in baseString that is not in the comparator.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | [CheckPosition](#checkpositionstring-string-int32)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's %CHECK. Verifies that each character in the baseString is among the characters in the comparator. | Returns the 1 based position of the first non-matched character in baseString that is not in the comparator.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | [CheckPositionReverse](#checkpositionreversestring-string-int32)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's %CHECK. Verifies that each character in the baseString is among the characters in the comparator, starting from the right most position. | Returns the 1 based position of the first non-matched character in baseString that is not in the comparator.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | [CheckPositionReverse](#checkpositionreversestring-string)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | RPG's %CHECK. Verifies that each character in the baseString is among the characters in the comparator, starting from the right most position. | Returns the 1 based position of the first non-matched character in baseString that is not in the comparator.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | [Equals](https://docs.microsoft.com/en-us/dotnet/api/system.object.equals)([Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | Determines whether the specified object is equal to the current object.<br>(Inherited from [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | true if the specified object is equal to the current object; otherwise, false.
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [Finalize](https://docs.microsoft.com/en-us/dotnet/api/system.object.finalize)() | Allows an object to try to free resources and perform other cleanup operations before it is reclaimed by garbage collection.<br>(Inherited from [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | 
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | [FromStringBinary](#fromstringbinarystring-int32-int32)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Returns a (binary) decimal number based on its 'memory' representation. | .
| [Byte](https://docs.microsoft.com/en-us/dotnet/api/system.byte) | [FromStringByte](#fromstringbytestring)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Returns a short number based on its 'memory' representation. | .
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | [FromStringInteger](#fromstringintegerstring)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Returns an integer number based on its 'memory' representation. | .
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | [FromStringLong](#fromstringlongstring)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Returns a long number based on its 'memory' representation. | .
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | [FromStringPacked](#fromstringpackedstring-int32)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Returns a (packed) decimal number based on its 'memory' representation. | .
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | [FromStringShort](#fromstringshortstring)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Returns a short number based on its 'memory' representation. | .
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | [FromStringZoned](#fromstringzonedstring-int32-int32)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Returns a (zoned) decimal number based on its 'memory' representation. | .
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | [GetHashCode](https://docs.microsoft.com/en-us/dotnet/api/system.object.gethashcode)() | Serves as the default hash function.<br>(Inherited from [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | A hash code for the current object.
| [Type](https://docs.microsoft.com/en-us/dotnet/api/system.type) | [GetType](https://docs.microsoft.com/en-us/dotnet/api/system.object.gettype)() | Gets the Type of the current instance.<br>(Inherited from [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | The exact runtime type of the current instance.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | [IsBlanks](#isblanksstring)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Tests a string to see if it is spaces. | .
| [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) | [MemberwiseClone](https://docs.microsoft.com/en-us/dotnet/api/system.object.memberwiseclone)() | Creates a shallow copy of the current Object.<br>(Inherited from [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | A shallow copy of the current Object.
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | [MoveLeft](#moveleftstring-decimal-int32-int32)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's MOVEL. Moves left a numeric string to decimal, without pad. | returns the value of the move.
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | [MoveLeft](#moveleftstring-string)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | RPG's MOVEL. Moves left a string to string, with or without pad. | returns the value of the move.
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | [MoveLeft](#moveleftstring-datetime-datetimedatakind-datetimeformat-datetimeseparator)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind](/reference/asna-qsys-runtime/date-time-data-kind.html), [DateTimeFormat]($$TODO-ASNA.DataGate.Common.DateTimeFormat.html), [DateTimeSeparator](/reference/asna-qsys-runtime/classes/date-time-separator.html)) | RPG's MOVEL. Moves left a string expressed in the given format into a date time type. | returns the value of the move.
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | [MoveLeft](#moveleftstring-int16)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16)) | RPG's MOVEL. Moves left a numeric string into an int2 (short). | returns the value of the move.
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | [MoveLeft](#moveleftstring-int32)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's MOVEL. Moves left a numeric string into an int4 (int). | returns the value of the move.
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | [MoveLeft](#moveleftstring-int64)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64)) | RPG's MOVEL. Moves left a numeric string into an int8 (long). | returns the value of the move.
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [MoveLeft\\`\\`1](#moveleft\`\`1string-fixedtimestamp{``0})([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [FixedTimestamp{\\`\\`0}](/reference/asna-qsys-runtime/fixed-timestamp{``0}.html)) | RPG's MOVEL. Moves left a string expressed in the given format into a date time type. | returns the value of the move.
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [MoveLeft\\`\\`2](#moveleft\`\`2string-fixeddate{``0-``1})([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [FixedDate{\\`\\`0,\\`\\`1}](/reference/asna-qsys-runtime/fixed-date{``0,``1}.html)) | RPG's MOVEL. Moves left a string expressed in the given format into a date time type. | returns the value of the move.
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [MoveLeft\\`\\`2](#moveleft\`\`2string-fixedtime{``0-``1})([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [FixedTime{\\`\\`0,\\`\\`1}](/reference/asna-qsys-runtime/fixed-time{``0,``1}.html)) | RPG's MOVEL. Moves left a string expressed in the given format into a date time type. | returns the value of the move.
| [Char](https://docs.microsoft.com/en-us/dotnet/api/system.char) | [MoveLeftToChar](#movelefttocharstring)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | RPG's MOVE. Moves left a string into a character. | returns the value of the move.
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | [MoveLeftWithPad](#moveleftwithpadstring-decimal-int32-int32)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's MOVEL. Moves left a numeric string to decimal, with pad. | returns the value of the move.
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | [MoveLeftWithPad](#moveleftwithpadstring-string)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | RPG's MOVEL. Moves left a string to string, with pad. | returns the value of the move.
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | [MoveLeftWithPad](#moveleftwithpadstring-int16)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16)) | RPG's MOVEL. Moves left a numeric string into an int2 (short) with pad. | returns the value of the move.
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | [MoveLeftWithPad](#moveleftwithpadstring-int32)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's MOVEL. Moves left a numeric string into an int4 (int) with pad. | returns the value of the move.
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | [MoveLeftWithPad](#moveleftwithpadstring-int64)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64)) | RPG's MOVEL. Moves right a numeric string into an int8 (long) with pad. | returns the value of the move.
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | [MoveRight](#moverightstring-decimal-int32-int32)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's MOVE. Moves right a numeric string to decimal, without pad. | returns the value of the move.
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | [MoveRight](#moverightstring-string)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | RPG's MOVE. Moves right a string to string, without pad. | returns the value of the move.
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | [MoveRight](#moverightstring-datetime-datetimedatakind-datetimeformat-datetimeseparator)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind](/reference/asna-qsys-runtime/date-time-data-kind.html), [DateTimeFormat]($$TODO-ASNA.DataGate.Common.DateTimeFormat.html), [DateTimeSeparator](/reference/asna-qsys-runtime/classes/date-time-separator.html)) | RPG's MOVE. Moves right a string expressed in the given format into a date time type. | returns the value of the move.
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | [MoveRight](#moverightstring-int16)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16)) | RPG's MOVE. Moves right a numeric string into an int2 (short). | returns the value of the move.
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | [MoveRight](#moverightstring-int32)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's MOVE. Moves right a numeric string into an int4 (int). | returns the value of the move.
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | [MoveRight](#moverightstring-int64)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64)) | RPG's MOVE. Moves right a numeric string into an int8 (long). | returns the value of the move.
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [MoveRight\\`\\`1](#moveright\`\`1string-fixedtimestamp{``0})([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [FixedTimestamp{\\`\\`0}](/reference/asna-qsys-runtime/fixed-timestamp{``0}.html)) | RPG's MOVE. Moves right a string expressed in the given format into a date time type. | 
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [MoveRight\\`\\`2](#moveright\`\`2string-fixeddate{``0-``1})([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [FixedDate{\\`\\`0,\\`\\`1}](/reference/asna-qsys-runtime/fixed-date{``0,``1}.html)) | RPG's MOVE. Moves right a string expressed in the given format into a date time type. | 
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [MoveRight\\`\\`2](#moveright\`\`2string-fixedtime{``0-``1})([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [FixedTime{\\`\\`0,\\`\\`1}](/reference/asna-qsys-runtime/fixed-time{``0,``1}.html)) | RPG's MOVE. Moves right a string expressed in the given format into a date time type. | 
| [Char](https://docs.microsoft.com/en-us/dotnet/api/system.char) | [MoveRightToChar](#moverighttocharstring)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | RPG's MOVE. Moves right a string into a character. | returns the value of the move.
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | [MoveRightWithPad](#moverightwithpadstring-decimal-int32-int32)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's MOVE. Moves right a numeric string to decimal, with pad. | returns the value of the move.
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | [MoveRightWithPad](#moverightwithpadstring-string)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | RPG's MOVE. Moves right a string to string, with pad. | returns the value of the move.
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | [MoveRightWithPad](#moverightwithpadstring-int16)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16)) | RPG's MOVE. Moves right a numeric string into an int2 (short) with pad. | returns the value of the move.
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | [MoveRightWithPad](#moverightwithpadstring-int32)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's MOVE. Moves right a numeric string into an int4 (int) with pad. | returns the value of the move.
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | [MoveRightWithPad](#moverightwithpadstring-int64)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64)) | RPG's MOVE. Moves right a numeric string into an int8 (long) with pad. | returns the value of the move.
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [MoveToArray](#movetoarraystring-array-int32)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Array]($$TODO-Array.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Moves a source string into an array. | 
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [MoveToArray\\`\\`2](#movetoarray\`\`2string-ifixedarraybase{``0-``1}-int32)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [IFixedArrayBase{\\`\\`0,\\`\\`1}](/reference/asna-qsys-runtime/i-fixed-array-base{``0,``1}.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Moves a source string into an array. | 
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [MoveToArrayWithPad](#movetoarraywithpadstring-array-int32)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Array]($$TODO-Array.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Moves a source string into an array. | 
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [MoveToArrayWithPad\\`\\`2](#movetoarraywithpad\`\`2string-ifixedarraybase{``0-``1}-int32)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [IFixedArrayBase{\\`\\`0,\\`\\`1}](/reference/asna-qsys-runtime/i-fixed-array-base{``0,``1}.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Moves a source string into an array. | 
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | [ReferenceEquals](https://docs.microsoft.com/en-us/dotnet/api/system.object.referenceequals)([Object](https://docs.microsoft.com/en-us/dotnet/api/system.object), [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | Determines whether the specified Object instances are the same instance.<br>(Inherited from [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | true if objA is the same instance as objB or if both are null; otherwise, false.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [Replace](#replacestring-string-int32-int32-boolean)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | RPG's %SUBST. Replaces characters in a string based on position and length. | .
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [Replace](#replacestring-string-int32-boolean)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | RPG's %SUBST. Replaces characters in a string based on position and length. | .
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [Replace](#replacestring-string-int32-int32)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Replace summary. | Replace returns.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [ReplaceFixed](#replacefixedstring-int32-string-int32-int32)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | ReplaceFixed summary. | ReplaceFixed returns.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | [ScanString](#scanstringstring-string-int32)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's %SCAN. Returns the first position of the search argument in the source string, or 0 if it was not found. | Returns the 1 based starting position of a match relative to the baseString.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | [ScanString](#scanstringstring-string)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | RPG's %SCAN. Returns the first position of the search argument in the source string, or 0 if it was not found. | Returns the 1 based starting position of a match relative to the baseString.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | [ScanString](#scanstringstring-string-int32-int32)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's SCAN. Attempts to find cmpStr in the baseString. | Returns true if cmpStr is found in baseString.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | [ScanString](#scanstringstring-string-int32-int32-indicator)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Indicator](/reference/asna-qsys-runtime/classes/indicator.html)) | RPG's SCAN. Attempts to find cmpStr in the baseString. | Returns true if cmpStr is found in baseString.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | [ScanString](#scanstringstring-string-int32-int32-array)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Array]($$TODO-Array.html)) | RPG's SCAN. Attempts to find cmpStr in the baseString. | Returns true if cmpStr is found in baseString.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | [ScanString](#scanstringstring-string-int32-int32-array-indicator)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Array]($$TODO-Array.html), [Indicator](/reference/asna-qsys-runtime/classes/indicator.html)) | RPG's SCAN. Attempts to find cmpStr in the baseString. | Returns true if cmpStr is found in baseString.
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [ScanString\\`\\`1](#scanstring\`\`1string-string-int32-int32-``0)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [\\`\\`0]($$TODO-``0@.html)) | RPG's SCAN. Attempts to find cmpStr in the baseString. | Returns true if cmpStr is found in baseString.
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [ScanString\\`\\`1](#scanstring\`\`1string-string-int32-int32-``0-indicator)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [\\`\\`0]($$TODO-``0@.html), [Indicator](/reference/asna-qsys-runtime/classes/indicator.html)) | RPG's SCAN. Attempts to find cmpStr in the baseString. | Returns true if cmpStr is found in baseString.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [SetHiLoEq](#sethiloeqstring-indicator-indicator-indicator)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Indicator](/reference/asna-qsys-runtime/classes/indicator.html), [Indicator](/reference/asna-qsys-runtime/classes/indicator.html), [Indicator](/reference/asna-qsys-runtime/classes/indicator.html)) | Sets the flags according to the value of testString. | The test value.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [SetVaryingLength](#setvaryinglengthstring-int32-int32)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Sets the variable length string to the indicated length, ensuring that it is no longer than limit. | .
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [SubStr](#substrstring-int32-int32)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's SUBST. Returns a substring from baseString, starting at startPos ending at subLen, puts it into target, no padding, no preservation of length. | The string value of the result of the SubStr.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [SubStr](#substrstring-int32-int32-indicator)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Indicator](/reference/asna-qsys-runtime/classes/indicator.html)) | RPG's SUBST. Returns a substring from baseString, starting at startPos ending at subLen, puts it into target, no padding, no preservation of length. | .
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [SubStrFixed](#substrfixedstring-int32-int32-string)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | RPG's SUBST. Returns a substring from baseString, starting at startPos ending at subLen, puts it into target. This function preserves the length of the target, no padding. | The string value of the result of the SubStr.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [SubStrFixed](#substrfixedstring-int32-int32-string-indicator)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Indicator](/reference/asna-qsys-runtime/classes/indicator.html)) | RPG's SUBST. Returns a substring from baseString, starting at startPos ending at subLen, puts it into target. This function preserves the length of the target, no padding. | The string value of the result of the SubStr.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [SubStrFixedWithPad](#substrfixedwithpadstring-int32-int32-string)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | RPG's SUBST. Returns a substring from baseString, starting at startPos ending at subLen, puts it into target. This function preserves the length of the target, and pads the result. | The string value of the result of the SubStr.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [SubStrFixedWithPad](#substrfixedwithpadstring-int32-int32-string-indicator)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Indicator](/reference/asna-qsys-runtime/classes/indicator.html)) | RPG's SUBST. Returns a substring from baseString, starting at startPos ending at subLen, puts it into target. This function preserves the length of the target, and pads the result. | The string value of the result of the SubStr.
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | [ToDateTime](#todatetimestring-datetimedatakind-datetimeformat-datetimeseparator)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [DateTimeDataKind](/reference/asna-qsys-runtime/date-time-data-kind.html), [DateTimeFormat]($$TODO-ASNA.DataGate.Common.DateTimeFormat.html), [DateTimeSeparator](/reference/asna-qsys-runtime/classes/date-time-separator.html)) | Converts a string representation of a date/time/timestamp into a DateTime. | .
| [Double]($$TODO-Double.html) | [ToDouble](#todoublestring)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Converts a numeric string into a double number. | double representation of given string.
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | [ToFixedDecimal](#tofixeddecimalstring-int32-int32)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Converts a numeric string into a RPG decimal. | decimal representation of given string.
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | [ToFixedDecimalRounded](#tofixeddecimalroundedstring-int32-int32)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Converts a numeric string into a RPG decimal with rounding (half adjust). | decimal representation of given string.
| [Single]($$TODO-Single.html) | [ToFloat](#tofloatstring)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Converts a numeric string into a float number. | float representation of given string.
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | [ToInt16](#toint16string)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Converts a numeric string into a short number. | short representation of given string.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | [ToInt32](#toint32string)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Converts a numeric string into an int number. | int representation of given string.
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | [ToInt64](#toint64string)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Converts a numeric string into a long number. | long representation of given string.
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | [ToPackedDecimal](#topackeddecimalstring-int32)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Converts a string representing a packed number into a RPG decimal. | decimal packed representation of given string.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | [ToString](https://docs.microsoft.com/en-us/dotnet/api/system.object.tostring)() | Returns a string that represents the current object.<br>(Inherited from [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | A string that represents the current object.
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | [ToZonedDecimal](#tozoneddecimalstring-int32-int32)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Converts a zoned representation string into a RPG decimal. | decimal representation of given string.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [Xlate](#xlatestring-string-string-int32)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's %Xlate. Translates baseString according to the values of mapFrom, mapTo, and startPos. | The string resulting after the Xlate operation.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [Xlate](#xlatestring-string-string-int32-indicator)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Indicator](/reference/asna-qsys-runtime/classes/indicator.html)) | RPG's %Xlate. Translates baseString according to the values of mapFrom, mapTo, and startPos. The parameter errInd will indicate if there was an error in the operation. | The string resulting after the Xlate operation.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [Xlate](#xlatestring-string-string-string-int32)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's XLATE. Translates characters in the baseString according to MapFrom, MapTo, startPos and targetString, no padding, no preservation of length. | The string value of the result of the Xlate.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [Xlate](#xlatestring-string-string-string-int32-indicator)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Indicator](/reference/asna-qsys-runtime/classes/indicator.html)) | RPG's XLATE. Translates characters in the baseString according to MapFrom, MapTo, startPos and targetString, no padding, no preservation of length. | The string value of the result of the Xlate.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [XlateFixed](#xlatefixedstring-string-string-string-int32)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's XLATE. Translates characters in the baseString according to MapFrom, MapTo, startPos and targetString. This version preserves the length of the result, does NOT pad. | The string value of the result of the Xlate.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [XlateFixed](#xlatefixedstring-string-string-string-int32-indicator)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Indicator](/reference/asna-qsys-runtime/classes/indicator.html)) | RPG's XLATE. Translates characters in the baseString according to MapFrom, MapTo, startPos and targetString. This version preserves the length of the result, does NOT pad. | The string value of the result of the Xlate.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [XlateFixedWithPad](#xlatefixedwithpadstring-string-string-string-int32)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's XLATE. Translates characters in the baseString according to MapFrom, MapTo, startPos and targetString. This version preserves the length of the result, with padding. | The string value of the result of the Xlate.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [XlateFixedWithPad](#xlatefixedwithpadstring-string-string-string-int32-indicator)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Indicator](/reference/asna-qsys-runtime/classes/indicator.html)) | RPG's XLATE. Translates characters in the baseString according to MapFrom, MapTo, startPos and targetString. This version preserves the length of the result, with padding. | The string value of the result of the Xlate.

<br>
<br>

### AdjustEnd([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

Adjusts the end of a string.

```cs
AdjustEnd(String charStr, Int32 length);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | charStr | any string. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | length | number to adjust, if greater than length charStr will pad. 

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

.


<br>
<br>

### AdjustStart([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

Adjusts the start of a string.

```cs
AdjustStart(String charStr, Int32 length);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | charStr | any string. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | length | number to adjust, if greater than length charStr will pad the begining. 

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

.


<br>
<br>

### AdjustVaryingLength([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

Trims the end of a variable length string if needed so the string is at most as long as limit.

```cs
AdjustVaryingLength(String charStr, Int32 limit);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | charStr | A variable length string. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | limit | Maximum length allowed for the string. 

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

.


<br>
<br>

### BitOff([Byte](https://docs.microsoft.com/en-us/dotnet/api/system.byte), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

RPG's BITOFF.

```cs
BitOff(Byte target, String mask);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Byte](https://docs.microsoft.com/en-us/dotnet/api/system.byte) | target | A one-position character field. 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | mask | Bit numbers 0-7. Enclose the bit numbers in apostrophes. For example, to set bits 0, 3, 6 on, enter '036'. A valid character expression. 

#### Returns

[Byte](https://docs.microsoft.com/en-us/dotnet/api/system.byte)

Returns the result of bitoff mask being applied to the target.


<br>
<br>

### BitOn([Byte](https://docs.microsoft.com/en-us/dotnet/api/system.byte), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

RPG's BITON.

```cs
BitOn(Byte target, String mask);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Byte](https://docs.microsoft.com/en-us/dotnet/api/system.byte) | target | A one-position character field. 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | mask | Bit numbers 0-7. Enclose the bit numbers in apostrophes. For example, to set bits 0, 3, 6 on, enter '036'. A valid character expression. 

#### Returns

[Byte](https://docs.microsoft.com/en-us/dotnet/api/system.byte)

Returns the result of biton mask being applied to the target.


<br>
<br>

### CheckCharacters([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Indicator](/reference/asna-qsys-runtime/classes/indicator.html))

RPG's CHECK. Verifies that each character in a base string or array is among the characters in the comparator string.

```cs
CheckCharacters(String baseString, String comparator, Int32 startPos, ref Int32 noMatch, ref ASNA.QSys.Runtime.Indicator err);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | baseString | A character expression that contains the string to compare with comparator. 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | comparator | A character expression that is used to compare against the baseString. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | startPos | Specifies the 1-based starting position and continues to the right of the baseString. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | noMatch | Returns the 1 based position of the first non-matched character in baseString that is not in the comparator. 
| [Indicator](/reference/asna-qsys-runtime/classes/indicator.html) | err | Indicator will be set if a runtime error occurs. 

#### Returns

[Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)

Returns true if a mismatch is found.


<br>
<br>

### CheckCharacters([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Indicator](/reference/asna-qsys-runtime/classes/indicator.html))

RPG's CHECK. Verifies that each character in a base string or array is among the characters in the comparator string.

```cs
CheckCharacters(String baseString, String comparator, Int32 startPos, ref ASNA.QSys.Runtime.Indicator err);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | baseString | A character expression that contains the string to compare with comparator. 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | comparator | A character expression that is used to compare against the baseString. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | startPos | Specifies the 1-based starting position and continues to the right of the baseString. 
| [Indicator](/reference/asna-qsys-runtime/classes/indicator.html) | err | Indicator will be set if a runtime error occurs. 

#### Returns

[Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)

Returns true if a mismatch is found.


<br>
<br>

### CheckCharacters([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

RPG's CHECK. Verifies that each character in a base string or array is among the characters in the comparator string.

```cs
CheckCharacters(String baseString, String comparator, Int32 startPos, ref Int32 noMatch);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | baseString | A character expression that contains the string to compare with comparator. 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | comparator | A character expression that is used to compare against the baseString. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | startPos | Specifies the 1-based starting position and continues to the right of the baseString. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | noMatch | Returns the 1-based position of the first non-matched character in baseString that is not in the comparator. 

#### Returns

[Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)

Returns true if a mismatch is found.


<br>
<br>

### CheckCharacters([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

RPG's CHECK. Verifies that each character in a base string or array is among the characters in the comparator string.

```cs
CheckCharacters(String baseString, String comparator, Int32 startPos);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | baseString | A character expression that contains the string to compare with comparator. 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | comparator | A character expression that is used to compare against the baseString. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | startPos | Specifies the 1-based starting position and continues to the right of the baseString. 

#### Returns

[Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)

Returns true if a mismatch is found.


<br>
<br>

### CheckCharacters([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Array]($$TODO-Array.html), [Indicator](/reference/asna-qsys-runtime/classes/indicator.html))

RPG's CHECK. Verifies that each character in a base string or array is among the characters in the comparator string.

```cs
CheckCharacters(String baseString, String comparator, Int32 startPos, Array noMatchArray, ref ASNA.QSys.Runtime.Indicator err);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | baseString | A character expression that contains the string to compare with comparator. 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | comparator | A character expression that is used to compare against the baseString. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | startPos | Specifies the 1-based starting position and continues to the right of the baseString. 
| [Array]($$TODO-Array.html) | noMatchArray | Returns all of the 1-based positions of characters that don't match. The first element in the array contains the leftmost non-match. 
| [Indicator](/reference/asna-qsys-runtime/classes/indicator.html) | err | Indicator will be set if a runtime error occurs. 

#### Returns

[Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)

Returns true if a mismatch is found.


<br>
<br>

### CheckCharacters([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Array]($$TODO-Array.html))

RPG's CHECK. Verifies that each character in a base string or array is among the characters in the comparator string.

```cs
CheckCharacters(String baseString, String comparator, Int32 startPos, Array noMatchArray);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | baseString | A character expression that contains the string to compare with comparator. 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | comparator | A character expression that is used to compare against the baseString. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | startPos | Specifies the 1-based starting position and continues to the right of the baseString. 
| [Array]($$TODO-Array.html) | noMatchArray | Returns all of the 1-based positions of characters that don't match. The first element in the array contains the leftmost non-match. 

#### Returns

[Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)

Returns true if a mismatch is found.


<br>
<br>

### CheckCharactersReverse([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Indicator](/reference/asna-qsys-runtime/classes/indicator.html))

RPG's CHECKR. Verifies that each character in a base string or array is among the characters in the comparator string.

```cs
CheckCharactersReverse(String baseString, String comparator, Int32 startPos, ref Int32 noMatch, ref ASNA.QSys.Runtime.Indicator err);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | baseString | A character expression that contains the string to compare with comparator. 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | comparator | A character expression that is used to compare against the baseString. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | startPos | Specifies the 1-based starting position and continues to the left of the baseString. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | noMatch | Returns the 1-based position of the first non-matched character in baseString that is not in the comparator. 
| [Indicator](/reference/asna-qsys-runtime/classes/indicator.html) | err | Indicator will be set if a runtime error occurs. 

#### Returns

[Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)

Returns true if a mismatch is found.


<br>
<br>

### CheckCharactersReverse([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Indicator](/reference/asna-qsys-runtime/classes/indicator.html))

RPG's CHECKR. Verifies that each character in a base string or array is among the characters in the comparator string.

```cs
CheckCharactersReverse(String baseString, String comparator, Int32 startPos, ref ASNA.QSys.Runtime.Indicator err);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | baseString | A character expression that contains the string to compare with comparator. 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | comparator | A character expression that is used to compare against the baseString. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | startPos | Specifies the 1-based starting position and continues to the left of the baseString. 
| [Indicator](/reference/asna-qsys-runtime/classes/indicator.html) | err | Indicator will be set if a runtime error occurs. 

#### Returns

[Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)

Returns true if a mismatch is found.


<br>
<br>

### CheckCharactersReverse([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

RPG's CHECKR. Verifies that each character in a base string or array is among the characters in the comparator string.

```cs
CheckCharactersReverse(String baseString, String comparator, Int32 startPos, ref Int32 noMatch);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | baseString | A character expression that contains the string to compare with comparator. 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | comparator | A character expression that is used to compare against the baseString. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | startPos | Specifies the 1-based starting position and continues to the left of the baseString. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | noMatch | Returns the 1-based position of the first non-matched character in baseString that is not in the comparator. 

#### Returns

[Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)

Returns true if a mismatch is found.


<br>
<br>

### CheckCharactersReverse([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

RPG's CHECKR. Verifies that each character in a base string or array is among the characters in the comparator string.

```cs
CheckCharactersReverse(String baseString, String comparator, Int32 startPos);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | baseString | A character expression that contains the string to compare with comparator. 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | comparator | A character expression that is used to compare against the baseString. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | startPos | Specifies the 1-based starting position and continues to the left of the baseString. 

#### Returns

[Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)

Returns true if a mismatch is found.


<br>
<br>

### CheckCharactersReverse([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Array]($$TODO-Array.html), [Indicator](/reference/asna-qsys-runtime/classes/indicator.html))

RPG's CHECKR. Verifies that each character in a base string or array is among the characters in the comparator string.

```cs
CheckCharactersReverse(String baseString, String comparator, Int32 startPos, Array noMatchArray, ref ASNA.QSys.Runtime.Indicator err);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | baseString | A character expression that contains the string to compare with comparator. 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | comparator | A character expression that is used to compare against the baseString. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | startPos | Specifies the 1-based starting position and continues to the left of the baseString. 
| [Array]($$TODO-Array.html) | noMatchArray | Returns the 1-based position of the first non-matched character in baseString that is not in the comparator.
            The first index in NoMatchArray is the rightmost mismatch in the baseString. 
| [Indicator](/reference/asna-qsys-runtime/classes/indicator.html) | err | Indicator will be set if a runtime error occurs. 

#### Returns

[Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)

Returns true if a mismatch is found.


<br>
<br>

### CheckCharactersReverse([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Array]($$TODO-Array.html))

RPG's CHECKR. Verifies that each character in a base string or array is among the characters in the comparator string.

```cs
CheckCharactersReverse(String baseString, String comparator, Int32 startPos, Array noMatchArray);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | baseString | A character expression that contains the string to compare with comparator. 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | comparator | A character expression that is used to compare against the baseString. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | startPos | Specifies the 1-based starting position and continues to the left of the baseString. 
| [Array]($$TODO-Array.html) | noMatchArray | Returns the 1-based position of the first non-matched character in baseString that is not in the comparator.
            The first index in NoMatchArray is the rightmost mismatch in the baseString. 

#### Returns

[Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)

Returns true if a mismatch is found.


<br>
<br>

### CheckPosition([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

RPG's %CHECK. Verifies that each character in the baseString is among the characters in the comparator.

```cs
CheckPosition(String baseString, String comparator);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | baseString | A character expression that contains the string to compare with comparator. 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | comparator | A character expression that is used to compare against the baseString. 

#### Returns

[Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)

Returns the 1 based position of the first non-matched character in baseString that is not in the comparator.


<br>
<br>

### CheckPosition([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

RPG's %CHECK. Verifies that each character in the baseString is among the characters in the comparator.

```cs
CheckPosition(String baseString, String comparator, Int32 startPos);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | baseString | A character expression that contains the string to compare with comparator. 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | comparator | A character expression that is used to compare against the baseString. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | startPos | Default Position 1, not zero based.  Specifies the start position from the left most position. 

#### Returns

[Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)

Returns the 1 based position of the first non-matched character in baseString that is not in the comparator.


<br>
<br>

### CheckPositionReverse([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

RPG's %CHECK. Verifies that each character in the baseString is among the characters in the comparator, starting from the right most position.

```cs
CheckPositionReverse(String baseString, String comparator, Int32 startPos);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | baseString | A character expression that contains the string to compare with comparator. 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | comparator | A character expression that is used to compare against the baseString. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | startPos | Default Position end of string, not zero based.  Specifies the start position from the left most position. 

#### Returns

[Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)

Returns the 1 based position of the first non-matched character in baseString that is not in the comparator.


<br>
<br>

### CheckPositionReverse([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

RPG's %CHECK. Verifies that each character in the baseString is among the characters in the comparator, starting from the right most position.

```cs
CheckPositionReverse(String baseString, String comparator);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | baseString | A character expression that contains the string to compare with comparator. 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | comparator | A character expression that is used to compare against the baseString. 

#### Returns

[Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)

Returns the 1 based position of the first non-matched character in baseString that is not in the comparator.


<br>
<br>

### FromStringBinary([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

Returns a (binary) decimal number based on its 'memory' representation.

```cs
FromStringBinary(String num, Int32 digits, Int32 decimals);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | num | The string representation of the number. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | digits | The number of digits in the decimal number. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | decimals | The number of decimal positions in the decimal number. 

#### Returns

[Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal)

.


<br>
<br>

### FromStringByte([String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Returns a short number based on its 'memory' representation.

```cs
FromStringByte(String num);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | num | The string representation of the number. 

#### Returns

[Byte](https://docs.microsoft.com/en-us/dotnet/api/system.byte)

.


<br>
<br>

### FromStringInteger([String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Returns an integer number based on its 'memory' representation.

```cs
FromStringInteger(String num);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | num | The string representation of the number. 

#### Returns

[Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)

.


<br>
<br>

### FromStringLong([String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Returns a long number based on its 'memory' representation.

```cs
FromStringLong(String num);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | num | The string representation of the number. 

#### Returns

[Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64)

.


<br>
<br>

### FromStringPacked([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

Returns a (packed) decimal number based on its 'memory' representation.

```cs
FromStringPacked(String num, Int32 decimals);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | num | The string representation of the number. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | decimals | The number of decimal positions in the decimal number. 

#### Returns

[Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal)

.


<br>
<br>

### FromStringShort([String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Returns a short number based on its 'memory' representation.

```cs
FromStringShort(String num);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | num | The string representation of the number. 

#### Returns

[Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16)

.


<br>
<br>

### FromStringZoned([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

Returns a (zoned) decimal number based on its 'memory' representation.

```cs
FromStringZoned(String num, Int32 digits, Int32 decimals);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | num | The string representation of the number. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | digits | The total number of digits the decimal has. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | decimals | The number of decimal positions in the decimal number. 

#### Returns

[Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal)

.


<br>
<br>

### IsBlanks([String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Tests a string to see if it is spaces.

```cs
IsBlanks(String arg);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | arg | . 

#### Returns

[Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)

.


<br>
<br>

### MoveLeft([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

RPG's MOVEL. Moves left a numeric string to decimal, without pad.

```cs
MoveLeft(String charStr, Decimal targetOperand, Int32 targetOperandDig, Int32 targetOperandDec);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | charStr | string representing a decimal number. 
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | targetOperand | decimal number of the targetOperand number. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetOperandDig | number of digits in targetOperand. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetOperandDec | number of decimals in targetOperand. 

#### Returns

[DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime)

returns the value of the move.


<br>
<br>

### MoveLeft([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

RPG's MOVEL. Moves left a string to string, with or without pad.

```cs
MoveLeft(String charStr, String targetOperand);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | charStr | any string. 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | targetOperand | string targetOperand. 

#### Returns

[DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime)

returns the value of the move.


<br>
<br>

### MoveLeft([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind](/reference/asna-qsys-runtime/date-time-data-kind.html), [DateTimeFormat]($$TODO-ASNA.DataGate.Common.DateTimeFormat.html), [DateTimeSeparator](/reference/asna-qsys-runtime/classes/date-time-separator.html))

RPG's MOVEL. Moves left a string expressed in the given format into a date time type.

```cs
MoveLeft(String charStr, DateTime dateTime, ASNA.QSys.Runtime.DateTimeDataKind dateTimeKind, ASNA.DataGate.Common.DateTimeFormat dateTimeFormat, ASNA.QSys.Runtime.DateTimeSeparator dateTimeSeparator);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | charStr | Source string. 
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | dateTime | Destination DateTime. 
| [DateTimeDataKind](/reference/asna-qsys-runtime/date-time-data-kind.html) | dateTimeKind | Date, Time, Timestamp. 
| [DateTimeFormat]($$TODO-ASNA.DataGate.Common.DateTimeFormat.html) | dateTimeFormat | DateTime format. 
| [DateTimeSeparator](/reference/asna-qsys-runtime/classes/date-time-separator.html) | dateTimeSeparator | string separator. 

#### Returns

[DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime)

returns the value of the move.


<br>
<br>

### MoveLeft([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16))

RPG's MOVEL. Moves left a numeric string into an int2 (short).

```cs
MoveLeft(String charStr, Int16 targetOperand);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | charStr | Source numeric string. 
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | targetOperand | Short value of the target. 

#### Returns

[DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime)

returns the value of the move.


<br>
<br>

### MoveLeft([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

RPG's MOVEL. Moves left a numeric string into an int4 (int).

```cs
MoveLeft(String charStr, Int32 targetOperand);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | charStr | Source numeric string. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetOperand | Int value of the target. 

#### Returns

[DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime)

returns the value of the move.


<br>
<br>

### MoveLeft([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64))

RPG's MOVEL. Moves left a numeric string into an int8 (long).

```cs
MoveLeft(String charStr, Int64 targetOperand);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | charStr | Source numeric string. 
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | targetOperand | Long value of the target. 

#### Returns

[DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime)

returns the value of the move.


<br>
<br>

### MoveLeft\`\`1([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [FixedTimestamp{\\`\\`0}](/reference/asna-qsys-runtime/fixed-timestamp{``0}.html))

RPG's MOVEL. Moves left a string expressed in the given format into a date time type.

```cs
MoveLeft``1(String charStr, ASNA.QSys.Runtime.FixedTimestamp{``0} timeStamp);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | charStr | Source FixedString. 
| [FixedTimestamp{\\`\\`0}](/reference/asna-qsys-runtime/fixed-timestamp{``0}.html) | timeStamp | Destination FixedTimestamp. 


<br>
<br>

### MoveLeft\`\`2([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [FixedDate{\\`\\`0,\\`\\`1}](/reference/asna-qsys-runtime/fixed-date{``0,``1}.html))

RPG's MOVEL. Moves left a string expressed in the given format into a date time type.

```cs
MoveLeft``2(String charStr, ASNA.QSys.Runtime.FixedDate{``0,``1} date);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | charStr | Source FixedString. 
| [FixedDate{\\`\\`0,\\`\\`1}](/reference/asna-qsys-runtime/fixed-date{``0,``1}.html) | date | Destination FixedDate. 


<br>
<br>

### MoveLeft\`\`2([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [FixedTime{\\`\\`0,\\`\\`1}](/reference/asna-qsys-runtime/fixed-time{``0,``1}.html))

RPG's MOVEL. Moves left a string expressed in the given format into a date time type.

```cs
MoveLeft``2(String charStr, ASNA.QSys.Runtime.FixedTime{``0,``1} time);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | charStr | Source FixedString. 
| [FixedTime{\\`\\`0,\\`\\`1}](/reference/asna-qsys-runtime/fixed-time{``0,``1}.html) | time | Destination FixedTime. 


<br>
<br>

### MoveLeftToChar([String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

RPG's MOVE. Moves left a string into a character.

```cs
MoveLeftToChar(String charStr);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | charStr | A string the represents the source of the move. 

#### Returns

[Char](https://docs.microsoft.com/en-us/dotnet/api/system.char)

returns the value of the move.


<br>
<br>

### MoveLeftWithPad([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

RPG's MOVEL. Moves left a numeric string to decimal, with pad.

```cs
MoveLeftWithPad(String charStr, Decimal targetOperand, Int32 targetOperandDig, Int32 targetOperandDec);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | charStr | string representing a decimal number. 
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | targetOperand | decimal number of the targetOperand number. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetOperandDig | number of digits in targetOperand. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetOperandDec | number of decimals in targetOperand. 

#### Returns

[Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16)

returns the value of the move.


<br>
<br>

### MoveLeftWithPad([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

RPG's MOVEL. Moves left a string to string, with pad.

```cs
MoveLeftWithPad(String charStr, String targetOperand);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | charStr | any string. 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | targetOperand | string targetOperand. 

#### Returns

[Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16)

returns the value of the move.


<br>
<br>

### MoveLeftWithPad([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16))

RPG's MOVEL. Moves left a numeric string into an int2 (short) with pad.

```cs
MoveLeftWithPad(String charStr, Int16 targetOperand);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | charStr | Source numeric string. 
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | targetOperand | Short value of the target. 

#### Returns

[Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16)

returns the value of the move.


<br>
<br>

### MoveLeftWithPad([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

RPG's MOVEL. Moves left a numeric string into an int4 (int) with pad.

```cs
MoveLeftWithPad(String charStr, Int32 targetOperand);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | charStr | Source numeric string. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetOperand | Int value of the target. 

#### Returns

[Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16)

returns the value of the move.


<br>
<br>

### MoveLeftWithPad([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64))

RPG's MOVEL. Moves right a numeric string into an int8 (long) with pad.

```cs
MoveLeftWithPad(String charStr, Int64 targetOperand);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | charStr | Source numeric string. 
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | targetOperand | Long value of the target. 

#### Returns

[Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16)

returns the value of the move.


<br>
<br>

### MoveRight([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

RPG's MOVE. Moves right a numeric string to decimal, without pad.

```cs
MoveRight(String charStr, Decimal targetOperand, Int32 targetOperandDig, Int32 targetOperandDec);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | charStr | string representing a decimal number. 
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | targetOperand | decimal number of the targetOperand number. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetOperandDig | number of digits in targetOperand. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetOperandDec | number of decimals in targetOperand. 

#### Returns

[DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime)

returns the value of the move.


<br>
<br>

### MoveRight([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

RPG's MOVE. Moves right a string to string, without pad.

```cs
MoveRight(String charStr, String targetOperand);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | charStr | any string. 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | targetOperand | string targetOperand. 

#### Returns

[DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime)

returns the value of the move.


<br>
<br>

### MoveRight([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind](/reference/asna-qsys-runtime/date-time-data-kind.html), [DateTimeFormat]($$TODO-ASNA.DataGate.Common.DateTimeFormat.html), [DateTimeSeparator](/reference/asna-qsys-runtime/classes/date-time-separator.html))

RPG's MOVE. Moves right a string expressed in the given format into a date time type.

```cs
MoveRight(String charStr, DateTime dateTime, ASNA.QSys.Runtime.DateTimeDataKind dateTimeKind, ASNA.DataGate.Common.DateTimeFormat dateTimeFormat, ASNA.QSys.Runtime.DateTimeSeparator dateTimeSeparator);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | charStr | Source string. 
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | dateTime | Destination DateTime. 
| [DateTimeDataKind](/reference/asna-qsys-runtime/date-time-data-kind.html) | dateTimeKind | Date, Time, Timestamp. 
| [DateTimeFormat]($$TODO-ASNA.DataGate.Common.DateTimeFormat.html) | dateTimeFormat | DateTime format. 
| [DateTimeSeparator](/reference/asna-qsys-runtime/classes/date-time-separator.html) | dateTimeSeparator | string separator. 

#### Returns

[DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime)

returns the value of the move.


<br>
<br>

### MoveRight([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16))

RPG's MOVE. Moves right a numeric string into an int2 (short).

```cs
MoveRight(String charStr, Int16 targetOperand);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | charStr | Source numeric string. 
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | targetOperand | Short value of the target. 

#### Returns

[DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime)

returns the value of the move.


<br>
<br>

### MoveRight([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

RPG's MOVE. Moves right a numeric string into an int4 (int).

```cs
MoveRight(String charStr, Int32 targetOperand);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | charStr | Source numeric string. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetOperand | Int value of the target. 

#### Returns

[DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime)

returns the value of the move.


<br>
<br>

### MoveRight([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64))

RPG's MOVE. Moves right a numeric string into an int8 (long).

```cs
MoveRight(String charStr, Int64 targetOperand);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | charStr | Source numeric string. 
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | targetOperand | Long value of the target. 

#### Returns

[DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime)

returns the value of the move.


<br>
<br>

### MoveRight\`\`1([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [FixedTimestamp{\\`\\`0}](/reference/asna-qsys-runtime/fixed-timestamp{``0}.html))

RPG's MOVE. Moves right a string expressed in the given format into a date time type.

```cs
MoveRight``1(String charStr, ASNA.QSys.Runtime.FixedTimestamp{``0} timeStamp);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | charStr | Source FixedString. 
| [FixedTimestamp{\\`\\`0}](/reference/asna-qsys-runtime/fixed-timestamp{``0}.html) | timeStamp | Destination FixedTimestamp. 


<br>
<br>

### MoveRight\`\`2([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [FixedDate{\\`\\`0,\\`\\`1}](/reference/asna-qsys-runtime/fixed-date{``0,``1}.html))

RPG's MOVE. Moves right a string expressed in the given format into a date time type.

```cs
MoveRight``2(String charStr, ASNA.QSys.Runtime.FixedDate{``0,``1} date);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | charStr | Source FixedString. 
| [FixedDate{\\`\\`0,\\`\\`1}](/reference/asna-qsys-runtime/fixed-date{``0,``1}.html) | date | Destination FixedDate. 


<br>
<br>

### MoveRight\`\`2([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [FixedTime{\\`\\`0,\\`\\`1}](/reference/asna-qsys-runtime/fixed-time{``0,``1}.html))

RPG's MOVE. Moves right a string expressed in the given format into a date time type.

```cs
MoveRight``2(String charStr, ASNA.QSys.Runtime.FixedTime{``0,``1} time);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | charStr | Source FixedString. 
| [FixedTime{\\`\\`0,\\`\\`1}](/reference/asna-qsys-runtime/fixed-time{``0,``1}.html) | time | Destination FixedTime. 


<br>
<br>

### MoveRightToChar([String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

RPG's MOVE. Moves right a string into a character.

```cs
MoveRightToChar(String charStr);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | charStr | A string the represents the source of the move. 

#### Returns

[Char](https://docs.microsoft.com/en-us/dotnet/api/system.char)

returns the value of the move.


<br>
<br>

### MoveRightWithPad([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

RPG's MOVE. Moves right a numeric string to decimal, with pad.

```cs
MoveRightWithPad(String charStr, Decimal targetOperand, Int32 targetOperandDig, Int32 targetOperandDec);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | charStr | string representing a decimal number. 
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | targetOperand | decimal number of the targetOperand number. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetOperandDig | number of digits in targetOperand. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetOperandDec | number of decimals in targetOperand. 

#### Returns

[Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16)

returns the value of the move.


<br>
<br>

### MoveRightWithPad([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

RPG's MOVE. Moves right a string to string, with pad.

```cs
MoveRightWithPad(String charStr, String targetOperand);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | charStr | any string. 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | targetOperand | string targetOperand. 

#### Returns

[Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16)

returns the value of the move.


<br>
<br>

### MoveRightWithPad([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16))

RPG's MOVE. Moves right a numeric string into an int2 (short) with pad.

```cs
MoveRightWithPad(String charStr, Int16 targetOperand);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | charStr | Source numeric string. 
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | targetOperand | Short value of the target. 

#### Returns

[Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16)

returns the value of the move.


<br>
<br>

### MoveRightWithPad([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

RPG's MOVE. Moves right a numeric string into an int4 (int) with pad.

```cs
MoveRightWithPad(String charStr, Int32 targetOperand);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | charStr | Source numeric string. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetOperand | Int value of the target. 

#### Returns

[Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16)

returns the value of the move.


<br>
<br>

### MoveRightWithPad([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64))

RPG's MOVE. Moves right a numeric string into an int8 (long) with pad.

```cs
MoveRightWithPad(String charStr, Int64 targetOperand);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | charStr | Source numeric string. 
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | targetOperand | Long value of the target. 

#### Returns

[Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16)

returns the value of the move.


<br>
<br>

### MoveToArray([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Array]($$TODO-Array.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

Moves a source string into an array.

```cs
MoveToArray(String source, Array target, Int32 startPosition);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | source | Source string. 
| [Array]($$TODO-Array.html) | target | Destination array. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | startPosition | The array element where the copy starts. 


<br>
<br>

### MoveToArray\`\`2([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [IFixedArrayBase{\\`\\`0,\\`\\`1}](/reference/asna-qsys-runtime/i-fixed-array-base{``0,``1}.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

Moves a source string into an array.

```cs
MoveToArray``2(String source, ASNA.QSys.Runtime.IFixedArrayBase{``0,``1} target, Int32 startPosition);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | source | Source string. 
| [IFixedArrayBase{\\`\\`0,\\`\\`1}](/reference/asna-qsys-runtime/i-fixed-array-base{``0,``1}.html) | target | Destination array. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | startPosition | The array element where the copy starts. 


<br>
<br>

### MoveToArrayWithPad([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Array]($$TODO-Array.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

Moves a source string into an array.

```cs
MoveToArrayWithPad(String source, Array target, Int32 startPosition);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | source | Source string. 
| [Array]($$TODO-Array.html) | target | Destination array. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | startPosition | The array element where the copy starts. 


<br>
<br>

### MoveToArrayWithPad\`\`2([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [IFixedArrayBase{\\`\\`0,\\`\\`1}](/reference/asna-qsys-runtime/i-fixed-array-base{``0,``1}.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

Moves a source string into an array.

```cs
MoveToArrayWithPad``2(String source, ASNA.QSys.Runtime.IFixedArrayBase{``0,``1} target, Int32 startPosition);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | source | Source string. 
| [IFixedArrayBase{\\`\\`0,\\`\\`1}](/reference/asna-qsys-runtime/i-fixed-array-base{``0,``1}.html) | target | Destination array. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | startPosition | The array element where the copy starts. 


<br>
<br>

### Replace([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

RPG's %SUBST. Replaces characters in a string based on position and length.

```cs
Replace(String target, String from, Int32 startPos, Int32 length, Boolean isRightAdg);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | target | The string where replacements will occur. 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | from | The replace string. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | startPos | Starting position in target. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | length | Length of replacement. 
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | isRightAdg | true for right adjust, false for left adjust (default). 

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

.


<br>
<br>

### Replace([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

RPG's %SUBST. Replaces characters in a string based on position and length.

```cs
Replace(String target, String from, Int32 startPos, Boolean isRightAdg);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | target | The string where replacements will occur. 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | from | The replace string. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | startPos | Starting position in target. 
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | isRightAdg | true for right adjust, false for left adjust (default). 

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

.


<br>
<br>

### Replace([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

Replace summary.

```cs
Replace(String baseString, String repString, Int32 startPos, Int32 lengthToReplace);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | baseString | Replace baseString param. 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | repString | Replace repString param. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | startPos | Replace startPos param. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | lengthToReplace | Replace lengthToReplace param. 

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

Replace returns.


<br>
<br>

### ReplaceFixed([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

ReplaceFixed summary.

```cs
ReplaceFixed(String baseString, Int32 baseLenConst, String repString, Int32 startPos, Int32 lengthToReplace);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | baseString | ReplaceFixed baseString param. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | baseLenConst | ReplaceFixed baseLenConst param. 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | repString | ReplaceFixed repString param. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | startPos | ReplaceFixed startPos param. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | lengthToReplace | ReplaceFixed lengthToReplace param. 

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

ReplaceFixed returns.


<br>
<br>

### ScanString([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

RPG's %SCAN. Returns the first position of the search argument in the source string, or 0 if it was not found.

```cs
ScanString(String baseString, String CmpStr, Int32 startPos);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | baseString | A character expression that contains the string that scan will search. 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | CmpStr | A character expression scan will use to search the baseString. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | startPos | The 1 based start position in baseString. 

#### Returns

[Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)

Returns the 1 based starting position of a match relative to the baseString.


<br>
<br>

### ScanString([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

RPG's %SCAN. Returns the first position of the search argument in the source string, or 0 if it was not found.

```cs
ScanString(String baseString, String CmpStr);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | baseString | A character expression that contains the string that scan will search. 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | CmpStr | A character expression scan will use to search the baseString. 

#### Returns

[Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)

Returns the 1 based starting position of a match relative to the baseString.


<br>
<br>

### ScanString([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

RPG's SCAN. Attempts to find cmpStr in the baseString.

```cs
ScanString(String baseString, String cmpStr, Int32 cmpLen, Int32 startPos);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | baseString | A character expression that contains the string to compare with cmpStr. 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | cmpStr | A character expression that baseString is scanned for. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | cmpLen | Default value is the length of cmpStr. Specifies the length of cmpStr that is scanned for in baseString. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | startPos | The 1 based start position in baseString. 

#### Returns

[Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)

Returns true if cmpStr is found in baseString.


<br>
<br>

### ScanString([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Indicator](/reference/asna-qsys-runtime/classes/indicator.html))

RPG's SCAN. Attempts to find cmpStr in the baseString.

```cs
ScanString(String baseString, String cmpStr, Int32 cmpLen, Int32 startPos, ref ASNA.QSys.Runtime.Indicator err);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | baseString | A character expression that contains the string to compare with cmpStr. 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | cmpStr | A character expression that baseString is scanned for. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | cmpLen | Default value is the length of cmpStr. Specifies the length of cmpStr that is scanned for in baseString. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | startPos | The 1 based start position in baseString. 
| [Indicator](/reference/asna-qsys-runtime/classes/indicator.html) | err | Indicator will be set if a runtime error occurs. 

#### Returns

[Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)

Returns true if cmpStr is found in baseString.


<br>
<br>

### ScanString([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Array]($$TODO-Array.html))

RPG's SCAN. Attempts to find cmpStr in the baseString.

```cs
ScanString(String baseString, String cmpStr, Int32 cmpLen, Int32 startPos, Array fndPosArray);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | baseString | A character expression that contains the string to compare with cmpStr. 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | cmpStr | A character expression that baseString is scanned for. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | cmpLen | Default value is the length of cmpStr. Specifies the length of cmpStr that is scanned for in baseString. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | startPos | The 1 based start position in baseString. 
| [Array]($$TODO-Array.html) | fndPosArray | . 

#### Returns

[Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)

Returns true if cmpStr is found in baseString.


<br>
<br>

### ScanString([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Array]($$TODO-Array.html), [Indicator](/reference/asna-qsys-runtime/classes/indicator.html))

RPG's SCAN. Attempts to find cmpStr in the baseString.

```cs
ScanString(String baseString, String cmpStr, Int32 cmpLen, Int32 startPos, Array fndPosArray, ref ASNA.QSys.Runtime.Indicator err);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | baseString | A character expression that contains the string to compare with cmpStr. 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | cmpStr | A character expression that baseString is scanned for. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | cmpLen | Default value is the length of cmpStr. Specifies the length of cmpStr that is scanned for in baseString. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | startPos | The 1 based start position in baseString. 
| [Array]($$TODO-Array.html) | fndPosArray | . 
| [Indicator](/reference/asna-qsys-runtime/classes/indicator.html) | err | Indicator will be set if a runtime error occurs. 

#### Returns

[Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)

Returns true if cmpStr is found in baseString.


<br>
<br>

### ScanString\`\`1([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [\\`\\`0]($$TODO-``0@.html))

RPG's SCAN. Attempts to find cmpStr in the baseString.

```cs
ScanString``1(String baseString, String cmpStr, Int32 cmpLen, Int32 startPos, ref ``0 fndPos);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | baseString | A character expression that contains the string to compare with cmpStr. 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | cmpStr | A character expression that baseString is scanned for. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | cmpLen | Default value is the length of cmpStr. Specifies the length of cmpStr that is scanned for in baseString. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | startPos | The 1 based start position in baseString. 
| [\\`\\`0]($$TODO-``0@.html) | fndPos | Will be 0 if scan cannot find cmpStr in baseString. Otherwise will be the 1 based array index position of the beginning of the first match from the left. 


<br>
<br>

### ScanString\`\`1([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [\\`\\`0]($$TODO-``0@.html), [Indicator](/reference/asna-qsys-runtime/classes/indicator.html))

RPG's SCAN. Attempts to find cmpStr in the baseString.

```cs
ScanString``1(String baseString, String cmpStr, Int32 cmpLen, Int32 startPos, ref ``0 fndPos, ref ASNA.QSys.Runtime.Indicator err);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | baseString | A character expression that contains the string to compare with cmpStr. 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | cmpStr | A character expression that baseString is scanned for. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | cmpLen | Default value is the length of cmpStr. Specifies the length of cmpStr that is scanned for in baseString. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | startPos | The 1 based start position in baseString. 
| [\\`\\`0]($$TODO-``0@.html) | fndPos | Will be 0 if scan cannot find cmpStr in baseString. Otherwise will be the 1 based array index position of the beginning of the first match from the left. 
| [Indicator](/reference/asna-qsys-runtime/classes/indicator.html) | err | Indicator will be set if a runtime error occurs. 


<br>
<br>

### SetHiLoEq([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Indicator](/reference/asna-qsys-runtime/classes/indicator.html), [Indicator](/reference/asna-qsys-runtime/classes/indicator.html), [Indicator](/reference/asna-qsys-runtime/classes/indicator.html))

Sets the flags according to the value of testString.

```cs
SetHiLoEq(String testString, ref ASNA.QSys.Runtime.Indicator hi, ref ASNA.QSys.Runtime.Indicator lo, ref ASNA.QSys.Runtime.Indicator eq);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | testString | The string to test. 
| [Indicator](/reference/asna-qsys-runtime/classes/indicator.html) | hi | Will be set to '0'. 
| [Indicator](/reference/asna-qsys-runtime/classes/indicator.html) | lo | Will be set to '0'. 
| [Indicator](/reference/asna-qsys-runtime/classes/indicator.html) | eq | Will be '1' if testString is all blanks, otherwise '0'. 

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

The test value.


<br>
<br>

### SetVaryingLength([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

Sets the variable length string to the indicated length, ensuring that it is no longer than limit.

```cs
SetVaryingLength(String charStr, Int32 length, Int32 limit);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | charStr | A variable length string. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | length | The desired length. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | limit | The maximum allowed length. 

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

.


<br>
<br>

### SubStr([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

RPG's SUBST. Returns a substring from baseString, starting at startPos ending at subLen, puts it into target, no padding, no preservation of length.

```cs
SubStr(String baseString, Int32 startPos, Int32 subLen);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | baseString | A character expression that contains the string SubStr will operate on. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | startPos | The 1 based start position for baseString. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | subLen | The length of the substring. 

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

The string value of the result of the SubStr.


<br>
<br>

### SubStr([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Indicator](/reference/asna-qsys-runtime/classes/indicator.html))

RPG's SUBST. Returns a substring from baseString, starting at startPos ending at subLen, puts it into target, no padding, no preservation of length.

```cs
SubStr(String baseString, Int32 startPos, Int32 subLen, ref ASNA.QSys.Runtime.Indicator errInd);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | baseString | A character expression that contains the string SubStr will operate on. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | startPos | The 1 based start position for baseString. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | subLen | The length of the substring. 
| [Indicator](/reference/asna-qsys-runtime/classes/indicator.html) | errInd | Indicator will be set if a runtime error occurs. 

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

.


<br>
<br>

### SubStrFixed([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

RPG's SUBST. Returns a substring from baseString, starting at startPos ending at subLen, puts it into target. This function preserves the length of the target, no padding.

```cs
SubStrFixed(String baseString, Int32 startPos, Int32 subLen, String target);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | baseString | A character expression that contains the string SubStr will operate on. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | startPos | The 1 based start position for baseString. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | subLen | The length of the substring. 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | target | Target Operand of the substring. 

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

The string value of the result of the SubStr.


<br>
<br>

### SubStrFixed([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Indicator](/reference/asna-qsys-runtime/classes/indicator.html))

RPG's SUBST. Returns a substring from baseString, starting at startPos ending at subLen, puts it into target. This function preserves the length of the target, no padding.

```cs
SubStrFixed(String baseString, Int32 startPos, Int32 subLen, String target, ref ASNA.QSys.Runtime.Indicator errInd);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | baseString | A character expression that contains the string SubStr will operate on. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | startPos | The 1 based start position for baseString. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | subLen | The length of the substring. 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | target | Target Operand of the substring. 
| [Indicator](/reference/asna-qsys-runtime/classes/indicator.html) | errInd | Indicator will be set if a runtime error occurs. 

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

The string value of the result of the SubStr.


<br>
<br>

### SubStrFixedWithPad([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

RPG's SUBST. Returns a substring from baseString, starting at startPos ending at subLen, puts it into target. This function preserves the length of the target, and pads the result.

```cs
SubStrFixedWithPad(String baseString, Int32 startPos, Int32 subLen, String target);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | baseString | A character expression that contains the string SubStr will operate on. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | startPos | The 1 based start position for baseString. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | subLen | The length of the substring. 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | target | Target Operand of the substring. 

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

The string value of the result of the SubStr.


<br>
<br>

### SubStrFixedWithPad([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Indicator](/reference/asna-qsys-runtime/classes/indicator.html))

RPG's SUBST. Returns a substring from baseString, starting at startPos ending at subLen, puts it into target. This function preserves the length of the target, and pads the result.

```cs
SubStrFixedWithPad(String baseString, Int32 startPos, Int32 subLen, String target, ref ASNA.QSys.Runtime.Indicator errInd);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | baseString | A character expression that contains the string SubStr will operate on. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | startPos | The 1 based start position for baseString. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | subLen | The length of the substring. 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | target | Target Operand of the substring. 
| [Indicator](/reference/asna-qsys-runtime/classes/indicator.html) | errInd | Indicator will be set if a runtime error occurs. 

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

The string value of the result of the SubStr.


<br>
<br>

### ToDateTime([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [DateTimeDataKind](/reference/asna-qsys-runtime/date-time-data-kind.html), [DateTimeFormat]($$TODO-ASNA.DataGate.Common.DateTimeFormat.html), [DateTimeSeparator](/reference/asna-qsys-runtime/classes/date-time-separator.html))

Converts a string representation of a date/time/timestamp into a DateTime.

```cs
ToDateTime(String charStr, ASNA.QSys.Runtime.DateTimeDataKind dateTimeKind, ASNA.DataGate.Common.DateTimeFormat dateTimeFormat, ASNA.QSys.Runtime.DateTimeSeparator dateTimeSeparator);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | charStr | string representing a date/time/timestamp. 
| [DateTimeDataKind](/reference/asna-qsys-runtime/date-time-data-kind.html) | dateTimeKind | Date, Time, Timestamp. 
| [DateTimeFormat]($$TODO-ASNA.DataGate.Common.DateTimeFormat.html) | dateTimeFormat | DateTime format. 
| [DateTimeSeparator](/reference/asna-qsys-runtime/classes/date-time-separator.html) | dateTimeSeparator | string separator. 

#### Returns

[DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime)

.


<br>
<br>

### ToDouble([String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Converts a numeric string into a double number.

```cs
ToDouble(String charStr);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | charStr | string representing a double number. 

#### Returns

[Double]($$TODO-Double.html)

double representation of given string.


<br>
<br>

### ToFixedDecimal([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

Converts a numeric string into a RPG decimal.

```cs
ToFixedDecimal(String charStr, Int32 digits, Int32 decimals);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | charStr | string representing a decimal number. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | digits | number of digits in the targetOperand. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | decimals | number of decimals in the targetOperand. 

#### Returns

[Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal)

decimal representation of given string.


<br>
<br>

### ToFixedDecimalRounded([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

Converts a numeric string into a RPG decimal with rounding (half adjust).

```cs
ToFixedDecimalRounded(String charStr, Int32 digits, Int32 decimals);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | charStr | string representing a decimal number. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | digits | number of digits in the targetOperand. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | decimals | number of decimals in the targetOperand. 

#### Returns

[Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal)

decimal representation of given string.


<br>
<br>

### ToFloat([String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Converts a numeric string into a float number.

```cs
ToFloat(String charStr);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | charStr | string representing a float number. 

#### Returns

[Single]($$TODO-Single.html)

float representation of given string.


<br>
<br>

### ToInt16([String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Converts a numeric string into a short number.

```cs
ToInt16(String charStr);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | charStr | string representing a short number. 

#### Returns

[Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16)

short representation of given string.


<br>
<br>

### ToInt32([String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Converts a numeric string into an int number.

```cs
ToInt32(String charStr);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | charStr | string representing an int number. 

#### Returns

[Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)

int representation of given string.


<br>
<br>

### ToInt64([String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Converts a numeric string into a long number.

```cs
ToInt64(String charStr);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | charStr | string representing a long number. 

#### Returns

[Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64)

long representation of given string.


<br>
<br>

### ToPackedDecimal([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

Converts a string representing a packed number into a RPG decimal.

```cs
ToPackedDecimal(String charStr, Int32 decimals);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | charStr | string representing a packed decimal number. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | decimals | number of decimal positions in the targetOperand. 

#### Returns

[Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal)

decimal packed representation of given string.


<br>
<br>

### ToZonedDecimal([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

Converts a zoned representation string into a RPG decimal.

```cs
ToZonedDecimal(String charStr, Int32 digits, Int32 decimals);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | charStr | string representing a zoned decimal number. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | digits | number of digits in the targetOperand. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | decimals | number of decimals in the targetOperand. 

#### Returns

[Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal)

decimal representation of given string.


<br>
<br>

### Xlate([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

RPG's %Xlate. Translates baseString according to the values of mapFrom, mapTo, and startPos.

```cs
Xlate(String baseString, String mapFrom, String mapTo, Int32 startPos);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | baseString | The string to be translated. 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | mapFrom | A string containing a list of characters that should be replaced. 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | mapTo | A string containing a list of characters with replacement values. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | startPos | The 1-based position in the baseString where replacement starts. Defaults to 1. 

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

The string resulting after the Xlate operation.


<br>
<br>

### Xlate([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Indicator](/reference/asna-qsys-runtime/classes/indicator.html))

RPG's %Xlate. Translates baseString according to the values of mapFrom, mapTo, and startPos. The parameter errInd will indicate if there was an error in the operation.

```cs
Xlate(String baseString, String mapFrom, String mapTo, Int32 startPos, ref ASNA.QSys.Runtime.Indicator errInd);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | baseString | The string to be translated. 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | mapFrom | A string containing a list of characters that should be replaced. 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | mapTo | A string containing a list of characters with replacement values. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | startPos | The 1-based position in the baseString where replacement starts. 
| [Indicator](/reference/asna-qsys-runtime/classes/indicator.html) | errInd | Indicator will be set if a runtime error occurs. 

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

The string resulting after the Xlate operation.


<br>
<br>

### Xlate([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

RPG's XLATE. Translates characters in the baseString according to MapFrom, MapTo, startPos and targetString, no padding, no preservation of length.

```cs
Xlate(String baseString, String mapFrom, String mapTo, String targetString, Int32 startPos);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | baseString | A character expression that contains the string Xlate will operate on. 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | mapFrom | From string, if characters are duplicated the first occurrence is used. 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | mapTo | To string, describes what the characters in mapFrom will become. 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | targetString | Target opperand of the Xlate operation. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | startPos | The 1 based start position for baseString. 

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

The string value of the result of the Xlate.


<br>
<br>

### Xlate([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Indicator](/reference/asna-qsys-runtime/classes/indicator.html))

RPG's XLATE. Translates characters in the baseString according to MapFrom, MapTo, startPos and targetString, no padding, no preservation of length.

```cs
Xlate(String baseString, String mapFrom, String mapTo, String targetString, Int32 startPos, ref ASNA.QSys.Runtime.Indicator errInd);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | baseString | A character expression that contains the string Xlate will operate on. 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | mapFrom | From string, if characters are duplicated the first occurrence is used. 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | mapTo | To string, describes what the characters in mapFrom will become. 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | targetString | Target opperand of the Xlate operation. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | startPos | The 1 based start position for baseString. 
| [Indicator](/reference/asna-qsys-runtime/classes/indicator.html) | errInd | Indicator will be set if a runtime error occurs. 

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

The string value of the result of the Xlate.


<br>
<br>

### XlateFixed([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

RPG's XLATE. Translates characters in the baseString according to MapFrom, MapTo, startPos and targetString. This version preserves the length of the result, does NOT pad.

```cs
XlateFixed(String baseString, String mapFrom, String mapTo, String targetString, Int32 startPos);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | baseString | A character expression that contains the string Xlate will operate on. 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | mapFrom | From string, if characters are duplicated the first occurrence is used. 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | mapTo | To string, describes what the characters in mapFrom will become. 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | targetString | Target opperand of the Xlate operation. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | startPos | The 1 based start position for baseString. 

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

The string value of the result of the Xlate.


<br>
<br>

### XlateFixed([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Indicator](/reference/asna-qsys-runtime/classes/indicator.html))

RPG's XLATE. Translates characters in the baseString according to MapFrom, MapTo, startPos and targetString. This version preserves the length of the result, does NOT pad.

```cs
XlateFixed(String baseString, String mapFrom, String mapTo, String targetString, Int32 startPos, ref ASNA.QSys.Runtime.Indicator errInd);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | baseString | A character expression that contains the string Xlate will operate on. 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | mapFrom | From string, if characters are duplicated the first occurrence is used. 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | mapTo | To string, describes what the characters in mapFrom will become. 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | targetString | Target opperand of the Xlate operation. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | startPos | The 1 based start position for baseString. 
| [Indicator](/reference/asna-qsys-runtime/classes/indicator.html) | errInd | Indicator will be set if a runtime error occurs. 

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

The string value of the result of the Xlate.


<br>
<br>

### XlateFixedWithPad([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

RPG's XLATE. Translates characters in the baseString according to MapFrom, MapTo, startPos and targetString. This version preserves the length of the result, with padding.

```cs
XlateFixedWithPad(String baseString, String mapFrom, String mapTo, String targetString, Int32 startPos);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | baseString | A character expression that contains the string Xlate will operate on. 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | mapFrom | From string, if characters are duplicated the first occurrence is used. 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | mapTo | To string, describes what the characters in mapFrom will become. 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | targetString | Target opperand of the Xlate operation. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | startPos | The 1 based start position for baseString. 

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

The string value of the result of the Xlate.


<br>
<br>

### XlateFixedWithPad([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Indicator](/reference/asna-qsys-runtime/classes/indicator.html))

RPG's XLATE. Translates characters in the baseString according to MapFrom, MapTo, startPos and targetString. This version preserves the length of the result, with padding.

```cs
XlateFixedWithPad(String baseString, String mapFrom, String mapTo, String targetString, Int32 startPos, ref ASNA.QSys.Runtime.Indicator errInd);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | baseString | A character expression that contains the string Xlate will operate on. 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | mapFrom | From string, if characters are duplicated the first occurrence is used. 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | mapTo | To string, describes what the characters in mapFrom will become. 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | targetString | Target opperand of the Xlate operation. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | startPos | The 1 based start position for baseString. 
| [Indicator](/reference/asna-qsys-runtime/classes/indicator.html) | errInd | Indicator will be set if a runtime error occurs. 

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

The string value of the result of the Xlate.


<br>
<br>

