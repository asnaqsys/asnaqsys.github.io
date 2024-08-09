---
title: "EditCode class                | QSYS API Reference Guide"
description: "Provides methods for applying and manipulating edit codes, which define output formatting patterns for business numeric data. "
last_modified_at: 2024-08-09T17:25:29Z
---

Provides methods for applying and manipulating edit codes, which define output formatting patterns for business numeric data.

**Namespace:** ASNA.QSys.Runtime
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>

## Methods

| Signature | Description |
| --- | --- |
| [Apply](#string-applydecimal-numeric-int-decimals-int-length-editcodes-editcode-int-isasteriskfill)([Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [EditCodes](/reference/expo/qsys-expo-model/edit-codes.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Applies Edit Code parameters.
| [Apply](#string-applydecimal-numeric-int-decimals-int-length-editcodes-editcode-string-currencysymbol)([Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [EditCodes](/reference/expo/qsys-expo-model/edit-codes.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Applies Edit Code parameters.
| [ApplyEditCode](#string-applyeditcodeeditcodes-editcode-int-decimals-int-length-string-inputstring-char-decimalpoint-char-thousandseparator-char-currencysymbol-bool-isasteriskfill)([EditCodes](/reference/expo/qsys-expo-model/edit-codes.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Char](https://docs.microsoft.com/en-us/dotnet/api/system.char), [Char](https://docs.microsoft.com/en-us/dotnet/api/system.char), [Char](https://docs.microsoft.com/en-us/dotnet/api/system.char), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Applies Edit Code.
| [GetEditCodeEnumFromChar](#editcodes-geteditcodeenumfromcharchar-editcode)([Char](https://docs.microsoft.com/en-us/dotnet/api/system.char)) | Get EditCode enumeration member from input char.
| [UsesThousandsSeparator](#bool-usesthousandsseparatoreditcodes-editcode)([EditCodes](/reference/expo/qsys-expo-model/edit-codes.html)) | Determines if Edit Code uses thousands separator symbol.

### string Apply([decimal numeric](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [int decimals](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int length](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [EditCodes editCode](/reference/expo/qsys-expo-model/edit-codes.html), [int isAsteriskFill](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Applies Edit Code parameters.

```cs
string Apply(decimal numeric, int decimals, int length, EditCodes editCode, int isAsteriskFill)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | numeric | Numeric input value.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | decimals | Number of decimals.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | length | Fixed length.
| [EditCodes](/reference/expo/qsys-expo-model/edit-codes.html) | editCode | Edit Code.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | isAsteriskFill | True if value should be filled with asterisks, false otherwise.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | Formatted value as string.

### string Apply([decimal numeric](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [int decimals](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int length](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [EditCodes editCode](/reference/expo/qsys-expo-model/edit-codes.html), [string currencySymbol](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Applies Edit Code parameters.

```cs
string Apply(decimal numeric, int decimals, int length, EditCodes editCode, string currencySymbol)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | numeric | Numeric input value.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | decimals | Number of decimals.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | length | Fixed length.
| [EditCodes](/reference/expo/qsys-expo-model/edit-codes.html) | editCode | Edit Code.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | currencySymbol | Currency symbol.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | Formatted value as string.

### string ApplyEditCode([EditCodes editCode](/reference/expo/qsys-expo-model/edit-codes.html), [int decimals](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int length](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [string inputString](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [char decimalPoint](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/char), [char thousandSeparator](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/char), [char currencySymbol](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/char), [bool isAsteriskFill](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Applies Edit Code.

```cs
string ApplyEditCode(EditCodes editCode, int decimals, int length, string inputString, char decimalPoint, char thousandSeparator, char currencySymbol, bool isAsteriskFill)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [EditCodes](/reference/expo/qsys-expo-model/edit-codes.html) | editCode | Edit Code.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | decimals | Number of decimals.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | length | Fixed length.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | inputString | Input string.
| [Char](https://docs.microsoft.com/en-us/dotnet/api/system.char) | decimalPoint | Decimal point symbol.
| [Char](https://docs.microsoft.com/en-us/dotnet/api/system.char) | thousandSeparator | Thousands separator symbol.
| [Char](https://docs.microsoft.com/en-us/dotnet/api/system.char) | currencySymbol | Currency symbol.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | isAsteriskFill | True if value should be filled with asterisks, false otherwise.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | Formatted value as string.

### EditCodes GetEditCodeEnumFromChar([char editCode](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/char))

Get EditCode enumeration member from input char.

```cs
EditCodes GetEditCodeEnumFromChar(char editCode)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Char](https://docs.microsoft.com/en-us/dotnet/api/system.char) | editCode | Edit code char.

#### Returns

| Type | Description
| --- | ---
| [EditCodes](/reference/expo/qsys-expo-model/edit-codes.html) | Edit Codes enumeration member.

### bool UsesThousandsSeparator([EditCodes editCode](/reference/expo/qsys-expo-model/edit-codes.html))

Determines if Edit Code uses thousands separator symbol.

```cs
bool UsesThousandsSeparator(EditCodes editCode)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [EditCodes](/reference/expo/qsys-expo-model/edit-codes.html) | editCode | Edit code input.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | true if Edit Code uses thousands separator, false otherwise.
