---
title: "CharacterMethods class        | QSYS API Reference Guide"
description: "Contains extension methods for Char (onechar/indicator) conversions. "
last_modified_at: 2024-08-09T17:25:29Z
---

Contains extension methods for Char (onechar/indicator) conversions.

**Namespace:** ASNA.QSys.Runtime
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>

## Methods

| Signature | Description |
| --- | --- |
| [MoveLeft](#decimal-moveleftchar-character-decimal-targetoperand-int-targetoperanddig-int-targetoperanddec)([Char](https://docs.microsoft.com/en-us/dotnet/api/system.char), [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's MOVEL. Moves left a character to a decimal.
| [MoveLeft](#string-moveleftchar-character-string-targetoperand)([Char](https://docs.microsoft.com/en-us/dotnet/api/system.char), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | RPG's MOVEL. Moves left a character to a string with pad.
| [MoveLeft](#short-moveleftchar-character-short-targetoperand)([Char](https://docs.microsoft.com/en-us/dotnet/api/system.char), [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16)) | RPG's MOVEL. Moves left a character to a short.
| [MoveLeft](#int-moveleftchar-character-int-targetoperand)([Char](https://docs.microsoft.com/en-us/dotnet/api/system.char), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's MOVEL. Moves left a character to an int.
| [MoveLeft](#long-moveleftchar-character-long-targetoperand)([Char](https://docs.microsoft.com/en-us/dotnet/api/system.char), [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64)) | RPG's MOVEL. Moves left a character to a long.
| [MoveLeftToChar](#char-movelefttocharchar-character)([Char](https://docs.microsoft.com/en-us/dotnet/api/system.char)) | RPG's MOVEL. Moves left a character to a character.
| [MoveLeftWithPad](#decimal-moveleftwithpadchar-character-decimal-targetoperand-int-targetoperanddig-int-targetoperanddec)([Char](https://docs.microsoft.com/en-us/dotnet/api/system.char), [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's MOVEL. Moves left a character to a decimal with pad.
| [MoveLeftWithPad](#string-moveleftwithpadchar-character-string-targetoperand)([Char](https://docs.microsoft.com/en-us/dotnet/api/system.char), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | RPG's MOVEL. Moves left a character to a string with pad.
| [MoveLeftWithPad](#short-moveleftwithpadchar-character-short-targetoperand)([Char](https://docs.microsoft.com/en-us/dotnet/api/system.char), [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16)) | RPG's MOVEL. Moves left a character to a short with pad.
| [MoveLeftWithPad](#int-moveleftwithpadchar-character-int-targetoperand)([Char](https://docs.microsoft.com/en-us/dotnet/api/system.char), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's MOVEL. Moves left a character to an int with pad.
| [MoveLeftWithPad](#long-moveleftwithpadchar-character-long-targetoperand)([Char](https://docs.microsoft.com/en-us/dotnet/api/system.char), [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64)) | RPG's MOVE. Moves right a character to a long with pad.
| [MoveRight](#decimal-moverightchar-character-decimal-targetoperand-int-targetoperanddig-int-targetoperanddec)([Char](https://docs.microsoft.com/en-us/dotnet/api/system.char), [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's MOVE. Moves right a character to a decimal.
| [MoveRight](#string-moverightchar-character-string-targetoperand)([Char](https://docs.microsoft.com/en-us/dotnet/api/system.char), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | RPG's MOVE. Moves right a character to a string.
| [MoveRight](#short-moverightchar-character-short-targetoperand)([Char](https://docs.microsoft.com/en-us/dotnet/api/system.char), [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16)) | RPG's MOVE. Moves right a character to a short.
| [MoveRight](#int-moverightchar-character-int-targetoperand)([Char](https://docs.microsoft.com/en-us/dotnet/api/system.char), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's MOVE. Moves right a character to an int.
| [MoveRight](#long-moverightchar-character-long-targetoperand)([Char](https://docs.microsoft.com/en-us/dotnet/api/system.char), [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64)) | RPG's MOVE. Moves right a character to a long.
| [MoveRightToChar](#char-moverighttocharchar-character)([Char](https://docs.microsoft.com/en-us/dotnet/api/system.char)) | RPG's MOVE. Moves right a character to a character.
| [MoveRightWithPad](#decimal-moverightwithpadchar-character-decimal-targetoperand-int-targetoperanddig-int-targetoperanddec)([Char](https://docs.microsoft.com/en-us/dotnet/api/system.char), [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's MOVE. Moves right a character to a decimal with pad.
| [MoveRightWithPad](#string-moverightwithpadchar-character-string-targetoperand)([Char](https://docs.microsoft.com/en-us/dotnet/api/system.char), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | RPG's MOVE. Moves right a character to a string with pad.
| [MoveRightWithPad](#short-moverightwithpadchar-character-short-targetoperand)([Char](https://docs.microsoft.com/en-us/dotnet/api/system.char), [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16)) | RPG's MOVE. Moves right a character to a short with pad.
| [MoveRightWithPad](#int-moverightwithpadchar-character-int-targetoperand)([Char](https://docs.microsoft.com/en-us/dotnet/api/system.char), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's MOVE. Moves right a character to a int with pad.
| [MoveRightWithPad](#long-moverightwithpadchar-character-long-targetoperand)([Char](https://docs.microsoft.com/en-us/dotnet/api/system.char), [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64)) | RPG's MOVE. Moves right a character to a long with pad.
| [TestTime](#bool-testtimestring-num-datetimedatakind-kind-datetimeformat-format-datetimeseparator-separator)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [DateTimeDataKind](/reference/runtime/qsys-runtime/date-time-data-kind.html), [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html), [DateTimeSeparator](/reference/runtime/qsys-runtime/date-time-separator.html)) | Tests whether a string value represents a valid date/time/timestamp value. 

### decimal MoveLeft([char character](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/char), [decimal targetOperand](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [int targetOperandDig](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int targetOperandDec](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVEL. Moves left a character to a decimal.

```cs
decimal MoveLeft(char character, decimal targetOperand, int targetOperandDig, int targetOperandDec)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Char](https://docs.microsoft.com/en-us/dotnet/api/system.char) | character | A char that represents the source of the move.
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | targetOperand | targetOperand represents what is currently in the target of the move.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetOperandDig | number of digits in the targetOperand.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetOperandDec | number of decimal places.

#### Returns

| Type | Description
| --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | Returns the value of the move.

### string MoveLeft([char character](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/char), [string targetOperand](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

RPG's MOVEL. Moves left a character to a string with pad.

```cs
string MoveLeft(char character, string targetOperand)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Char](https://docs.microsoft.com/en-us/dotnet/api/system.char) | character | A char that represents the source of the move.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | targetOperand | targetOperand represents what is currently in the target of the move.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | Returns the value of the move.

### short MoveLeft([char character](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/char), [short targetOperand](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVEL. Moves left a character to a short.

```cs
short MoveLeft(char character, short targetOperand)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Char](https://docs.microsoft.com/en-us/dotnet/api/system.char) | character | A char that represents the source of the move.
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | targetOperand | targetOperand represents what is currently in the target of the move.

#### Returns

| Type | Description
| --- | ---
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | Returns the value of the move.

### int MoveLeft([char character](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/char), [int targetOperand](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVEL. Moves left a character to an int.

```cs
int MoveLeft(char character, int targetOperand)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Char](https://docs.microsoft.com/en-us/dotnet/api/system.char) | character | A char that represents the source of the move.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetOperand | targetOperand represents what is currently in the target of the move.

#### Returns

| Type | Description
| --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | Returns the value of the move.

### long MoveLeft([char character](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/char), [long targetOperand](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVEL. Moves left a character to a long.

```cs
long MoveLeft(char character, long targetOperand)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Char](https://docs.microsoft.com/en-us/dotnet/api/system.char) | character | A char that represents the source of the move.
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | targetOperand | targetOperand represents what is currently in the target of the move.

#### Returns

| Type | Description
| --- | ---
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | Returns the value of the move.

### char MoveLeftToChar([char character](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/char))

RPG's MOVEL. Moves left a character to a character.

```cs
char MoveLeftToChar(char character)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Char](https://docs.microsoft.com/en-us/dotnet/api/system.char) | character | A char that represents the source of the move.

#### Returns

| Type | Description
| --- | ---
| [Char](https://docs.microsoft.com/en-us/dotnet/api/system.char) | Returns the value of the move.

### decimal MoveLeftWithPad([char character](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/char), [decimal targetOperand](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [int targetOperandDig](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int targetOperandDec](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVEL. Moves left a character to a decimal with pad.

```cs
decimal MoveLeftWithPad(char character, decimal targetOperand, int targetOperandDig, int targetOperandDec)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Char](https://docs.microsoft.com/en-us/dotnet/api/system.char) | character | A char that represents the source of the move.
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | targetOperand | targetOperand represents what is currently in the target of the move.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetOperandDig | number of digits in the targetOperand.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetOperandDec | number of decimal places.

#### Returns

| Type | Description
| --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | Returns the value of the move.

### string MoveLeftWithPad([char character](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/char), [string targetOperand](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

RPG's MOVEL. Moves left a character to a string with pad.

```cs
string MoveLeftWithPad(char character, string targetOperand)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Char](https://docs.microsoft.com/en-us/dotnet/api/system.char) | character | A char that represents the source of the move.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | targetOperand | targetOperand represents what is currently in the target of the move.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | Returns the value of the move.

### short MoveLeftWithPad([char character](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/char), [short targetOperand](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVEL. Moves left a character to a short with pad.

```cs
short MoveLeftWithPad(char character, short targetOperand)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Char](https://docs.microsoft.com/en-us/dotnet/api/system.char) | character | A char that represents the source of the move.
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | targetOperand | targetOperand represents what is currently in the target of the move.

#### Returns

| Type | Description
| --- | ---
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | Returns the value of the move.

### int MoveLeftWithPad([char character](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/char), [int targetOperand](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVEL. Moves left a character to an int with pad.

```cs
int MoveLeftWithPad(char character, int targetOperand)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Char](https://docs.microsoft.com/en-us/dotnet/api/system.char) | character | A char that represents the source of the move.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetOperand | targetOperand represents what is currently in the target of the move.

#### Returns

| Type | Description
| --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | Returns the value of the move.

### long MoveLeftWithPad([char character](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/char), [long targetOperand](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVE. Moves right a character to a long with pad.

```cs
long MoveLeftWithPad(char character, long targetOperand)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Char](https://docs.microsoft.com/en-us/dotnet/api/system.char) | character | A char that represents the source of the move.
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | targetOperand | targetOperand represents what is currently in the target of the move.

#### Returns

| Type | Description
| --- | ---
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | Returns the value of the move.

### decimal MoveRight([char character](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/char), [decimal targetOperand](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [int targetOperandDig](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int targetOperandDec](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVE. Moves right a character to a decimal.

```cs
decimal MoveRight(char character, decimal targetOperand, int targetOperandDig, int targetOperandDec)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Char](https://docs.microsoft.com/en-us/dotnet/api/system.char) | character | A char that represents the source of the move.
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | targetOperand | targetOperand represents what is currently in the target of the move.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetOperandDig | number of digits in the targetOperand.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetOperandDec | number of decimal places.

#### Returns

| Type | Description
| --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | Returns the value of the move.

### string MoveRight([char character](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/char), [string targetOperand](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

RPG's MOVE. Moves right a character to a string.

```cs
string MoveRight(char character, string targetOperand)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Char](https://docs.microsoft.com/en-us/dotnet/api/system.char) | character | A char that represents the source of the move.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | targetOperand | targetOperand represents what is currently in the target of the move.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | Returns the value of the move.

### short MoveRight([char character](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/char), [short targetOperand](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVE. Moves right a character to a short.

```cs
short MoveRight(char character, short targetOperand)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Char](https://docs.microsoft.com/en-us/dotnet/api/system.char) | character | A char that represents the source of the move.
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | targetOperand | targetOperand represents what is currently in the target of the move.

#### Returns

| Type | Description
| --- | ---
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | Returns the value of the move.

### int MoveRight([char character](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/char), [int targetOperand](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVE. Moves right a character to an int.

```cs
int MoveRight(char character, int targetOperand)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Char](https://docs.microsoft.com/en-us/dotnet/api/system.char) | character | A char that represents the source of the move.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetOperand | targetOperand represents what is currently in the target of the move.

#### Returns

| Type | Description
| --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | Returns the value of the move.

### long MoveRight([char character](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/char), [long targetOperand](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVE. Moves right a character to a long.

```cs
long MoveRight(char character, long targetOperand)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Char](https://docs.microsoft.com/en-us/dotnet/api/system.char) | character | A char that represents the source of the move.
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | targetOperand | targetOperand represents what is currently in the target of the move.

#### Returns

| Type | Description
| --- | ---
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | Returns the value of the move.

### char MoveRightToChar([char character](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/char))

RPG's MOVE. Moves right a character to a character.

```cs
char MoveRightToChar(char character)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Char](https://docs.microsoft.com/en-us/dotnet/api/system.char) | character | A char that represents the source of the move.

#### Returns

| Type | Description
| --- | ---
| [Char](https://docs.microsoft.com/en-us/dotnet/api/system.char) | Returns the value of the move.

### decimal MoveRightWithPad([char character](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/char), [decimal targetOperand](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [int targetOperandDig](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int targetOperandDec](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVE. Moves right a character to a decimal with pad.

```cs
decimal MoveRightWithPad(char character, decimal targetOperand, int targetOperandDig, int targetOperandDec)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Char](https://docs.microsoft.com/en-us/dotnet/api/system.char) | character | A char that represents the source of the move.
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | targetOperand | targetOperand represents what is currently in the target of the move.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetOperandDig | number of digits in the targetOperand.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetOperandDec | number of decimal places.

#### Returns

| Type | Description
| --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | Returns the value of the move.

### string MoveRightWithPad([char character](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/char), [string targetOperand](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

RPG's MOVE. Moves right a character to a string with pad.

```cs
string MoveRightWithPad(char character, string targetOperand)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Char](https://docs.microsoft.com/en-us/dotnet/api/system.char) | character | A char that represents the source of the move.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | targetOperand | targetOperand represents what is currently in the target of the move.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | Returns the value of the move.

### short MoveRightWithPad([char character](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/char), [short targetOperand](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVE. Moves right a character to a short with pad.

```cs
short MoveRightWithPad(char character, short targetOperand)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Char](https://docs.microsoft.com/en-us/dotnet/api/system.char) | character | A char that represents the source of the move.
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | targetOperand | targetOperand represents what is currently in the target of the move.

#### Returns

| Type | Description
| --- | ---
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | Returns the value of the move.

### int MoveRightWithPad([char character](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/char), [int targetOperand](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVE. Moves right a character to a int with pad.

```cs
int MoveRightWithPad(char character, int targetOperand)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Char](https://docs.microsoft.com/en-us/dotnet/api/system.char) | character | A char that represents the source of the move.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetOperand | targetOperand represents what is currently in the target of the move.

#### Returns

| Type | Description
| --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | Returns the value of the move.

### long MoveRightWithPad([char character](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/char), [long targetOperand](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVE. Moves right a character to a long with pad.

```cs
long MoveRightWithPad(char character, long targetOperand)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Char](https://docs.microsoft.com/en-us/dotnet/api/system.char) | character | A char that represents the source of the move.
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | targetOperand | targetOperand represents what is currently in the target of the move.

#### Returns

| Type | Description
| --- | ---
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | Returns the value of the move.

### bool TestTime([string num](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [DateTimeDataKind kind](/reference/runtime/qsys-runtime/date-time-data-kind.html), [DateTimeFormat format](/reference/datagate/datagate-common/date-time-format.html), [DateTimeSeparator separator](/reference/runtime/qsys-runtime/date-time-separator.html))

Tests whether a string value represents a valid date/time/timestamp value. 

```cs
bool TestTime(string num, DateTimeDataKind kind, DateTimeFormat format, DateTimeSeparator separator)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | num | The string to test.
| [DateTimeDataKind](/reference/runtime/qsys-runtime/date-time-data-kind.html) | kind | The DateTimeDataKind value representing a test for a date, time, or timestamp.
| [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html) | format | The DateTimeFormat of the date/time/timestamp value.
| [DateTimeSeparator](/reference/runtime/qsys-runtime/date-time-separator.html) | separator | The DateTimeSeparator of the date/time/timestamp value.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | True if num represents a valid date/time/timestamp with the given format and separator.
