---
title: "StringMethods class           | QSYS API Reference Guide"
description: "Contains extension methods for handling RPG operations and conversions for string values. "
last_modified_at: 2024-08-09T17:25:29Z
---

Contains extension methods for handling RPG operations and conversions for string values.

**Namespace:** ASNA.QSys.Runtime
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>

## Methods

| Signature | Description |
| --- | --- |
| [AdjustEnd](#string-adjustendstring-charstr-int-length)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Adjust the length of a string to a given value, by padding or truncating the string on the right.
| [AdjustStart](#string-adjuststartstring-charstr-int-length)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Adjust the length of a string to a given value, by padding or truncating the string on the left.
| [AdjustVaryingLength](#string-adjustvaryinglengthstring-charstr-int-limit)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Trims the end of a variable length string if needed so the string is at most as long as limit.
| [BitOff](#byte-bitoffbyte-target-string-mask)([Byte](https://docs.microsoft.com/en-us/dotnet/api/system.byte), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | RPG's BITOFF.
| [BitOn](#byte-bitonbyte-target-string-mask)([Byte](https://docs.microsoft.com/en-us/dotnet/api/system.byte), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | RPG's BITON.
| [CheckCharacters](#bool-checkcharactersstring-basestring-string-comparator-int-startpos)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's CHECK. Verifies that each character in a base string or array is among the characters in the comparator string.
| [CheckCharacters](#bool-checkcharactersstring-basestring-string-comparator-int-startpos-array-nomatcharray)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Array](https://learn.microsoft.com/en-us/dotnet/api/system.array?view=net-8.0)) | RPG's CHECK. Verifies that each character in a base string or array is among the characters in the comparator string.
| [CheckCharactersReverse](#bool-checkcharactersreversestring-basestring-string-comparator-int-startpos)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's CHECKR. Verifies that each character in a base string or array is among the characters in the comparator string.
| [CheckCharactersReverse](#bool-checkcharactersreversestring-basestring-string-comparator-int-startpos-array-nomatcharray)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Array](https://learn.microsoft.com/en-us/dotnet/api/system.array?view=net-8.0)) | RPG's CHECKR. Verifies that each character in a base string or array is among the characters in the comparator string.
| [CheckPosition](#int-checkpositionstring-basestring-string-comparator)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | RPG's %CHECK. Verifies that each character in the baseString is among the characters in the comparator.
| [CheckPosition](#int-checkpositionstring-basestring-string-comparator-int-startpos)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's %CHECK. Verifies that each character in the baseString is among the characters in the comparator.
| [CheckPositionReverse](#int-checkpositionreversestring-basestring-string-comparator-int-startpos)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's %CHECK. Verifies that each character in the baseString is among the characters in the comparator, starting from the right most position.
| [CheckPositionReverse](#int-checkpositionreversestring-basestring-string-comparator)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | RPG's %CHECK. Verifies that each character in the baseString is among the characters in the comparator, starting from the right most position.
| [FromStringBinary](#decimal-fromstringbinarystring-num-int-digits-int-decimals)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Returns a (binary) decimal number based on its 'memory' representation.
| [FromStringByte](#byte-fromstringbytestring-num)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Returns a byte based on its 'memory' representation.
| [FromStringInteger](#int-fromstringintegerstring-num)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Returns an integer number based on its 'memory' representation.
| [FromStringLong](#long-fromstringlongstring-num)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Returns a long number based on its 'memory' representation.
| [FromStringPacked](#decimal-fromstringpackedstring-num-int-decimals)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Returns a (packed) decimal number based on its 'memory' representation.
| [FromStringShort](#short-fromstringshortstring-num)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Returns a short number based on its 'memory' representation.
| [FromStringZoned](#decimal-fromstringzonedstring-num-int-digits-int-decimals)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Returns a (zoned) decimal number based on its 'memory' representation.
| [IsBlanks](#bool-isblanksstring-arg)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Test a string to see if it is spaces.
| [MoveLeft](#decimal-moveleftstring-charstr-decimal-targetoperand-int-targetoperanddig-int-targetoperanddec)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's MOVEL. Moves left a numeric string to decimal, without pad.
| [MoveLeft](#string-moveleftstring-charstr-string-targetoperand)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | RPG's MOVEL. Moves left a string to string, with or without pad.
| [MoveLeft](#datetime-moveleftstring-charstr-datetime-datetime-datetimedatakind-datetimekind-datetimeformat-datetimeformat-datetimeseparator-datetimeseparator)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind](/reference/runtime/qsys-runtime/date-time-data-kind.html), [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html), [DateTimeSeparator](/reference/runtime/qsys-runtime/date-time-separator.html)) | RPG's MOVEL. Moves left a string expressed in the given format into a date time type.
| [MoveLeft](#short-moveleftstring-charstr-short-targetoperand)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16)) | RPG's MOVEL. Moves left a numeric string into an int2 (short).
| [MoveLeft](#int-moveleftstring-charstr-int-targetoperand)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's MOVEL. Moves left a numeric string into an int4 (int).
| [MoveLeft](#long-moveleftstring-charstr-long-targetoperand)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64)) | RPG's MOVEL. Moves left a numeric string into an int8 (long).
| [MoveLeftToChar](#char-movelefttocharstring-charstr)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | RPG's MOVE. Moves left a string into a character.
| [MoveLeftWithPad](#decimal-moveleftwithpadstring-charstr-decimal-targetoperand-int-targetoperanddig-int-targetoperanddec)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's MOVEL. Moves left a numeric string to decimal, with pad.
| [MoveLeftWithPad](#string-moveleftwithpadstring-charstr-string-targetoperand)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | RPG's MOVEL. Moves left a string to string, with pad.
| [MoveLeftWithPad](#short-moveleftwithpadstring-charstr-short-targetoperand)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16)) | RPG's MOVEL. Moves left a numeric string into an int2 (short) with pad.
| [MoveLeftWithPad](#int-moveleftwithpadstring-charstr-int-targetoperand)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's MOVEL. Moves left a numeric string into an int4 (int) with pad.
| [MoveLeftWithPad](#long-moveleftwithpadstring-charstr-long-targetoperand)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64)) | RPG's MOVEL. Moves right a numeric string into an int8 (long) with pad.
| [MoveRight](#decimal-moverightstring-charstr-decimal-targetoperand-int-targetoperanddig-int-targetoperanddec)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's MOVE. Moves right a numeric string to decimal, without pad.
| [MoveRight](#string-moverightstring-charstr-string-targetoperand)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | RPG's MOVE. Moves right a string to string, without pad.
| [MoveRight](#datetime-moverightstring-charstr-datetime-datetime-datetimedatakind-datetimekind-datetimeformat-datetimeformat-datetimeseparator-datetimeseparator)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind](/reference/runtime/qsys-runtime/date-time-data-kind.html), [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html), [DateTimeSeparator](/reference/runtime/qsys-runtime/date-time-separator.html)) | RPG's MOVE. Moves right a string expressed in the given format into a date time type.
| [MoveRight](#short-moverightstring-charstr-short-targetoperand)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16)) | RPG's MOVE. Moves right a numeric string into an int2 (short).
| [MoveRight](#int-moverightstring-charstr-int-targetoperand)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's MOVE. Moves right a numeric string into an int4 (int).
| [MoveRight](#long-moverightstring-charstr-long-targetoperand)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64)) | RPG's MOVE. Moves right a numeric string into an int8 (long).
| [MoveRightToChar](#char-moverighttocharstring-charstr)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | RPG's MOVE. Moves right a string into a character.
| [MoveRightWithPad](#decimal-moverightwithpadstring-charstr-decimal-targetoperand-int-targetoperanddig-int-targetoperanddec)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's MOVE. Moves right a numeric string to decimal, with pad.
| [MoveRightWithPad](#string-moverightwithpadstring-charstr-string-targetoperand)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | RPG's MOVE. Moves right a string to string, with pad.
| [MoveRightWithPad](#short-moverightwithpadstring-charstr-short-targetoperand)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16)) | RPG's MOVE. Moves right a numeric string into an int2 (short) with pad.
| [MoveRightWithPad](#int-moverightwithpadstring-charstr-int-targetoperand)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's MOVE. Moves right a numeric string into an int4 (int) with pad.
| [MoveRightWithPad](#long-moverightwithpadstring-charstr-long-targetoperand)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64)) | RPG's MOVE. Moves right a numeric string into an int8 (long) with pad.
| [MoveToArray](#void-movetoarraystring-source-array-target-int-startposition)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Array](https://learn.microsoft.com/en-us/dotnet/api/system.array?view=net-8.0), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Moves a source string into an array.
| [MoveToArrayWithPad](#void-movetoarraywithpadstring-source-array-target-int-startposition)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Array](https://learn.microsoft.com/en-us/dotnet/api/system.array?view=net-8.0), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Moves a source string into an array.
| [Replace](#string-replacestring-target-string-from-int-startpos-int-length-bool-isrightadg)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | RPG's %SUBST. Replaces characters in a string based on position and length.
| [Replace](#string-replacestring-target-string-from-int-startpos-bool-isrightadg)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | RPG's %SUBST. Replaces characters in a string based on position and length.
| [Replace](#string-replacestring-target-string-from-int-startpos-int-length)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's %SUBST. Replaces characters in a string based on position and length.
| [ReplaceFixed](#string-replacefixedstring-target-int-baselength-string-from-int-startpos-int-length)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's %SUBST. Replaces characters in a string based on position and length.
| [ScanString](#int-scanstringstring-basestring-string-cmpstr-int-startpos)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's %SCAN. Returns the first position of the search argument in the source string, or 0 if it was not found.
| [ScanString](#int-scanstringstring-basestring-string-cmpstr)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | RPG's %SCAN. Returns the first position of the search argument in the source string, or 0 if it was not found.
| [ScanString](#bool-scanstringstring-basestring-string-cmpstr-int-cmplen-int-startpos)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's SCAN. Attempts to find cmpStr in the baseString.
| [ScanString](#bool-scanstringstring-basestring-string-cmpstr-int-cmplen-int-startpos-array-fndposarray)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Array](https://learn.microsoft.com/en-us/dotnet/api/system.array?view=net-8.0)) | RPG's SCAN. Attempts to find cmpStr in the baseString.
| [SetHiLoEq](#string-sethiloeqstring-teststring-indicator-hi-indicator-lo-indicator-eq)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Indicator&](/reference/runtime/qsys-runtime/indicator.html), [Indicator&](/reference/runtime/qsys-runtime/indicator.html), [Indicator&](/reference/runtime/qsys-runtime/indicator.html)) | Sets the flags according to the value of testString.
| [SetVaryingLength](#string-setvaryinglengthstring-charstr-int-length-int-limit)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Sets the variable length string to the indicated length, ensuring that it is no longer than limit.
| [SubStr](#string-substrstring-basestring-int-startpos-int-sublen)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's SUBST. Returns a substring from baseString, starting at startPos ending at subLen, puts it into target, no padding, no preservation of length.
| [SubStrFixed](#string-substrfixedstring-basestring-int-startpos-int-sublen-string-target)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | RPG's SUBST. Returns a substring from baseString, starting at startPos ending at subLen, puts it into target. This function preserves the length of the target, no padding.
| [SubStrFixedWithPad](#string-substrfixedwithpadstring-basestring-int-startpos-int-sublen-string-target)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | RPG's SUBST. Returns a substring from baseString, starting at startPos ending at subLen, puts it into target. This function preserves the length of the target, and pads the result.
| [ToByte](#byte-tobytestring-charstr)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Converts a numeric string into a byte number.
| [ToDateTime](#datetime-todatetimestring-charstr-datetimedatakind-datetimekind-datetimeformat-datetimeformat-datetimeseparator-datetimeseparator)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [DateTimeDataKind](/reference/runtime/qsys-runtime/date-time-data-kind.html), [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html), [DateTimeSeparator](/reference/runtime/qsys-runtime/date-time-separator.html)) | Converts a string representation of a date/time/timestamp into a DateTime.
| [ToDouble](#double-todoublestring-charstr)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Converts a numeric string into a double number.
| [ToFixedDecimal](#decimal-tofixeddecimalstring-charstr-int-digits-int-decimals)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Converts a numeric string into a RPG decimal.
| [ToFixedDecimalRounded](#decimal-tofixeddecimalroundedstring-charstr-int-digits-int-decimals)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Converts a numeric string into a RPG decimal with rounding (half adjust).
| [ToFloat](#float-tofloatstring-charstr)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Converts a numeric string into a float number.
| [ToInt16](#short-toint16string-charstr)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Converts a numeric string into a short number.
| [ToInt32](#int-toint32string-charstr)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Converts a numeric string into an int number.
| [ToInt64](#long-toint64string-charstr)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Converts a numeric string into a long number.
| [ToPackedDecimal](#decimal-topackeddecimalstring-charstr-int-decimals)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Converts a string representing a packed number into a RPG decimal.
| [ToZonedDecimal](#decimal-tozoneddecimalstring-charstr-int-digits-int-decimals)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Converts a zoned representation string into a RPG decimal.
| [Xlate](#string-xlatestring-basestring-string-mapfrom-string-mapto-int-startpos)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's %Xlate. Translates baseString according to the values of mapFrom, mapTo, and startPos.
| [Xlate](#string-xlatestring-basestring-string-mapfrom-string-mapto-string-targetstring-int-startpos)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's XLATE. Translates characters in the baseString according to MapFrom, MapTo, startPos and targetString, no padding, no preservation of length.
| [XlateFixed](#string-xlatefixedstring-basestring-string-mapfrom-string-mapto-string-targetstring-int-startpos)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's XLATE. Translates characters in the baseString according to MapFrom, MapTo, startPos and targetString. This version preserves the length of the result, does NOT pad.
| [XlateFixedWithPad](#string-xlatefixedwithpadstring-basestring-string-mapfrom-string-mapto-string-targetstring-int-startpos)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's XLATE. Translates characters in the baseString according to MapFrom, MapTo, startPos and targetString. This version preserves the length of the result, with padding.

### string AdjustEnd([string charStr](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [int length](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Adjust the length of a string to a given value, by padding or truncating the string on the right.

```cs
string AdjustEnd(string charStr, int length)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | charStr | The string to adjust.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | length | The desired length.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The string at the desired length.

### string AdjustStart([string charStr](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [int length](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Adjust the length of a string to a given value, by padding or truncating the string on the left.

```cs
string AdjustStart(string charStr, int length)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | charStr | The string to adjust.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | length | The desired length.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The string at the desired length.

### string AdjustVaryingLength([string charStr](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [int limit](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Trims the end of a variable length string if needed so the string is at most as long as limit.

```cs
string AdjustVaryingLength(string charStr, int limit)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | charStr | A variable length string.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | limit | Maximum length allowed for the string.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The string value with length at most equal to limit.

### byte BitOff([byte target](https://docs.microsoft.com/en-us/dotnet/api/system.byte), [string mask](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

RPG's BITOFF.

```cs
byte BitOff(byte target, string mask)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Byte](https://docs.microsoft.com/en-us/dotnet/api/system.byte) | target | A one-position character field.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | mask | Bit numbers 0-7. Enclose the bit numbers in apostrophes. For example, to set bits 0, 3, 6 on, enter '036'. A valid character expression.

#### Returns

| Type | Description
| --- | ---
| [Byte](https://docs.microsoft.com/en-us/dotnet/api/system.byte) | Returns the result of bitoff mask being applied to the target.

### byte BitOn([byte target](https://docs.microsoft.com/en-us/dotnet/api/system.byte), [string mask](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

RPG's BITON.

```cs
byte BitOn(byte target, string mask)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Byte](https://docs.microsoft.com/en-us/dotnet/api/system.byte) | target | A one-position character field.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | mask | Bit numbers 0-7. Enclose the bit numbers in apostrophes. For example, to set bits 0, 3, 6 on, enter '036'. A valid character expression.

#### Returns

| Type | Description
| --- | ---
| [Byte](https://docs.microsoft.com/en-us/dotnet/api/system.byte) | Returns the result of biton mask being applied to the target.

### bool CheckCharacters([string baseString](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string comparator](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [int startPos](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's CHECK. Verifies that each character in a base string or array is among the characters in the comparator string.

```cs
bool CheckCharacters(string baseString, string comparator, int startPos)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | baseString | A character expression that contains the string to compare with comparator.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | comparator | A character expression that is used to compare against the baseString.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | startPos | Specifies the 1-based starting position and continues to the right of the baseString.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | Returns true if a mismatch is found.

### bool CheckCharacters([string baseString](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string comparator](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [int startPos](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [Array noMatchArray](https://learn.microsoft.com/en-us/dotnet/api/system.array?view=net-8.0))

RPG's CHECK. Verifies that each character in a base string or array is among the characters in the comparator string.

```cs
bool CheckCharacters(string baseString, string comparator, int startPos, Array noMatchArray)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | baseString | A character expression that contains the string to compare with comparator.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | comparator | A character expression that is used to compare against the baseString.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | startPos | Specifies the 1-based starting position and continues to the right of the baseString.
| [Array](https://learn.microsoft.com/en-us/dotnet/api/system.array?view=net-8.0) | noMatchArray | Returns all of the 1-based positions of characters that don't match. The first element in the array contains the leftmost non-match.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | Returns true if a mismatch is found.

### bool CheckCharactersReverse([string baseString](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string comparator](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [int startPos](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's CHECKR. Verifies that each character in a base string or array is among the characters in the comparator string.

```cs
bool CheckCharactersReverse(string baseString, string comparator, int startPos)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | baseString | A character expression that contains the string to compare with comparator.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | comparator | A character expression that is used to compare against the baseString.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | startPos | Specifies the 1-based starting position and continues to the left of the baseString.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | Returns true if a mismatch is found.

### bool CheckCharactersReverse([string baseString](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string comparator](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [int startPos](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [Array noMatchArray](https://learn.microsoft.com/en-us/dotnet/api/system.array?view=net-8.0))

RPG's CHECKR. Verifies that each character in a base string or array is among the characters in the comparator string.

```cs
bool CheckCharactersReverse(string baseString, string comparator, int startPos, Array noMatchArray)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | baseString | A character expression that contains the string to compare with comparator.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | comparator | A character expression that is used to compare against the baseString.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | startPos | Specifies the 1-based starting position and continues to the left of the baseString.
| [Array](https://learn.microsoft.com/en-us/dotnet/api/system.array?view=net-8.0) | noMatchArray | Returns the 1-based position of the first non-matched character in baseString that is not in the comparator.            The first index in NoMatchArray is the rightmost mismatch in the baseString.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | Returns true if a mismatch is found.

### int CheckPosition([string baseString](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string comparator](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

RPG's %CHECK. Verifies that each character in the baseString is among the characters in the comparator.

```cs
int CheckPosition(string baseString, string comparator)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | baseString | A character expression that contains the string to compare with comparator.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | comparator | A character expression that is used to compare against the baseString.

#### Returns

| Type | Description
| --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | Returns the 1 based position of the first non-matched character in baseString that is not in the comparator.

### int CheckPosition([string baseString](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string comparator](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [int startPos](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's %CHECK. Verifies that each character in the baseString is among the characters in the comparator.

```cs
int CheckPosition(string baseString, string comparator, int startPos)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | baseString | A character expression that contains the string to compare with comparator.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | comparator | A character expression that is used to compare against the baseString.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | startPos | Default Position 1, not zero based.  Specifies the start position from the left most position.

#### Returns

| Type | Description
| --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | Returns the 1 based position of the first non-matched character in baseString that is not in the comparator.

### int CheckPositionReverse([string baseString](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string comparator](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [int startPos](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's %CHECK. Verifies that each character in the baseString is among the characters in the comparator, starting from the right most position.

```cs
int CheckPositionReverse(string baseString, string comparator, int startPos)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | baseString | A character expression that contains the string to compare with comparator.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | comparator | A character expression that is used to compare against the baseString.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | startPos | Default Position end of string, not zero based.  Specifies the start position from the left most position.

#### Returns

| Type | Description
| --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | Returns the 1 based position of the first non-matched character in baseString that is not in the comparator.

### int CheckPositionReverse([string baseString](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string comparator](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

RPG's %CHECK. Verifies that each character in the baseString is among the characters in the comparator, starting from the right most position.

```cs
int CheckPositionReverse(string baseString, string comparator)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | baseString | A character expression that contains the string to compare with comparator.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | comparator | A character expression that is used to compare against the baseString.

#### Returns

| Type | Description
| --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | Returns the 1 based position of the first non-matched character in baseString that is not in the comparator.

### decimal FromStringBinary([string num](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [int digits](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int decimals](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Returns a (binary) decimal number based on its 'memory' representation.

```cs
decimal FromStringBinary(string num, int digits, int decimals)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | num | The string representation of the number.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | digits | The number of digits in the decimal number.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | decimals | The number of decimal positions in the decimal number.

#### Returns

| Type | Description
| --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | The decimal number corresponding to the binary decimal representation.

### byte FromStringByte([string num](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Returns a byte based on its 'memory' representation.

```cs
byte FromStringByte(string num)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | num | The string representation of the number.

#### Returns

| Type | Description
| --- | ---
| [Byte](https://docs.microsoft.com/en-us/dotnet/api/system.byte) | The byte value corresponding to the first byte in the byte[] representation of the string.

### int FromStringInteger([string num](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Returns an integer number based on its 'memory' representation.

```cs
int FromStringInteger(string num)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | num | The string representation of the number.

#### Returns

| Type | Description
| --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | The int value corresponding to the first 4 bytes in the byte[] representation of the string.

### long FromStringLong([string num](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Returns a long number based on its 'memory' representation.

```cs
long FromStringLong(string num)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | num | The string representation of the number.

#### Returns

| Type | Description
| --- | ---
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | The long value corresponding to the first 8 bytes in the byte[] representation of the string.

### decimal FromStringPacked([string num](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [int decimals](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Returns a (packed) decimal number based on its 'memory' representation.

```cs
decimal FromStringPacked(string num, int decimals)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | num | The string representation of the number.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | decimals | The number of decimal positions in the decimal number.

#### Returns

| Type | Description
| --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | The decimal number corresponding to the packed decimal representation.

### short FromStringShort([string num](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Returns a short number based on its 'memory' representation.

```cs
short FromStringShort(string num)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | num | The string representation of the number.

#### Returns

| Type | Description
| --- | ---
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | The short value corresponding to the first 2 bytes in the byte[] representation of the string.

### decimal FromStringZoned([string num](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [int digits](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int decimals](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Returns a (zoned) decimal number based on its 'memory' representation.

```cs
decimal FromStringZoned(string num, int digits, int decimals)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | num | The string representation of the number.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | digits | The total number of digits the decimal has.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | decimals | The number of decimal positions in the decimal number.

#### Returns

| Type | Description
| --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | The decimal number corresponding to the zoned decimal representation.

### bool IsBlanks([string arg](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Test a string to see if it is spaces.

```cs
bool IsBlanks(string arg)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | arg | The string to test.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | True if the string characters are all blanks (space). False otherwise.

### decimal MoveLeft([string charStr](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [decimal targetOperand](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [int targetOperandDig](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int targetOperandDec](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVEL. Moves left a numeric string to decimal, without pad.

```cs
decimal MoveLeft(string charStr, decimal targetOperand, int targetOperandDig, int targetOperandDec)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | charStr | string representing a decimal number.
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | targetOperand | decimal number of the targetOperand number.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetOperandDig | number of digits in targetOperand.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetOperandDec | number of decimals in targetOperand.

#### Returns

| Type | Description
| --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | returns the value of the move.

### string MoveLeft([string charStr](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string targetOperand](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

RPG's MOVEL. Moves left a string to string, with or without pad.

```cs
string MoveLeft(string charStr, string targetOperand)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | charStr | any string.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | targetOperand | string targetOperand.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | returns the value of the move.

### DateTime MoveLeft([string charStr](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [DateTime dateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind dateTimeKind](/reference/runtime/qsys-runtime/date-time-data-kind.html), [DateTimeFormat dateTimeFormat](/reference/datagate/datagate-common/date-time-format.html), [DateTimeSeparator dateTimeSeparator](/reference/runtime/qsys-runtime/date-time-separator.html))

RPG's MOVEL. Moves left a string expressed in the given format into a date time type.

```cs
DateTime MoveLeft(string charStr, DateTime dateTime, DateTimeDataKind dateTimeKind, DateTimeFormat dateTimeFormat, DateTimeSeparator dateTimeSeparator)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | charStr | Source string.
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | dateTime | Destination DateTime.
| [DateTimeDataKind](/reference/runtime/qsys-runtime/date-time-data-kind.html) | dateTimeKind | Date, Time, Timestamp.
| [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html) | dateTimeFormat | DateTime format.
| [DateTimeSeparator](/reference/runtime/qsys-runtime/date-time-separator.html) | dateTimeSeparator | string separator.

#### Returns

| Type | Description
| --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | returns the value of the move.

### short MoveLeft([string charStr](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [short targetOperand](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVEL. Moves left a numeric string into an int2 (short).

```cs
short MoveLeft(string charStr, short targetOperand)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | charStr | Source numeric string.
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | targetOperand | Short value of the target.

#### Returns

| Type | Description
| --- | ---
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | returns the value of the move.

### int MoveLeft([string charStr](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [int targetOperand](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVEL. Moves left a numeric string into an int4 (int).

```cs
int MoveLeft(string charStr, int targetOperand)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | charStr | Source numeric string.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetOperand | Int value of the target.

#### Returns

| Type | Description
| --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | returns the value of the move.

### long MoveLeft([string charStr](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [long targetOperand](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVEL. Moves left a numeric string into an int8 (long).

```cs
long MoveLeft(string charStr, long targetOperand)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | charStr | Source numeric string.
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | targetOperand | Long value of the target.

#### Returns

| Type | Description
| --- | ---
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | returns the value of the move.

### char MoveLeftToChar([string charStr](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

RPG's MOVE. Moves left a string into a character.

```cs
char MoveLeftToChar(string charStr)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | charStr | A string the represents the source of the move.

#### Returns

| Type | Description
| --- | ---
| [Char](https://docs.microsoft.com/en-us/dotnet/api/system.char) | returns the value of the move.

### decimal MoveLeftWithPad([string charStr](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [decimal targetOperand](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [int targetOperandDig](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int targetOperandDec](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVEL. Moves left a numeric string to decimal, with pad.

```cs
decimal MoveLeftWithPad(string charStr, decimal targetOperand, int targetOperandDig, int targetOperandDec)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | charStr | string representing a decimal number.
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | targetOperand | decimal number of the targetOperand number.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetOperandDig | number of digits in targetOperand.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetOperandDec | number of decimals in targetOperand.

#### Returns

| Type | Description
| --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | returns the value of the move.

### string MoveLeftWithPad([string charStr](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string targetOperand](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

RPG's MOVEL. Moves left a string to string, with pad.

```cs
string MoveLeftWithPad(string charStr, string targetOperand)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | charStr | any string.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | targetOperand | string targetOperand.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | returns the value of the move.

### short MoveLeftWithPad([string charStr](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [short targetOperand](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVEL. Moves left a numeric string into an int2 (short) with pad.

```cs
short MoveLeftWithPad(string charStr, short targetOperand)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | charStr | Source numeric string.
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | targetOperand | Short value of the target.

#### Returns

| Type | Description
| --- | ---
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | returns the value of the move.

### int MoveLeftWithPad([string charStr](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [int targetOperand](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVEL. Moves left a numeric string into an int4 (int) with pad.

```cs
int MoveLeftWithPad(string charStr, int targetOperand)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | charStr | Source numeric string.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetOperand | Int value of the target.

#### Returns

| Type | Description
| --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | returns the value of the move.

### long MoveLeftWithPad([string charStr](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [long targetOperand](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVEL. Moves right a numeric string into an int8 (long) with pad.

```cs
long MoveLeftWithPad(string charStr, long targetOperand)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | charStr | Source numeric string.
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | targetOperand | Long value of the target.

#### Returns

| Type | Description
| --- | ---
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | returns the value of the move.

### decimal MoveRight([string charStr](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [decimal targetOperand](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [int targetOperandDig](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int targetOperandDec](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVE. Moves right a numeric string to decimal, without pad.

```cs
decimal MoveRight(string charStr, decimal targetOperand, int targetOperandDig, int targetOperandDec)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | charStr | string representing a decimal number.
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | targetOperand | decimal number of the targetOperand number.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetOperandDig | number of digits in targetOperand.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetOperandDec | number of decimals in targetOperand.

#### Returns

| Type | Description
| --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | returns the value of the move.

### string MoveRight([string charStr](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string targetOperand](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

RPG's MOVE. Moves right a string to string, without pad.

```cs
string MoveRight(string charStr, string targetOperand)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | charStr | any string.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | targetOperand | string targetOperand.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | returns the value of the move.

### DateTime MoveRight([string charStr](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [DateTime dateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTimeDataKind dateTimeKind](/reference/runtime/qsys-runtime/date-time-data-kind.html), [DateTimeFormat dateTimeFormat](/reference/datagate/datagate-common/date-time-format.html), [DateTimeSeparator dateTimeSeparator](/reference/runtime/qsys-runtime/date-time-separator.html))

RPG's MOVE. Moves right a string expressed in the given format into a date time type.

```cs
DateTime MoveRight(string charStr, DateTime dateTime, DateTimeDataKind dateTimeKind, DateTimeFormat dateTimeFormat, DateTimeSeparator dateTimeSeparator)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | charStr | Source string.
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | dateTime | Destination DateTime.
| [DateTimeDataKind](/reference/runtime/qsys-runtime/date-time-data-kind.html) | dateTimeKind | Date, Time, Timestamp.
| [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html) | dateTimeFormat | DateTime format.
| [DateTimeSeparator](/reference/runtime/qsys-runtime/date-time-separator.html) | dateTimeSeparator | string separator.

#### Returns

| Type | Description
| --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | returns the value of the move.

### short MoveRight([string charStr](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [short targetOperand](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVE. Moves right a numeric string into an int2 (short).

```cs
short MoveRight(string charStr, short targetOperand)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | charStr | Source numeric string.
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | targetOperand | Short value of the target.

#### Returns

| Type | Description
| --- | ---
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | returns the value of the move.

### int MoveRight([string charStr](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [int targetOperand](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVE. Moves right a numeric string into an int4 (int).

```cs
int MoveRight(string charStr, int targetOperand)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | charStr | Source numeric string.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetOperand | Int value of the target.

#### Returns

| Type | Description
| --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | returns the value of the move.

### long MoveRight([string charStr](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [long targetOperand](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVE. Moves right a numeric string into an int8 (long).

```cs
long MoveRight(string charStr, long targetOperand)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | charStr | Source numeric string.
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | targetOperand | Long value of the target.

#### Returns

| Type | Description
| --- | ---
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | returns the value of the move.

### char MoveRightToChar([string charStr](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

RPG's MOVE. Moves right a string into a character.

```cs
char MoveRightToChar(string charStr)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | charStr | A string the represents the source of the move.

#### Returns

| Type | Description
| --- | ---
| [Char](https://docs.microsoft.com/en-us/dotnet/api/system.char) | returns the value of the move.

### decimal MoveRightWithPad([string charStr](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [decimal targetOperand](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [int targetOperandDig](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int targetOperandDec](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVE. Moves right a numeric string to decimal, with pad.

```cs
decimal MoveRightWithPad(string charStr, decimal targetOperand, int targetOperandDig, int targetOperandDec)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | charStr | string representing a decimal number.
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | targetOperand | decimal number of the targetOperand number.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetOperandDig | number of digits in targetOperand.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetOperandDec | number of decimals in targetOperand.

#### Returns

| Type | Description
| --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | returns the value of the move.

### string MoveRightWithPad([string charStr](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string targetOperand](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

RPG's MOVE. Moves right a string to string, with pad.

```cs
string MoveRightWithPad(string charStr, string targetOperand)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | charStr | any string.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | targetOperand | string targetOperand.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | returns the value of the move.

### short MoveRightWithPad([string charStr](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [short targetOperand](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVE. Moves right a numeric string into an int2 (short) with pad.

```cs
short MoveRightWithPad(string charStr, short targetOperand)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | charStr | Source numeric string.
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | targetOperand | Short value of the target.

#### Returns

| Type | Description
| --- | ---
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | returns the value of the move.

### int MoveRightWithPad([string charStr](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [int targetOperand](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVE. Moves right a numeric string into an int4 (int) with pad.

```cs
int MoveRightWithPad(string charStr, int targetOperand)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | charStr | Source numeric string.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetOperand | Int value of the target.

#### Returns

| Type | Description
| --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | returns the value of the move.

### long MoveRightWithPad([string charStr](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [long targetOperand](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVE. Moves right a numeric string into an int8 (long) with pad.

```cs
long MoveRightWithPad(string charStr, long targetOperand)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | charStr | Source numeric string.
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | targetOperand | Long value of the target.

#### Returns

| Type | Description
| --- | ---
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | returns the value of the move.

### void MoveToArray([string source](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [Array target](https://learn.microsoft.com/en-us/dotnet/api/system.array?view=net-8.0), [int startPosition](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Moves a source string into an array.

```cs
void MoveToArray(string source, Array target, int startPosition)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | source | The FixedString value to move.
| [Array](https://learn.microsoft.com/en-us/dotnet/api/system.array?view=net-8.0) | target | The array that will receive values from source.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | startPosition | The array element where the copy starts.

### void MoveToArrayWithPad([string source](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [Array target](https://learn.microsoft.com/en-us/dotnet/api/system.array?view=net-8.0), [int startPosition](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Moves a source string into an array.

```cs
void MoveToArrayWithPad(string source, Array target, int startPosition)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | source | The FixedString value to move.
| [Array](https://learn.microsoft.com/en-us/dotnet/api/system.array?view=net-8.0) | target | The array that will receive values from source.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | startPosition | The array element where the copy starts.

### string Replace([string target](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string from](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [int startPos](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int length](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [bool isRightAdg](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

RPG's %SUBST. Replaces characters in a string based on position and length.

```cs
string Replace(string target, string from, int startPos, int length, bool isRightAdg)
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

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The string after the replacement.

### string Replace([string target](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string from](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [int startPos](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [bool isRightAdg](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

RPG's %SUBST. Replaces characters in a string based on position and length.

```cs
string Replace(string target, string from, int startPos, bool isRightAdg)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | target | The string where replacements will occur.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | from | The replace string.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | startPos | Starting position in target.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | isRightAdg | true for right adjust, false for left adjust (default).

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The string after the replacement.

### string Replace([string target](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string from](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [int startPos](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int length](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's %SUBST. Replaces characters in a string based on position and length.

```cs
string Replace(string target, string from, int startPos, int length)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | target | The string where replacements will occur..
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | from | The replace string.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | startPos | Starting position in target.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | length | Length to replace, pass -1 to use the length of the replacement string.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The string after the replacement.

### string ReplaceFixed([string target](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [int baseLength](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [string from](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [int startPos](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int length](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's %SUBST. Replaces characters in a string based on position and length.

```cs
string ReplaceFixed(string target, int baseLength, string from, int startPos, int length)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | target | The string where replacements will occur..
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | baseLength | The length of the resulting string.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | from | The replace string.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | startPos | Starting position in target.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | length | Length to replace, pass -1 to use the length of the replacement string.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The string after the replacement.

### int ScanString([string baseString](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string CmpStr](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [int startPos](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's %SCAN. Returns the first position of the search argument in the source string, or 0 if it was not found.

```cs
int ScanString(string baseString, string CmpStr, int startPos)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | baseString | A character expression that contains the string that scan will search.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | CmpStr | A character expression scan will use to search the baseString.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | startPos | The 1 based start position in baseString.

#### Returns

| Type | Description
| --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | Returns the 1 based starting position of a match relative to the baseString.

### int ScanString([string baseString](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string CmpStr](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

RPG's %SCAN. Returns the first position of the search argument in the source string, or 0 if it was not found.

```cs
int ScanString(string baseString, string CmpStr)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | baseString | A character expression that contains the string that scan will search.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | CmpStr | A character expression scan will use to search the baseString.

#### Returns

| Type | Description
| --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | Returns the 1 based starting position of a match relative to the baseString.

### bool ScanString([string baseString](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string cmpStr](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [int cmpLen](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int startPos](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's SCAN. Attempts to find cmpStr in the baseString.

```cs
bool ScanString(string baseString, string cmpStr, int cmpLen, int startPos)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | baseString | A character expression that contains the string to compare with cmpStr.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | cmpStr | A character expression that baseString is scanned for.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | cmpLen | Default value is the length of cmpStr. Specifies the length of cmpStr that is scanned for in baseString.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | startPos | The 1 based start position in baseString.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | Returns true if cmpStr is found in baseString.

### bool ScanString([string baseString](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string cmpStr](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [int cmpLen](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int startPos](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [Array fndPosArray](https://learn.microsoft.com/en-us/dotnet/api/system.array?view=net-8.0))

RPG's SCAN. Attempts to find cmpStr in the baseString.

```cs
bool ScanString(string baseString, string cmpStr, int cmpLen, int startPos, Array fndPosArray)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | baseString | A character expression that contains the string to compare with cmpStr.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | cmpStr | A character expression that baseString is scanned for.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | cmpLen | Default value is the length of cmpStr. Specifies the length of cmpStr that is scanned for in baseString.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | startPos | The 1 based start position in baseString.
| [Array](https://learn.microsoft.com/en-us/dotnet/api/system.array?view=net-8.0) | fndPosArray | The array on which to store all the positions in baseString where cmpStr starts.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | Returns true if cmpStr is found in baseString.

### string SetHiLoEq([string testString](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [Indicator& hi](/reference/runtime/qsys-runtime/indicator.html), [Indicator& lo](/reference/runtime/qsys-runtime/indicator.html), [Indicator& eq](/reference/runtime/qsys-runtime/indicator.html))

Sets the flags according to the value of testString.

```cs
string SetHiLoEq(string testString, Indicator& hi, Indicator& lo, Indicator& eq)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | testString | The string to test.
| [Indicator&](/reference/runtime/qsys-runtime/indicator.html) | hi | Will be set to '0'.
| [Indicator&](/reference/runtime/qsys-runtime/indicator.html) | lo | Will be set to '0'.
| [Indicator&](/reference/runtime/qsys-runtime/indicator.html) | eq | Will be '1' if testString is all blanks, otherwise '0'.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The test value.

### string SetVaryingLength([string charStr](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [int length](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int limit](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Sets the variable length string to the indicated length, ensuring that it is no longer than limit.

```cs
string SetVaryingLength(string charStr, int length, int limit)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | charStr | A variable length string.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | length | The desired length.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | limit | The maximum allowed length.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The string value at the desired length, at most equal to limit.

### string SubStr([string baseString](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [int startPos](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int subLen](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's SUBST. Returns a substring from baseString, starting at startPos ending at subLen, puts it into target, no padding, no preservation of length.

```cs
string SubStr(string baseString, int startPos, int subLen)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | baseString | A character expression that contains the string SubStr will operate on.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | startPos | The 1 based start position for baseString.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | subLen | The length of the substring.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The string value resulting from the operation.

### string SubStrFixed([string baseString](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [int startPos](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int subLen](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [string target](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

RPG's SUBST. Returns a substring from baseString, starting at startPos ending at subLen, puts it into target. This function preserves the length of the target, no padding.

```cs
string SubStrFixed(string baseString, int startPos, int subLen, string target)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | baseString | A character expression that contains the string SubStr will operate on.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | startPos | The 1 based start position for baseString.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | subLen | The length of the substring.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | target | Target Operand of the substring.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The string value resulting from the operation.

### string SubStrFixedWithPad([string baseString](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [int startPos](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int subLen](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [string target](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

RPG's SUBST. Returns a substring from baseString, starting at startPos ending at subLen, puts it into target. This function preserves the length of the target, and pads the result.

```cs
string SubStrFixedWithPad(string baseString, int startPos, int subLen, string target)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | baseString | A character expression that contains the string SubStr will operate on.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | startPos | The 1 based start position for baseString.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | subLen | The length of the substring.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | target | Target Operand of the substring.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The string value resulting from the operation.

### byte ToByte([string charStr](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Converts a numeric string into a byte number.

```cs
byte ToByte(string charStr)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | charStr | string representing a byte number.

#### Returns

| Type | Description
| --- | ---
| [Byte](https://docs.microsoft.com/en-us/dotnet/api/system.byte) | byte representation of given string.

### DateTime ToDateTime([string charStr](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [DateTimeDataKind dateTimeKind](/reference/runtime/qsys-runtime/date-time-data-kind.html), [DateTimeFormat dateTimeFormat](/reference/datagate/datagate-common/date-time-format.html), [DateTimeSeparator dateTimeSeparator](/reference/runtime/qsys-runtime/date-time-separator.html))

Converts a string representation of a date/time/timestamp into a DateTime.

```cs
DateTime ToDateTime(string charStr, DateTimeDataKind dateTimeKind, DateTimeFormat dateTimeFormat, DateTimeSeparator dateTimeSeparator)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | charStr | The string value representing a date/time/timestamp.
| [DateTimeDataKind](/reference/runtime/qsys-runtime/date-time-data-kind.html) | dateTimeKind | Date, Time, Timestamp.
| [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html) | dateTimeFormat | DateTime format.
| [DateTimeSeparator](/reference/runtime/qsys-runtime/date-time-separator.html) | dateTimeSeparator | string separator.

#### Returns

| Type | Description
| --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | The DateTime value parsed from charStr.

### double ToDouble([string charStr](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Converts a numeric string into a double number.

```cs
double ToDouble(string charStr)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | charStr | string representing a double number.

#### Returns

| Type | Description
| --- | ---
| [Double](https://learn.microsoft.com/en-us/dotnet/api/system.double?view=net-8.0) | double representation of given string.

### decimal ToFixedDecimal([string charStr](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [int digits](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int decimals](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Converts a numeric string into a RPG decimal.

```cs
decimal ToFixedDecimal(string charStr, int digits, int decimals)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | charStr | string representing a decimal number.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | digits | number of digits in the targetOperand.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | decimals | number of decimals in the targetOperand.

#### Returns

| Type | Description
| --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | decimal representation of given string.

### decimal ToFixedDecimalRounded([string charStr](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [int digits](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int decimals](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Converts a numeric string into a RPG decimal with rounding (half adjust).

```cs
decimal ToFixedDecimalRounded(string charStr, int digits, int decimals)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | charStr | string representing a decimal number.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | digits | number of digits in the targetOperand.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | decimals | number of decimals in the targetOperand.

#### Returns

| Type | Description
| --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | decimal representation of given string.

### float ToFloat([string charStr](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Converts a numeric string into a float number.

```cs
float ToFloat(string charStr)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | charStr | string representing a float number.

#### Returns

| Type | Description
| --- | ---
| [Single](https://learn.microsoft.com/en-us/dotnet/api/system.single?view=net-8.0) | float representation of given string.

### short ToInt16([string charStr](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Converts a numeric string into a short number.

```cs
short ToInt16(string charStr)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | charStr | string representing a short number.

#### Returns

| Type | Description
| --- | ---
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | short representation of given string.

### int ToInt32([string charStr](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Converts a numeric string into an int number.

```cs
int ToInt32(string charStr)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | charStr | string representing an int number.

#### Returns

| Type | Description
| --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | int representation of given string.

### long ToInt64([string charStr](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Converts a numeric string into a long number.

```cs
long ToInt64(string charStr)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | charStr | string representing a long number.

#### Returns

| Type | Description
| --- | ---
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | long representation of given string.

### decimal ToPackedDecimal([string charStr](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [int decimals](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Converts a string representing a packed number into a RPG decimal.

```cs
decimal ToPackedDecimal(string charStr, int decimals)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | charStr | string representing a packed decimal number.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | decimals | number of decimal positions in the targetOperand.

#### Returns

| Type | Description
| --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | decimal packed representation of given string.

### decimal ToZonedDecimal([string charStr](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [int digits](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int decimals](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Converts a zoned representation string into a RPG decimal.

```cs
decimal ToZonedDecimal(string charStr, int digits, int decimals)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | charStr | string representing a zoned decimal number.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | digits | number of digits in the targetOperand.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | decimals | number of decimals in the targetOperand.

#### Returns

| Type | Description
| --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | decimal representation of given string.

### string Xlate([string baseString](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string mapFrom](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string mapTo](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [int startPos](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's %Xlate. Translates baseString according to the values of mapFrom, mapTo, and startPos.

```cs
string Xlate(string baseString, string mapFrom, string mapTo, int startPos)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | baseString | The string to be translated.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | mapFrom | A string containing a list of characters that should be replaced.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | mapTo | A string containing a list of characters with replacement values.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | startPos | The 1-based position in the baseString where replacement starts. Defaults to 1.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The string resulting after the Xlate operation.

### string Xlate([string baseString](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string mapFrom](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string mapTo](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string targetString](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [int startPos](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's XLATE. Translates characters in the baseString according to MapFrom, MapTo, startPos and targetString, no padding, no preservation of length.

```cs
string Xlate(string baseString, string mapFrom, string mapTo, string targetString, int startPos)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | baseString | A character expression that contains the string Xlate will operate on.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | mapFrom | From string, if characters are duplicated the first occurrence is used.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | mapTo | To string, describes what the characters in mapFrom will become.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | targetString | Target operand of the Xlate operation.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | startPos | The 1 based start position for baseString.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The string value of the result of the Xlate.

### string XlateFixed([string baseString](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string mapFrom](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string mapTo](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string targetString](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [int startPos](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's XLATE. Translates characters in the baseString according to MapFrom, MapTo, startPos and targetString. This version preserves the length of the result, does NOT pad.

```cs
string XlateFixed(string baseString, string mapFrom, string mapTo, string targetString, int startPos)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | baseString | A character expression that contains the string Xlate will operate on.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | mapFrom | From string, if characters are duplicated the first occurrence is used.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | mapTo | To string, describes what the characters in mapFrom will become.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | targetString | Target operand of the Xlate operation.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | startPos | The 1 based start position for baseString.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The string value of the result of the Xlate.

### string XlateFixedWithPad([string baseString](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string mapFrom](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string mapTo](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string targetString](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [int startPos](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's XLATE. Translates characters in the baseString according to MapFrom, MapTo, startPos and targetString. This version preserves the length of the result, with padding.

```cs
string XlateFixedWithPad(string baseString, string mapFrom, string mapTo, string targetString, int startPos)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | baseString | A character expression that contains the string Xlate will operate on.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | mapFrom | From string, if characters are duplicated the first occurrence is used.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | mapTo | To string, describes what the characters in mapFrom will become.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | targetString | Target operand of the Xlate operation.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | startPos | The 1 based start position for baseString.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The string value of the result of the Xlate.
