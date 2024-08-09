---
title: "IndicatorMethods class        | QSYS API Reference Guide"
description: "Contains extension methods for handling RPG operations for Indicator values. "
last_modified_at: 2024-08-09T17:25:29Z
---

Contains extension methods for handling RPG operations for Indicator values.

**Namespace:** ASNA.QSys.Runtime
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>

## Methods

| Signature | Description |
| --- | --- |
| [MoveLeft](#string-moveleftindicator-character-string-targetoperand)([Indicator](/reference/runtime/qsys-runtime/indicator.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | RPG's MOVEL. Moves left a character to a string with pad.
| [MoveLeft](#short-moveleftindicator-character-short-targetoperand)([Indicator](/reference/runtime/qsys-runtime/indicator.html), [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16)) | RPG's MOVEL. Moves left a character to a short.
| [MoveLeft](#int-moveleftindicator-character-int-targetoperand)([Indicator](/reference/runtime/qsys-runtime/indicator.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's MOVEL. Moves left a character to an int.
| [MoveLeft](#long-moveleftindicator-character-long-targetoperand)([Indicator](/reference/runtime/qsys-runtime/indicator.html), [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64)) | RPG's MOVEL. Moves left a character to a long.
| [MoveLeftToChar](#char-movelefttocharindicator-character)([Indicator](/reference/runtime/qsys-runtime/indicator.html)) | RPG's MOVEL. Moves left a character to a character.
| [MoveLeftWithPad](#string-moveleftwithpadindicator-character-string-targetoperand)([Indicator](/reference/runtime/qsys-runtime/indicator.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | RPG's MOVEL. Moves left a character to a string with pad.
| [MoveLeftWithPad](#short-moveleftwithpadindicator-character-short-targetoperand)([Indicator](/reference/runtime/qsys-runtime/indicator.html), [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16)) | RPG's MOVEL. Moves left a character to a short with pad.
| [MoveLeftWithPad](#int-moveleftwithpadindicator-character-int-targetoperand)([Indicator](/reference/runtime/qsys-runtime/indicator.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's MOVEL. Moves left a character to an int with pad.
| [MoveLeftWithPad](#long-moveleftwithpadindicator-character-long-targetoperand)([Indicator](/reference/runtime/qsys-runtime/indicator.html), [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64)) | RPG's MOVE. Moves right a character to a long with pad.
| [MoveRight](#string-moverightindicator-character-string-targetoperand)([Indicator](/reference/runtime/qsys-runtime/indicator.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | RPG's MOVE. Moves right a character to a string.
| [MoveRight](#short-moverightindicator-character-short-targetoperand)([Indicator](/reference/runtime/qsys-runtime/indicator.html), [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16)) | RPG's MOVE. Moves right a character to a short.
| [MoveRight](#int-moverightindicator-character-int-targetoperand)([Indicator](/reference/runtime/qsys-runtime/indicator.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's MOVE. Moves right a character to an int.
| [MoveRight](#long-moverightindicator-character-long-targetoperand)([Indicator](/reference/runtime/qsys-runtime/indicator.html), [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64)) | RPG's MOVE. Moves right a character to a long.
| [MoveRightToChar](#char-moverighttocharindicator-character)([Indicator](/reference/runtime/qsys-runtime/indicator.html)) | RPG's MOVE. Moves right a character to a character.
| [MoveRightWithPad](#string-moverightwithpadindicator-character-string-targetoperand)([Indicator](/reference/runtime/qsys-runtime/indicator.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | RPG's MOVE. Moves right a character to a string with pad.
| [MoveRightWithPad](#short-moverightwithpadindicator-character-short-targetoperand)([Indicator](/reference/runtime/qsys-runtime/indicator.html), [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16)) | RPG's MOVE. Moves right a character to a short with pad.
| [MoveRightWithPad](#int-moverightwithpadindicator-character-int-targetoperand)([Indicator](/reference/runtime/qsys-runtime/indicator.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's MOVE. Moves right a character to a int with pad.
| [MoveRightWithPad](#long-moverightwithpadindicator-character-long-targetoperand)([Indicator](/reference/runtime/qsys-runtime/indicator.html), [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64)) | RPG's MOVE. Moves right a character to a long with pad.
| [TestTime](#bool-testtimestring-num-datetimedatakind-kind-datetimeformat-format-datetimeseparator-separator)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [DateTimeDataKind](/reference/runtime/qsys-runtime/date-time-data-kind.html), [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html), [DateTimeSeparator](/reference/runtime/qsys-runtime/date-time-separator.html)) | Tests whether a string containing a number represents a valid date/time/timestamp value. 

### string MoveLeft([Indicator character](/reference/runtime/qsys-runtime/indicator.html), [string targetOperand](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

RPG's MOVEL. Moves left a character to a string with pad.

```cs
string MoveLeft(Indicator character, string targetOperand)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Indicator](/reference/runtime/qsys-runtime/indicator.html) | character | A char that represents the source of the move.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | targetOperand | targetOperand represents what is currently in the target of the move.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | returns the value of the move.

### short MoveLeft([Indicator character](/reference/runtime/qsys-runtime/indicator.html), [short targetOperand](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVEL. Moves left a character to a short.

```cs
short MoveLeft(Indicator character, short targetOperand)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Indicator](/reference/runtime/qsys-runtime/indicator.html) | character | A char that represents the source of the move.
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | targetOperand | targetOperand represents what is currently in the target of the move.

#### Returns

| Type | Description
| --- | ---
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | returns the value of the move.

### int MoveLeft([Indicator character](/reference/runtime/qsys-runtime/indicator.html), [int targetOperand](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVEL. Moves left a character to an int.

```cs
int MoveLeft(Indicator character, int targetOperand)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Indicator](/reference/runtime/qsys-runtime/indicator.html) | character | A char that represents the source of the move.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetOperand | targetOperand represents what is currently in the target of the move.

#### Returns

| Type | Description
| --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | returns the value of the move.

### long MoveLeft([Indicator character](/reference/runtime/qsys-runtime/indicator.html), [long targetOperand](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVEL. Moves left a character to a long.

```cs
long MoveLeft(Indicator character, long targetOperand)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Indicator](/reference/runtime/qsys-runtime/indicator.html) | character | A char that represents the source of the move.
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | targetOperand | targetOperand represents what is currently in the target of the move.

#### Returns

| Type | Description
| --- | ---
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | returns the value of the move.

### char MoveLeftToChar([Indicator character](/reference/runtime/qsys-runtime/indicator.html))

RPG's MOVEL. Moves left a character to a character.

```cs
char MoveLeftToChar(Indicator character)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Indicator](/reference/runtime/qsys-runtime/indicator.html) | character | A char that represents the source of the move.

#### Returns

| Type | Description
| --- | ---
| [Char](https://docs.microsoft.com/en-us/dotnet/api/system.char) | returns the value of the move.

### string MoveLeftWithPad([Indicator character](/reference/runtime/qsys-runtime/indicator.html), [string targetOperand](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

RPG's MOVEL. Moves left a character to a string with pad.

```cs
string MoveLeftWithPad(Indicator character, string targetOperand)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Indicator](/reference/runtime/qsys-runtime/indicator.html) | character | A char that represents the source of the move.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | targetOperand | targetOperand represents what is currently in the target of the move.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | returns the value of the move.

### short MoveLeftWithPad([Indicator character](/reference/runtime/qsys-runtime/indicator.html), [short targetOperand](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVEL. Moves left a character to a short with pad.

```cs
short MoveLeftWithPad(Indicator character, short targetOperand)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Indicator](/reference/runtime/qsys-runtime/indicator.html) | character | A char that represents the source of the move.
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | targetOperand | targetOperand represents what is currently in the target of the move.

#### Returns

| Type | Description
| --- | ---
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | returns the value of the move.

### int MoveLeftWithPad([Indicator character](/reference/runtime/qsys-runtime/indicator.html), [int targetOperand](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVEL. Moves left a character to an int with pad.

```cs
int MoveLeftWithPad(Indicator character, int targetOperand)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Indicator](/reference/runtime/qsys-runtime/indicator.html) | character | A char that represents the source of the move.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetOperand | targetOperand represents what is currently in the target of the move.

#### Returns

| Type | Description
| --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | returns the value of the move.

### long MoveLeftWithPad([Indicator character](/reference/runtime/qsys-runtime/indicator.html), [long targetOperand](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVE. Moves right a character to a long with pad.

```cs
long MoveLeftWithPad(Indicator character, long targetOperand)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Indicator](/reference/runtime/qsys-runtime/indicator.html) | character | A char that represents the source of the move.
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | targetOperand | targetOperand represents what is currently in the target of the move.

#### Returns

| Type | Description
| --- | ---
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | returns the value of the move.

### string MoveRight([Indicator character](/reference/runtime/qsys-runtime/indicator.html), [string targetOperand](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

RPG's MOVE. Moves right a character to a string.

```cs
string MoveRight(Indicator character, string targetOperand)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Indicator](/reference/runtime/qsys-runtime/indicator.html) | character | A char that represents the source of the move.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | targetOperand | targetOperand represents what is currently in the target of the move.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | returns the value of the move.

### short MoveRight([Indicator character](/reference/runtime/qsys-runtime/indicator.html), [short targetOperand](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVE. Moves right a character to a short.

```cs
short MoveRight(Indicator character, short targetOperand)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Indicator](/reference/runtime/qsys-runtime/indicator.html) | character | A char that represents the source of the move.
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | targetOperand | targetOperand represents what is currently in the target of the move.

#### Returns

| Type | Description
| --- | ---
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | returns the value of the move.

### int MoveRight([Indicator character](/reference/runtime/qsys-runtime/indicator.html), [int targetOperand](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVE. Moves right a character to an int.

```cs
int MoveRight(Indicator character, int targetOperand)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Indicator](/reference/runtime/qsys-runtime/indicator.html) | character | A char that represents the source of the move.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetOperand | targetOperand represents what is currently in the target of the move.

#### Returns

| Type | Description
| --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | returns the value of the move.

### long MoveRight([Indicator character](/reference/runtime/qsys-runtime/indicator.html), [long targetOperand](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVE. Moves right a character to a long.

```cs
long MoveRight(Indicator character, long targetOperand)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Indicator](/reference/runtime/qsys-runtime/indicator.html) | character | A char that represents the source of the move.
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | targetOperand | targetOperand represents what is currently in the target of the move.

#### Returns

| Type | Description
| --- | ---
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | returns the value of the move.

### char MoveRightToChar([Indicator character](/reference/runtime/qsys-runtime/indicator.html))

RPG's MOVE. Moves right a character to a character.

```cs
char MoveRightToChar(Indicator character)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Indicator](/reference/runtime/qsys-runtime/indicator.html) | character | A char that represents the source of the move.

#### Returns

| Type | Description
| --- | ---
| [Char](https://docs.microsoft.com/en-us/dotnet/api/system.char) | returns the value of the move.

### string MoveRightWithPad([Indicator character](/reference/runtime/qsys-runtime/indicator.html), [string targetOperand](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

RPG's MOVE. Moves right a character to a string with pad.

```cs
string MoveRightWithPad(Indicator character, string targetOperand)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Indicator](/reference/runtime/qsys-runtime/indicator.html) | character | A char that represents the source of the move.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | targetOperand | targetOperand represents what is currently in the target of the move.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | returns the value of the move.

### short MoveRightWithPad([Indicator character](/reference/runtime/qsys-runtime/indicator.html), [short targetOperand](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVE. Moves right a character to a short with pad.

```cs
short MoveRightWithPad(Indicator character, short targetOperand)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Indicator](/reference/runtime/qsys-runtime/indicator.html) | character | A char that represents the source of the move.
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | targetOperand | targetOperand represents what is currently in the target of the move.

#### Returns

| Type | Description
| --- | ---
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | returns the value of the move.

### int MoveRightWithPad([Indicator character](/reference/runtime/qsys-runtime/indicator.html), [int targetOperand](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVE. Moves right a character to a int with pad.

```cs
int MoveRightWithPad(Indicator character, int targetOperand)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Indicator](/reference/runtime/qsys-runtime/indicator.html) | character | A char that represents the source of the move.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetOperand | targetOperand represents what is currently in the target of the move.

#### Returns

| Type | Description
| --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | returns the value of the move.

### long MoveRightWithPad([Indicator character](/reference/runtime/qsys-runtime/indicator.html), [long targetOperand](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVE. Moves right a character to a long with pad.

```cs
long MoveRightWithPad(Indicator character, long targetOperand)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Indicator](/reference/runtime/qsys-runtime/indicator.html) | character | A char that represents the source of the move.
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | targetOperand | targetOperand represents what is currently in the target of the move.

#### Returns

| Type | Description
| --- | ---
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | returns the value of the move.

### bool TestTime([string num](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [DateTimeDataKind kind](/reference/runtime/qsys-runtime/date-time-data-kind.html), [DateTimeFormat format](/reference/datagate/datagate-common/date-time-format.html), [DateTimeSeparator separator](/reference/runtime/qsys-runtime/date-time-separator.html))

Tests whether a string containing a number represents a valid date/time/timestamp value. 

```cs
bool TestTime(string num, DateTimeDataKind kind, DateTimeFormat format, DateTimeSeparator separator)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | num | The string to test.
| [DateTimeDataKind](/reference/runtime/qsys-runtime/date-time-data-kind.html) | kind | whether the string represents a date, time, or timestamp.
| [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html) | format | The date/time/timestamp format in which the string is.
| [DateTimeSeparator](/reference/runtime/qsys-runtime/date-time-separator.html) | separator | The date/time separator.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | True if the string contains a valid representation of a date/time/timestamp value in the given kind, format, and separator. False otherwise.
