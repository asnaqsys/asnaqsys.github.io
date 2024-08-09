---
title: "FixedStringMethods class      | QSYS API Reference Guide"
description: "Contains extension methods for handling RPG operations for FixedString values. "
last_modified_at: 2024-08-09T16:18:25Z
---

Contains extension methods for handling RPG operations for FixedString values.

**Namespace:** ASNA.QSys.Runtime
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>

## Methods

| Signature | Description |
| --- | --- |
| [AdjustEnd\<T\>](#string-adjustend-t-fixedstring-t-charstr-int-length)([FixedString\<T\>](/reference/runtime/qsys-runtime/fixed-string-1.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Adjusts the length of a string, padding on the right if necessary.
| [AdjustStart\<T\>](#string-adjuststart-t-fixedstring-t-charstr-int-length)([FixedString\<T\>](/reference/runtime/qsys-runtime/fixed-string-1.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Adjusts the length of a string, padding on the left if necessary.
| [FromStringBinary\<T\>](#decimal-fromstringbinary-t-fixedstring-t-num-int-digits-int-decimals)([FixedString\<T\>](/reference/runtime/qsys-runtime/fixed-string-1.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Returns a decimal number based on its binary 'memory' representation.
| [FromStringPacked\<T\>](#decimal-fromstringpacked-t-fixedstring-t-num-int-decimals)([FixedString\<T\>](/reference/runtime/qsys-runtime/fixed-string-1.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Returns a decimal number based on its packed 'memory' representation.
| [FromStringZoned\<T\>](#decimal-fromstringzoned-t-fixedstring-t-num-int-digits-int-decimals)([FixedString\<T\>](/reference/runtime/qsys-runtime/fixed-string-1.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Returns a decimal number based on its zoned 'memory' representation.
| [IsBlanks\<T\>](#bool-isblanks-t-fixedstring-t-arg)([FixedString\<T\>](/reference/runtime/qsys-runtime/fixed-string-1.html)) | Tests a string to see if it is all blanks (' ').
| [MoveLeft\<T\>](#datetime-moveleft-t-fixedstring-t-charstr-ifixeddatetime-datetime)([FixedString\<T\>](/reference/runtime/qsys-runtime/fixed-string-1.html), [IFixedDateTime](/reference/runtime/qsys-runtime/i-fixed-date-time.html)) | RPG's MOVEL. Moves left a string expressed in the given format into a date/time type.
| [MoveLeft\<T\>](#short-moveleft-t-fixedstring-t-charstr-short-target)([FixedString\<T\>](/reference/runtime/qsys-runtime/fixed-string-1.html), [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16)) | RPG's MOVEL. Moves left a numeric string into an int2 (short).
| [MoveLeft\<T\>](#short-moveleft-t-fixedstring-t-charstr-short-target)([FixedString\<T\>](/reference/runtime/qsys-runtime/fixed-string-1.html), [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16)) | RPG's MOVEL. Moves left a numeric string into an int4 (int).
| [MoveLeft\<T\>](#short-moveleft-t-fixedstring-t-charstr-short-target)([FixedString\<T\>](/reference/runtime/qsys-runtime/fixed-string-1.html), [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16)) | RPG's MOVEL. Moves left a numeric string into an int8 (long).
| [MoveLeftToChar\<T\>](#char-movelefttochar-t-fixedstring-t-charstr)([FixedString\<T\>](/reference/runtime/qsys-runtime/fixed-string-1.html)) | RPG's MOVE. Moves left a string into a character.
| [MoveLeftWithPad\<T\>](#short-moveleftwithpad-t-fixedstring-t-charstr-short-target)([FixedString\<T\>](/reference/runtime/qsys-runtime/fixed-string-1.html), [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16)) | RPG's MOVEL. Moves left a numeric string into an int2 (short) with pad.
| [MoveLeftWithPad\<T\>](#short-moveleftwithpad-t-fixedstring-t-charstr-short-target)([FixedString\<T\>](/reference/runtime/qsys-runtime/fixed-string-1.html), [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16)) | RPG's MOVEL. Moves left a numeric string into an int4 (int) with pad.
| [MoveLeftWithPad\<T\>](#short-moveleftwithpad-t-fixedstring-t-charstr-short-target)([FixedString\<T\>](/reference/runtime/qsys-runtime/fixed-string-1.html), [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16)) | RPG's MOVEL. Moves right a numeric string into an int8 (long) with pad.
| [MoveRight\<T\>](#datetime-moveright-t-fixedstring-t-charstr-ifixeddatetime-datetime)([FixedString\<T\>](/reference/runtime/qsys-runtime/fixed-string-1.html), [IFixedDateTime](/reference/runtime/qsys-runtime/i-fixed-date-time.html)) | RPG's MOVE. Moves right a string expressed in the given format into a date/time type.
| [MoveRight\<T\>](#short-moveright-t-fixedstring-t-charstr-short-target)([FixedString\<T\>](/reference/runtime/qsys-runtime/fixed-string-1.html), [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16)) | RPG's MOVE. Moves right a numeric string into an int2 (short).
| [MoveRight\<T\>](#short-moveright-t-fixedstring-t-charstr-short-target)([FixedString\<T\>](/reference/runtime/qsys-runtime/fixed-string-1.html), [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16)) | RPG's MOVE. Moves right a numeric string into an int4 (int).
| [MoveRight\<T\>](#short-moveright-t-fixedstring-t-charstr-short-target)([FixedString\<T\>](/reference/runtime/qsys-runtime/fixed-string-1.html), [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16)) | RPG's MOVE. Moves right a numeric string into an int8 (long).
| [MoveRightToChar\<T\>](#char-moverighttochar-t-fixedstring-t-charstr)([FixedString\<T\>](/reference/runtime/qsys-runtime/fixed-string-1.html)) | RPG's MOVE. Moves right a string into a character.
| [MoveRightWithPad\<T\>](#short-moverightwithpad-t-fixedstring-t-charstr-short-target)([FixedString\<T\>](/reference/runtime/qsys-runtime/fixed-string-1.html), [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16)) | RPG's MOVE. Moves right a numeric string into an int2 (short) with pad.
| [MoveRightWithPad\<T\>](#short-moverightwithpad-t-fixedstring-t-charstr-short-target)([FixedString\<T\>](/reference/runtime/qsys-runtime/fixed-string-1.html), [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16)) | RPG's MOVE. Moves right a numeric string into an int4 (int) with pad.
| [MoveRightWithPad\<T\>](#short-moverightwithpad-t-fixedstring-t-charstr-short-target)([FixedString\<T\>](/reference/runtime/qsys-runtime/fixed-string-1.html), [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16)) | RPG's MOVE. Moves right a numeric string into an int8 (long) with pad.
| [ReplaceFixed\<T\>](#string-replacefixed-t-fixedstring-t-basestring-int-baselenconst-string-repstring-int-startpos-int-lengthtoreplace)([FixedString\<T\>](/reference/runtime/qsys-runtime/fixed-string-1.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's %REPLACE. Replaces a length of characters in a FixedString value with a replacement string.
| [SetHiLoEq\<T\>](#string-sethiloeq-t-fixedstring-t-teststring-indicator-hi-indicator-lo-indicator-eq)([FixedString\<T\>](/reference/runtime/qsys-runtime/fixed-string-1.html), [Indicator&](/reference/runtime/qsys-runtime/indicator.html), [Indicator&](/reference/runtime/qsys-runtime/indicator.html), [Indicator&](/reference/runtime/qsys-runtime/indicator.html)) | Sets the flags according to the value of testString.
| [SubStr\<T\>](#string-substr-t-fixedstring-t-basestring-int-startpos-int-sublen)([FixedString\<T\>](/reference/runtime/qsys-runtime/fixed-string-1.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's SUBST. Returns a substring from baseString, starting at startPos ending at subLen, puts it into target, no padding, no preservation of length.
| [SubStr\<T\>](#string-substr-t-fixedstring-t-basestring-int-startpos-int-sublen-indicator-errind)([FixedString\<T\>](/reference/runtime/qsys-runtime/fixed-string-1.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Indicator&](/reference/runtime/qsys-runtime/indicator.html)) | RPG's SUBST. Returns a substring from baseString, starting at startPos ending at subLen, puts it into target, no padding, no preservation of length.
| [ToDateTime\<T\>](#datetime-todatetime-t-fixedstring-t-charstr-ifixeddatetime-datetime)([FixedString\<T\>](/reference/runtime/qsys-runtime/fixed-string-1.html), [IFixedDateTime](/reference/runtime/qsys-runtime/i-fixed-date-time.html)) | Converts a string representation of a date/time/timestamp into a DateTime.
| [ToDateTime\<T\>](#datetime-todatetime-t-fixedstring-t-charstr-datetimedatakind-datetimekind-datetimeformat-datetimeformat-datetimeseparator-datetimeseparator)([FixedString\<T\>](/reference/runtime/qsys-runtime/fixed-string-1.html), [DateTimeDataKind](/reference/runtime/qsys-runtime/date-time-data-kind.html), [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html), [DateTimeSeparator](/reference/runtime/qsys-runtime/date-time-separator.html)) | Converts a string representation of a date/time/timestamp into a DateTime.
| [ToFixedDecimal\<T\>](#decimal-tofixeddecimal-t-fixedstring-t-charstr-int-digits-int-decimals)([FixedString\<T\>](/reference/runtime/qsys-runtime/fixed-string-1.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Converts a numeric string into a RPG decimal.
| [ToFixedDecimalRounded\<T\>](#decimal-tofixeddecimalrounded-t-fixedstring-t-charstr-int-digits-int-decimals)([FixedString\<T\>](/reference/runtime/qsys-runtime/fixed-string-1.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Converts a numeric string into a RPG decimal with rounding (half adjust).
| [ToPackedDecimal\<T\>](#decimal-topackeddecimal-t-fixedstring-t-charstr-int-decimals)([FixedString\<T\>](/reference/runtime/qsys-runtime/fixed-string-1.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Converts a string representing a packed decimal into a decimal number.
| [ToZonedDecimal\<T\>](#decimal-tozoneddecimal-t-fixedstring-t-charstr-int-digits-int-decimals)([FixedString\<T\>](/reference/runtime/qsys-runtime/fixed-string-1.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Converts a string representing a zoned decimal into a decimal number.
| [TrimEnd\<T\>](#string-trimend-t-fixedstring-t-basestring)([FixedString\<T\>](/reference/runtime/qsys-runtime/fixed-string-1.html)) | Removes all the trailing white-space characters from the current string.
| [TrimStart\<T\>](#string-trimstart-t-fixedstring-t-basestring)([FixedString\<T\>](/reference/runtime/qsys-runtime/fixed-string-1.html)) | Removes all the leading white-space characters from the current string.

### string AdjustEnd\<T\>([FixedString\<T\> charStr](/reference/runtime/qsys-runtime/fixed-string-1.html), [int length](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Adjusts the length of a string, padding on the right if necessary.

```cs
string AdjustEnd<T>(FixedString<T> charStr, int length)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [FixedString\<T\>](/reference/runtime/qsys-runtime/fixed-string-1.html) | charStr | The string to adjust.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | length | The desired length.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The string at the desired length, after trimming or padding on the right.

### string AdjustStart\<T\>([FixedString\<T\> charStr](/reference/runtime/qsys-runtime/fixed-string-1.html), [int length](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Adjusts the length of a string, padding on the left if necessary.

```cs
string AdjustStart<T>(FixedString<T> charStr, int length)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [FixedString\<T\>](/reference/runtime/qsys-runtime/fixed-string-1.html) | charStr | The string to adjust.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | length | The desired length.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The string at the desired length, after trimming or padding on the left.

### decimal FromStringBinary\<T\>([FixedString\<T\> num](/reference/runtime/qsys-runtime/fixed-string-1.html), [int digits](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int decimals](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Returns a decimal number based on its binary 'memory' representation.

```cs
decimal FromStringBinary<T>(FixedString<T> num, int digits, int decimals)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [FixedString\<T\>](/reference/runtime/qsys-runtime/fixed-string-1.html) | num | The string representation of the number.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | digits | The number of digits in the decimal number.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | decimals | The number of decimal positions in the decimal number.

#### Returns

| Type | Description
| --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | The decimal number corresponding to the binary decimal representation.

### decimal FromStringPacked\<T\>([FixedString\<T\> num](/reference/runtime/qsys-runtime/fixed-string-1.html), [int decimals](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Returns a decimal number based on its packed 'memory' representation.

```cs
decimal FromStringPacked<T>(FixedString<T> num, int decimals)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [FixedString\<T\>](/reference/runtime/qsys-runtime/fixed-string-1.html) | num | The string representation of the number.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | decimals | The number of decimal positions in the decimal number.

#### Returns

| Type | Description
| --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | The decimal number corresponding to the packed decimal representation.

### decimal FromStringZoned\<T\>([FixedString\<T\> num](/reference/runtime/qsys-runtime/fixed-string-1.html), [int digits](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int decimals](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Returns a decimal number based on its zoned 'memory' representation.

```cs
decimal FromStringZoned<T>(FixedString<T> num, int digits, int decimals)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [FixedString\<T\>](/reference/runtime/qsys-runtime/fixed-string-1.html) | num | The string representation of the number.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | digits | The total number of digits the decimal has.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | decimals | The number of decimal positions in the decimal number.

#### Returns

| Type | Description
| --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | The decimal number corresponding to the zoned decimal representation.

### bool IsBlanks\<T\>([FixedString\<T\> arg](/reference/runtime/qsys-runtime/fixed-string-1.html))

Tests a string to see if it is all blanks (' ').

```cs
bool IsBlanks<T>(FixedString<T> arg)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [FixedString\<T\>](/reference/runtime/qsys-runtime/fixed-string-1.html) | arg | The fixed string to test.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | True if the string contains blanks.

### DateTime MoveLeft\<T\>([FixedString\<T\> charStr](/reference/runtime/qsys-runtime/fixed-string-1.html), [IFixedDateTime dateTime](/reference/runtime/qsys-runtime/i-fixed-date-time.html))

RPG's MOVEL. Moves left a string expressed in the given format into a date/time type.

```cs
DateTime MoveLeft<T>(FixedString<T> charStr, IFixedDateTime dateTime)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [FixedString\<T\>](/reference/runtime/qsys-runtime/fixed-string-1.html) | charStr | Source FixedString.
| [IFixedDateTime](/reference/runtime/qsys-runtime/i-fixed-date-time.html) | dateTime | Destination FixedDate, FixedTime, or FixedTimestamp.

#### Returns

| Type | Description
| --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | The value that results after the Move operation, as a DateTime value.

### short MoveLeft\<T\>([FixedString\<T\> charStr](/reference/runtime/qsys-runtime/fixed-string-1.html), [short target](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVEL. Moves left a numeric string into an int2 (short).

```cs
short MoveLeft<T>(FixedString<T> charStr, short target)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [FixedString\<T\>](/reference/runtime/qsys-runtime/fixed-string-1.html) | charStr | Source numeric string.
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | target | Short value of the target.

#### Returns

| Type | Description
| --- | ---
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | returns the value of the move.

### short MoveLeft\<T\>([FixedString\<T\> charStr](/reference/runtime/qsys-runtime/fixed-string-1.html), [short target](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVEL. Moves left a numeric string into an int4 (int).

```cs
short MoveLeft<T>(FixedString<T> charStr, short target)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [FixedString\<T\>](/reference/runtime/qsys-runtime/fixed-string-1.html) | charStr | Source numeric string.
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | target | Int value of the target.

#### Returns

| Type | Description
| --- | ---
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | returns the value of the move.

### short MoveLeft\<T\>([FixedString\<T\> charStr](/reference/runtime/qsys-runtime/fixed-string-1.html), [short target](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVEL. Moves left a numeric string into an int8 (long).

```cs
short MoveLeft<T>(FixedString<T> charStr, short target)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [FixedString\<T\>](/reference/runtime/qsys-runtime/fixed-string-1.html) | charStr | Source numeric string.
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | target | Long value of the target.

#### Returns

| Type | Description
| --- | ---
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | returns the value of the move.

### char MoveLeftToChar\<T\>([FixedString\<T\> charStr](/reference/runtime/qsys-runtime/fixed-string-1.html))

RPG's MOVE. Moves left a string into a character.

```cs
char MoveLeftToChar<T>(FixedString<T> charStr)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [FixedString\<T\>](/reference/runtime/qsys-runtime/fixed-string-1.html) | charStr | A string the represents the source of the move.

#### Returns

| Type | Description
| --- | ---
| [Char](https://docs.microsoft.com/en-us/dotnet/api/system.char) | The leftmost character of charStr.

### short MoveLeftWithPad\<T\>([FixedString\<T\> charStr](/reference/runtime/qsys-runtime/fixed-string-1.html), [short target](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVEL. Moves left a numeric string into an int2 (short) with pad.

```cs
short MoveLeftWithPad<T>(FixedString<T> charStr, short target)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [FixedString\<T\>](/reference/runtime/qsys-runtime/fixed-string-1.html) | charStr | Source numeric string.
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | target | Short value of the target.

#### Returns

| Type | Description
| --- | ---
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | returns the value of the move.

### short MoveLeftWithPad\<T\>([FixedString\<T\> charStr](/reference/runtime/qsys-runtime/fixed-string-1.html), [short target](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVEL. Moves left a numeric string into an int4 (int) with pad.

```cs
short MoveLeftWithPad<T>(FixedString<T> charStr, short target)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [FixedString\<T\>](/reference/runtime/qsys-runtime/fixed-string-1.html) | charStr | Source numeric string.
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | target | Int value of the target.

#### Returns

| Type | Description
| --- | ---
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | returns the value of the move.

### short MoveLeftWithPad\<T\>([FixedString\<T\> charStr](/reference/runtime/qsys-runtime/fixed-string-1.html), [short target](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVEL. Moves right a numeric string into an int8 (long) with pad.

```cs
short MoveLeftWithPad<T>(FixedString<T> charStr, short target)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [FixedString\<T\>](/reference/runtime/qsys-runtime/fixed-string-1.html) | charStr | Source numeric string.
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | target | Long value of the target.

#### Returns

| Type | Description
| --- | ---
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | returns the value of the move.

### DateTime MoveRight\<T\>([FixedString\<T\> charStr](/reference/runtime/qsys-runtime/fixed-string-1.html), [IFixedDateTime dateTime](/reference/runtime/qsys-runtime/i-fixed-date-time.html))

RPG's MOVE. Moves right a string expressed in the given format into a date/time type.

```cs
DateTime MoveRight<T>(FixedString<T> charStr, IFixedDateTime dateTime)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [FixedString\<T\>](/reference/runtime/qsys-runtime/fixed-string-1.html) | charStr | Source FixedString.
| [IFixedDateTime](/reference/runtime/qsys-runtime/i-fixed-date-time.html) | dateTime | Destination FixedDate, FixedTime, or FixedTimestamp.

#### Returns

| Type | Description
| --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | The value that results after the Move operation, as a DateTime value.

### short MoveRight\<T\>([FixedString\<T\> charStr](/reference/runtime/qsys-runtime/fixed-string-1.html), [short target](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVE. Moves right a numeric string into an int2 (short).

```cs
short MoveRight<T>(FixedString<T> charStr, short target)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [FixedString\<T\>](/reference/runtime/qsys-runtime/fixed-string-1.html) | charStr | Source numeric string.
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | target | Short value of the target.

#### Returns

| Type | Description
| --- | ---
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | returns the value of the move.

### short MoveRight\<T\>([FixedString\<T\> charStr](/reference/runtime/qsys-runtime/fixed-string-1.html), [short target](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVE. Moves right a numeric string into an int4 (int).

```cs
short MoveRight<T>(FixedString<T> charStr, short target)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [FixedString\<T\>](/reference/runtime/qsys-runtime/fixed-string-1.html) | charStr | Source numeric string.
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | target | Int value of the target.

#### Returns

| Type | Description
| --- | ---
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | returns the value of the move.

### short MoveRight\<T\>([FixedString\<T\> charStr](/reference/runtime/qsys-runtime/fixed-string-1.html), [short target](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVE. Moves right a numeric string into an int8 (long).

```cs
short MoveRight<T>(FixedString<T> charStr, short target)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [FixedString\<T\>](/reference/runtime/qsys-runtime/fixed-string-1.html) | charStr | Source numeric string.
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | target | Long value of the target.

#### Returns

| Type | Description
| --- | ---
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | returns the value of the move.

### char MoveRightToChar\<T\>([FixedString\<T\> charStr](/reference/runtime/qsys-runtime/fixed-string-1.html))

RPG's MOVE. Moves right a string into a character.

```cs
char MoveRightToChar<T>(FixedString<T> charStr)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [FixedString\<T\>](/reference/runtime/qsys-runtime/fixed-string-1.html) | charStr | A string the represents the source of the move.

#### Returns

| Type | Description
| --- | ---
| [Char](https://docs.microsoft.com/en-us/dotnet/api/system.char) | The rightmost character of charStr.

### short MoveRightWithPad\<T\>([FixedString\<T\> charStr](/reference/runtime/qsys-runtime/fixed-string-1.html), [short target](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVE. Moves right a numeric string into an int2 (short) with pad.

```cs
short MoveRightWithPad<T>(FixedString<T> charStr, short target)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [FixedString\<T\>](/reference/runtime/qsys-runtime/fixed-string-1.html) | charStr | Source numeric string.
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | target | Short value of the target.

#### Returns

| Type | Description
| --- | ---
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | returns the value of the move.

### short MoveRightWithPad\<T\>([FixedString\<T\> charStr](/reference/runtime/qsys-runtime/fixed-string-1.html), [short target](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVE. Moves right a numeric string into an int4 (int) with pad.

```cs
short MoveRightWithPad<T>(FixedString<T> charStr, short target)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [FixedString\<T\>](/reference/runtime/qsys-runtime/fixed-string-1.html) | charStr | Source numeric string.
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | target | Int value of the target.

#### Returns

| Type | Description
| --- | ---
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | returns the value of the move.

### short MoveRightWithPad\<T\>([FixedString\<T\> charStr](/reference/runtime/qsys-runtime/fixed-string-1.html), [short target](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVE. Moves right a numeric string into an int8 (long) with pad.

```cs
short MoveRightWithPad<T>(FixedString<T> charStr, short target)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [FixedString\<T\>](/reference/runtime/qsys-runtime/fixed-string-1.html) | charStr | Source numeric string.
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | target | Long value of the target.

#### Returns

| Type | Description
| --- | ---
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | returns the value of the move.

### string ReplaceFixed\<T\>([FixedString\<T\> baseString](/reference/runtime/qsys-runtime/fixed-string-1.html), [int baseLenConst](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [string repString](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [int startPos](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int lengthToReplace](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's %REPLACE. Replaces a length of characters in a FixedString value with a replacement string.

```cs
string ReplaceFixed<T>(FixedString<T> baseString, int baseLenConst, string repString, int startPos, int lengthToReplace)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [FixedString\<T\>](/reference/runtime/qsys-runtime/fixed-string-1.html) | baseString | Original FixedString value where replacement will occur.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | baseLenConst | Length to adjust the resulting string to.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | repString | Replacement string.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | startPos | Position in the original string where replacement will start.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | lengthToReplace | Number of character in the original string to replace.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The string after the replacement and length adjustment.

### string SetHiLoEq\<T\>([FixedString\<T\> testString](/reference/runtime/qsys-runtime/fixed-string-1.html), [Indicator& hi](/reference/runtime/qsys-runtime/indicator.html), [Indicator& lo](/reference/runtime/qsys-runtime/indicator.html), [Indicator& eq](/reference/runtime/qsys-runtime/indicator.html))

Sets the flags according to the value of testString.

```cs
string SetHiLoEq<T>(FixedString<T> testString, Indicator& hi, Indicator& lo, Indicator& eq)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [FixedString\<T\>](/reference/runtime/qsys-runtime/fixed-string-1.html) | testString | The string to test.
| [Indicator&](/reference/runtime/qsys-runtime/indicator.html) | hi | Will be set to '0'.
| [Indicator&](/reference/runtime/qsys-runtime/indicator.html) | lo | Will be set to '0'.
| [Indicator&](/reference/runtime/qsys-runtime/indicator.html) | eq | Will be '1' if testString is all blanks, otherwise '0'.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | A copy of testString.

### string SubStr\<T\>([FixedString\<T\> baseString](/reference/runtime/qsys-runtime/fixed-string-1.html), [int startPos](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int subLen](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's SUBST. Returns a substring from baseString, starting at startPos ending at subLen, puts it into target, no padding, no preservation of length.

```cs
string SubStr<T>(FixedString<T> baseString, int startPos, int subLen)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [FixedString\<T\>](/reference/runtime/qsys-runtime/fixed-string-1.html) | baseString | A character expression that contains the string SubStr will operate on.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | startPos | The 1-based start position for baseString.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | subLen | The length of the substring.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The string value resulting from the operation.

### string SubStr\<T\>([FixedString\<T\> baseString](/reference/runtime/qsys-runtime/fixed-string-1.html), [int startPos](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int subLen](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [Indicator& errInd](/reference/runtime/qsys-runtime/indicator.html))

RPG's SUBST. Returns a substring from baseString, starting at startPos ending at subLen, puts it into target, no padding, no preservation of length.

```cs
string SubStr<T>(FixedString<T> baseString, int startPos, int subLen, Indicator& errInd)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [FixedString\<T\>](/reference/runtime/qsys-runtime/fixed-string-1.html) | baseString | A character expression that contains the string SubStr will operate on.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | startPos | The 1-based start position for baseString.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | subLen | The length of the substring.
| [Indicator&](/reference/runtime/qsys-runtime/indicator.html) | errInd | Indicator will be set if a runtime error occurs.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The string value resulting from the operation.

### DateTime ToDateTime\<T\>([FixedString\<T\> charStr](/reference/runtime/qsys-runtime/fixed-string-1.html), [IFixedDateTime dateTime](/reference/runtime/qsys-runtime/i-fixed-date-time.html))

Converts a string representation of a date/time/timestamp into a DateTime.

```cs
DateTime ToDateTime<T>(FixedString<T> charStr, IFixedDateTime dateTime)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [FixedString\<T\>](/reference/runtime/qsys-runtime/fixed-string-1.html) | charStr | The FixedString value representing a date/time/timestamp.
| [IFixedDateTime](/reference/runtime/qsys-runtime/i-fixed-date-time.html) | dateTime | FixedDate, FixedTime, FixedTimestamp that determines the format.

#### Returns

| Type | Description
| --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | The DateTime value parsed from charStr.

### DateTime ToDateTime\<T\>([FixedString\<T\> charStr](/reference/runtime/qsys-runtime/fixed-string-1.html), [DateTimeDataKind dateTimeKind](/reference/runtime/qsys-runtime/date-time-data-kind.html), [DateTimeFormat dateTimeFormat](/reference/datagate/datagate-common/date-time-format.html), [DateTimeSeparator dateTimeSeparator](/reference/runtime/qsys-runtime/date-time-separator.html))

Converts a string representation of a date/time/timestamp into a DateTime.

```cs
DateTime ToDateTime<T>(FixedString<T> charStr, DateTimeDataKind dateTimeKind, DateTimeFormat dateTimeFormat, DateTimeSeparator dateTimeSeparator)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [FixedString\<T\>](/reference/runtime/qsys-runtime/fixed-string-1.html) | charStr | string representing a date/time/timestamp.
| [DateTimeDataKind](/reference/runtime/qsys-runtime/date-time-data-kind.html) | dateTimeKind | Date, Time, Timestamp.
| [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html) | dateTimeFormat | DateTime format.
| [DateTimeSeparator](/reference/runtime/qsys-runtime/date-time-separator.html) | dateTimeSeparator | string separator.

#### Returns

| Type | Description
| --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | The DateTime value parsed from charStr.

### decimal ToFixedDecimal\<T\>([FixedString\<T\> charStr](/reference/runtime/qsys-runtime/fixed-string-1.html), [int digits](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int decimals](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Converts a numeric string into a RPG decimal.

```cs
decimal ToFixedDecimal<T>(FixedString<T> charStr, int digits, int decimals)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [FixedString\<T\>](/reference/runtime/qsys-runtime/fixed-string-1.html) | charStr | String representing a decimal number in the current culture.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | digits | Number of digits in the target.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | decimals | Number of decimals in the target.

#### Returns

| Type | Description
| --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | Decimal equivalent of the given string.

### decimal ToFixedDecimalRounded\<T\>([FixedString\<T\> charStr](/reference/runtime/qsys-runtime/fixed-string-1.html), [int digits](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int decimals](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Converts a numeric string into a RPG decimal with rounding (half adjust).

```cs
decimal ToFixedDecimalRounded<T>(FixedString<T> charStr, int digits, int decimals)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [FixedString\<T\>](/reference/runtime/qsys-runtime/fixed-string-1.html) | charStr | string representing a decimal number.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | digits | number of digits in the target.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | decimals | number of decimals in the target.

#### Returns

| Type | Description
| --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | decimal representation of given string.

### decimal ToPackedDecimal\<T\>([FixedString\<T\> charStr](/reference/runtime/qsys-runtime/fixed-string-1.html), [int decimals](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Converts a string representing a packed decimal into a decimal number.

```cs
decimal ToPackedDecimal<T>(FixedString<T> charStr, int decimals)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [FixedString\<T\>](/reference/runtime/qsys-runtime/fixed-string-1.html) | charStr | String representing a packed decimal.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | decimals | Number of decimals in the target.

#### Returns

| Type | Description
| --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | Decimal equivalent of the given string.

### decimal ToZonedDecimal\<T\>([FixedString\<T\> charStr](/reference/runtime/qsys-runtime/fixed-string-1.html), [int digits](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int decimals](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Converts a string representing a zoned decimal into a decimal number.

```cs
decimal ToZonedDecimal<T>(FixedString<T> charStr, int digits, int decimals)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [FixedString\<T\>](/reference/runtime/qsys-runtime/fixed-string-1.html) | charStr | String representing a zoned decimal.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | digits | Number of digits in the target.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | decimals | Number of decimals in the target.

#### Returns

| Type | Description
| --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | Decimal equivalent of the given string.

### string TrimEnd\<T\>([FixedString\<T\> baseString](/reference/runtime/qsys-runtime/fixed-string-1.html))

Removes all the trailing white-space characters from the current string.

```cs
string TrimEnd<T>(FixedString<T> baseString)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [FixedString\<T\>](/reference/runtime/qsys-runtime/fixed-string-1.html) | baseString | The FixedString value to trim.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The string that remains after all white-space characters are removed from theend of the current string. If no characters can be trimmed from the current instance,the method returns the current instance unchanged.

### string TrimStart\<T\>([FixedString\<T\> baseString](/reference/runtime/qsys-runtime/fixed-string-1.html))

Removes all the leading white-space characters from the current string.

```cs
string TrimStart<T>(FixedString<T> baseString)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [FixedString\<T\>](/reference/runtime/qsys-runtime/fixed-string-1.html) | baseString | The FixedString value to trim.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The string that remains after all white-space characters are removed from thebegining of the current string. If no characters can be trimmed from the current instance,the method returns the current instance unchanged.
