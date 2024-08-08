---
title: "GetObject class               | QSYS API Reference Guide"
description: "Class that contains methods to construct certain RPG objects. "
last_modified_at: 2024-08-08T21:41:46Z
---

Class that contains methods to construct certain RPG objects.

**Namespace:** ASNA.QSys.Runtime
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>

## Methods

| Signature | Description |
| --- | --- |
| [MaxFixedDecimalValue](#decimal-maxfixeddecimalvalueint-length-int-decimals)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's *HIVAL. Create a fixed decimal high value for the length and decimal positions given.
| [MinFixedDecimalValue](#decimal-minfixeddecimalvalueint-length-int-decimals)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's *LOVAL. Create a fixed decimal low value for the length and decimal positions given.
| [NewIndicatorArray](#array-newindicatorarrayint32--dimensions)([Int32\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Creates a new array of characters initialized to '0'
| [NewStringArray](#array-newstringarrayint32--dimensions-int-length)([Int32\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Creates a new array of fixed-length strings initialized to a string of blanks.
| [RepeatAndMakeInt](#int-repeatandmakeintstring-pattern)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | RPG's *ALL. Creates an integer by repeating the digits in the pattern multiple times.
| [RepeatAndMakeLong](#long-repeatandmakelongstring-pattern)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | RPG's *ALL. Creates a long by repeating the digits in the pattern multiple times.
| [RepeatAndMakeShort](#short-repeatandmakeshortstring-pattern)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | RPG's *ALL. Creates a short by repeating the digits in the pattern multiple times.
| [RepeatDecimals](#decimal-repeatdecimalsstring-pattern-int-digits-int-decimals)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's *ALL. Creates a decimal number by repeating the digits in the pattern multiple times.
| [RepeatString](#string-repeatstringstring-pattern-int-length)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's *ALL. Creates a string of the indicated length by repeating the pattern multiple times.

### decimal MaxFixedDecimalValue([int length](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int decimals](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's *HIVAL. Create a fixed decimal high value for the length and decimal positions given.

```cs
decimal MaxFixedDecimalValue(int length, int decimals)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | length | Desired length of the decimal number.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | decimals | Number of desired decimal positions.

#### Returns

| Type | Description
| --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | The *HIVAL decimal number of the proper size.

### decimal MinFixedDecimalValue([int length](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int decimals](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's *LOVAL. Create a fixed decimal low value for the length and decimal positions given.

```cs
decimal MinFixedDecimalValue(int length, int decimals)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | length | Desired length of the decimal number.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | decimals | Number of desired decimal positions.

#### Returns

| Type | Description
| --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | The *LOVAL decimal number of the proper size.

### Array NewIndicatorArray([Int32\[\] dimensions](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

Creates a new array of characters initialized to '0'

```cs
Array NewIndicatorArray(Int32[] dimensions)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | dimensions | Array dimensions.

#### Returns

| Type | Description
| --- | ---
| [Array](https://learn.microsoft.com/en-us/dotnet/api/system.array?view=net-8.0) | The array of indicators.

### Array NewStringArray([Int32\[\] dimensions](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [int length](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Creates a new array of fixed-length strings initialized to a string of blanks.

```cs
Array NewStringArray(Int32[] dimensions, int length)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | dimensions | Array dimensions.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | length | Length of the strings in the array.

#### Returns

| Type | Description
| --- | ---
| [Array](https://learn.microsoft.com/en-us/dotnet/api/system.array?view=net-8.0) | The array of fixed-length strings.

### int RepeatAndMakeInt([string pattern](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

RPG's *ALL. Creates an integer by repeating the digits in the pattern multiple times.

```cs
int RepeatAndMakeInt(string pattern)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | pattern | The repeating pattern.

#### Returns

| Type | Description
| --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | The largest integer number that can be formed repeating the pattern of digits.

### long RepeatAndMakeLong([string pattern](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

RPG's *ALL. Creates a long by repeating the digits in the pattern multiple times.

```cs
long RepeatAndMakeLong(string pattern)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | pattern | The repeating pattern.

#### Returns

| Type | Description
| --- | ---
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | The largest long number that can be formed repeating the pattern of digits.

### short RepeatAndMakeShort([string pattern](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

RPG's *ALL. Creates a short by repeating the digits in the pattern multiple times.

```cs
short RepeatAndMakeShort(string pattern)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | pattern | The repeating pattern.

#### Returns

| Type | Description
| --- | ---
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | The largest short number that can be formed repeating the pattern of digits.

### decimal RepeatDecimals([string pattern](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [int digits](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int decimals](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's *ALL. Creates a decimal number by repeating the digits in the pattern multiple times.

```cs
decimal RepeatDecimals(string pattern, int digits, int decimals)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | pattern | The repeating pattern.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | digits | The length of the resulting decimal number.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | decimals | The decimal positions of the result.

#### Returns

| Type | Description
| --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | The decimal number with the repeating digit pattern in the proper length.

### string RepeatString([string pattern](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [int length](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's *ALL. Creates a string of the indicated length by repeating the pattern multiple times.

```cs
string RepeatString(string pattern, int length)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | pattern | The repeating pattern.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | length | The desired string length.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The string with the repeating pattern, of the proper length.
