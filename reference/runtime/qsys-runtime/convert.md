---
title: "Convert class                 | QSYS API Reference Guide"
description: "Converts a base data type to another base data type, using RPG type conversion rules. "
last_modified_at: 2024-08-09T17:25:29Z
---

Converts a base data type to another base data type, using RPG type conversion rules.

**Namespace:** ASNA.QSys.Runtime
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>

## Methods

| Signature | Description |
| --- | --- |
| [ToByte](#byte-tobytestring-thestring)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Converts the value of the specified string to an equivalent byte value, using RPG type conversion rules.
| [ToDecimal](#decimal-todecimalstring-thestring)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Converts the specified string representation of a number to an equivalent decimal number.
| [ToDouble](#double-todoublestring-thestring)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Converts the specified string representation of a number to an equivalent double-precision floating-point number.
| [ToInt16](#short-toint16decimal-thedecimal)([Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal)) | Converts the value of the specified decimal number to an equivalent 16-bit signed integer, using RPG type conversion rules.
| [ToInt16](#short-toint16string-thestring)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Converts the value of the specified string to an equivalent 16-bit signed integer, using RPG type conversion rules.
| [ToInt32](#int-toint32decimal-thedecimal)([Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal)) | Converts the value of the specified decimal number to an equivalent 32-bit signed integer, using RPG type conversion rules.
| [ToInt32](#int-toint32string-thestring)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Converts the value of the specified string to an equivalent 32-bit signed integer, using RPG type conversion rules.
| [ToInt64](#long-toint64string-thestring)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Converts the value of the specified string to an equivalent 64-bit signed integer, using RPG type conversion rules.
| [ToSingle](#float-tosinglestring-thestring)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Converts the specified string representation of a number to an equivalent single-precision floating-point number.

### byte ToByte([string theString](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Converts the value of the specified string to an equivalent byte value, using RPG type conversion rules.

```cs
byte ToByte(string theString)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | theString | The string to convert.

#### Returns

| Type | Description
| --- | ---
| [Byte](https://docs.microsoft.com/en-us/dotnet/api/system.byte) | The resulting byte value, or 0 (zero) if the string is null or blanks.

### decimal ToDecimal([string theString](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Converts the specified string representation of a number to an equivalent decimal number.

```cs
decimal ToDecimal(string theString)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | theString | A string that contains a number to convert.

#### Returns

| Type | Description
| --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | A decimal number that is equivalent to the number in value, or 0 (zero) if value is null or blanks.

### double ToDouble([string theString](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Converts the specified string representation of a number to an equivalent double-precision floating-point number.

```cs
double ToDouble(string theString)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | theString | A string that contains the number to convert.

#### Returns

| Type | Description
| --- | ---
| [Double](https://learn.microsoft.com/en-us/dotnet/api/system.double?view=net-8.0) | A double-precision floating-point number that is equivalent to the number in value, or 0 (zero) if value is null or blanks.

### short ToInt16([decimal theDecimal](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types))

Converts the value of the specified decimal number to an equivalent 16-bit signed integer, using RPG type conversion rules.

```cs
short ToInt16(decimal theDecimal)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | theDecimal | The decimal number to convert.

#### Returns

| Type | Description
| --- | ---
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | The resulting 16-bit signed integer.

### short ToInt16([string theString](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Converts the value of the specified string to an equivalent 16-bit signed integer, using RPG type conversion rules.

```cs
short ToInt16(string theString)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | theString | The string to convert.

#### Returns

| Type | Description
| --- | ---
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | The resulting 16-bit signed integer, or 0 (zero) if value is null or blanks.

### int ToInt32([decimal theDecimal](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types))

Converts the value of the specified decimal number to an equivalent 32-bit signed integer, using RPG type conversion rules.

```cs
int ToInt32(decimal theDecimal)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | theDecimal | The decimal number to convert.

#### Returns

| Type | Description
| --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | The resulting 32-bit signed integer.

### int ToInt32([string theString](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Converts the value of the specified string to an equivalent 32-bit signed integer, using RPG type conversion rules.

```cs
int ToInt32(string theString)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | theString | The string to convert.

#### Returns

| Type | Description
| --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | The resulting 32-bit signed integer, or 0 (zero) if value is null or blanks.

### long ToInt64([string theString](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Converts the value of the specified string to an equivalent 64-bit signed integer, using RPG type conversion rules.

```cs
long ToInt64(string theString)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | theString | The string to convert.

#### Returns

| Type | Description
| --- | ---
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | The resulting 64-bit signed integer, or 0 (zero) if value is null or blanks.

### float ToSingle([string theString](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Converts the specified string representation of a number to an equivalent single-precision floating-point number.

```cs
float ToSingle(string theString)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | theString | A string that contains the number to convert.

#### Returns

| Type | Description
| --- | ---
| [Single](https://learn.microsoft.com/en-us/dotnet/api/system.single?view=net-8.0) | A single-precision floating-point number that is equivalent to the number in value, or 0 (zero) if value is null or blanks.
