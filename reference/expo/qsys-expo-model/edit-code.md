---
title: "EditCode class                | QSYS API Reference Guide"
description: "Provides methods to format numeric values according to Edit Code "
last_modified_at: 2024-08-09T17:26:04Z
---

Provides methods to format numeric values according to Edit Code

**Namespace:** ASNA.QSys.Expo.Model
**Assembly:** ASNA.QSys.Expo.Model.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>

## Remarks
The formatting rules are equivalent to those supported by [IBM i Edit Codes](https://www.ibm.com/docs/en/i/7.2?topic=codes-summary-edit)


## Methods

| Signature | Description |
| --- | --- |
| [Apply](#string-applydecimal-numeric-int-decimals-int-length-editcodes-editcode-bool-isasteriskfill)([Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [EditCodes](/reference/expo/qsys-expo-model/edit-codes.html), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Gets a string value representing the given numeric value after formatting it according to an Edit Code
| [Apply](#string-applydecimal-numeric-int-decimals-int-length-editcodes-editcode-string-currencysymbol)([Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [EditCodes](/reference/expo/qsys-expo-model/edit-codes.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Gets a string value representing the given numeric value after formatting it according to an Edit Code
| [ApplyEditCode](#string-applyeditcodeeditcodes-editcode-int-decimals-int-length-string-inputstring-char-decimalpoint-char-thousandseparator-char-currencysymbol-bool-isasteriskfill)([EditCodes](/reference/expo/qsys-expo-model/edit-codes.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Char](https://docs.microsoft.com/en-us/dotnet/api/system.char), [Char](https://docs.microsoft.com/en-us/dotnet/api/system.char), [Char](https://docs.microsoft.com/en-us/dotnet/api/system.char), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Gets a string value representing the given input string after formatting the value in the string according to given Edit Code 
| [FromChar](#editcodes-fromcharchar-editcodechar)([Char](https://docs.microsoft.com/en-us/dotnet/api/system.char)) | Gets the EditCodes enumeration given a character code.
| [ToChar](#char-tochareditcodes-editcode)([EditCodes](/reference/expo/qsys-expo-model/edit-codes.html)) | Gets a char value representing the enumeration element.
| [UsesThousandsSeparator](#bool-usesthousandsseparatoreditcodes-editcode)([EditCodes](/reference/expo/qsys-expo-model/edit-codes.html)) | Gets a boolean value indicating that the given Edit Code uses thousands separator.

### string Apply([decimal numeric](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [int decimals](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int length](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [EditCodes editCode](/reference/expo/qsys-expo-model/edit-codes.html), [bool isAsteriskFill](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Gets a string value representing the given numeric value after formatting it according to an Edit Code

```cs
string Apply(decimal numeric, int decimals, int length, EditCodes editCode, bool isAsteriskFill)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | numeric | input numeric value
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | decimals | field decimal positions
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | length | field length
| [EditCodes](/reference/expo/qsys-expo-model/edit-codes.html) | editCode | Edit Code
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | isAsteriskFill | true if value should be filled with *

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | the formatted value as string

### string Apply([decimal numeric](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [int decimals](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int length](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [EditCodes editCode](/reference/expo/qsys-expo-model/edit-codes.html), [string currencySymbol](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Gets a string value representing the given numeric value after formatting it according to an Edit Code

```cs
string Apply(decimal numeric, int decimals, int length, EditCodes editCode, string currencySymbol)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | numeric | input numeric value
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | decimals | field decimal positions
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | length | field length
| [EditCodes](/reference/expo/qsys-expo-model/edit-codes.html) | editCode | Edit Code
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | currencySymbol | currency symbol

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | the formatted value as string

### string ApplyEditCode([EditCodes editCode](/reference/expo/qsys-expo-model/edit-codes.html), [int decimals](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int length](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [string inputString](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [char decimalPoint](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/char), [char thousandSeparator](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/char), [char currencySymbol](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/char), [bool isAsteriskFill](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Gets a string value representing the given input string after formatting the value in the string according to given Edit Code 

```cs
string ApplyEditCode(EditCodes editCode, int decimals, int length, string inputString, char decimalPoint, char thousandSeparator, char currencySymbol, bool isAsteriskFill)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [EditCodes](/reference/expo/qsys-expo-model/edit-codes.html) | editCode | Edit Code
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | decimals | field decimal positions
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | length | field length
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | inputString | input numeric value in a string
| [Char](https://docs.microsoft.com/en-us/dotnet/api/system.char) | decimalPoint | decimal point symbol
| [Char](https://docs.microsoft.com/en-us/dotnet/api/system.char) | thousandSeparator | thousands separator symbol
| [Char](https://docs.microsoft.com/en-us/dotnet/api/system.char) | currencySymbol | currency symbol
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | isAsteriskFill | true if value should be filled with *

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | the formatted value as string

### EditCodes FromChar([char editCodeChar](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/char))

Gets the EditCodes enumeration given a character code.

```cs
EditCodes FromChar(char editCodeChar)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Char](https://docs.microsoft.com/en-us/dotnet/api/system.char) | editCodeChar | input char

#### Returns

| Type | Description
| --- | ---
| [EditCodes](/reference/expo/qsys-expo-model/edit-codes.html) | the enumeration

### char ToChar([EditCodes editCode](/reference/expo/qsys-expo-model/edit-codes.html))

Gets a char value representing the enumeration element.

```cs
char ToChar(EditCodes editCode)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [EditCodes](/reference/expo/qsys-expo-model/edit-codes.html) | editCode | input Edit code

#### Returns

| Type | Description
| --- | ---
| [Char](https://docs.microsoft.com/en-us/dotnet/api/system.char) | the char code

### bool UsesThousandsSeparator([EditCodes editCode](/reference/expo/qsys-expo-model/edit-codes.html))

Gets a boolean value indicating that the given Edit Code uses thousands separator.

```cs
bool UsesThousandsSeparator(EditCodes editCode)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [EditCodes](/reference/expo/qsys-expo-model/edit-codes.html) | editCode | inpu Edit Code

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | true if editCode uses thousands separator
