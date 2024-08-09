---
title: "EditWord class                | QSYS API Reference Guide"
description: "Provides methods for applying edit word parameters to numeric values, including formatting and manipulating the output string based on specified patte"
last_modified_at: 2024-08-09T17:25:29Z
---

Provides methods for applying edit word parameters to numeric values, including formatting and manipulating the output string based on specified patterns.

**Namespace:** ASNA.QSys.Runtime
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>

## Methods

| Signature | Description |
| --- | --- |
| [Apply](#string-applydecimal-numeric-int-decimals-int-length-string-editwordstring)([Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Applies Edit Word parameters.
| [ApplyEditWord](#string-applyeditwordstring-editwordstring-string-valuestring-char-decimalpoint-char-thousandseparator-char-currencysymbol-bool-printcurrencysymbol-bool-isfloatcurrencysymbol)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Char](https://docs.microsoft.com/en-us/dotnet/api/system.char), [Char](https://docs.microsoft.com/en-us/dotnet/api/system.char), [Char](https://docs.microsoft.com/en-us/dotnet/api/system.char), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Applies Edit Word.

### string Apply([decimal numeric](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [int decimals](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int length](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [string editwordString](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Applies Edit Word parameters.

```cs
string Apply(decimal numeric, int decimals, int length, string editwordString)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | numeric | Input numeric value.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | decimals | Input number of decimals.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | length | Input length
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | editwordString | EditWord string.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | Formatted value as string.

### string ApplyEditWord([string editwordString](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string valueString](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [char decimalPoint](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/char), [char thousandSeparator](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/char), [char currencySymbol](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/char), [bool printCurrencySymbol](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [bool isFloatCurrencySymbol](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Applies Edit Word.

```cs
string ApplyEditWord(string editwordString, string valueString, char decimalPoint, char thousandSeparator, char currencySymbol, bool printCurrencySymbol, bool isFloatCurrencySymbol)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | editwordString | Edit Word.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | valueString | Value.
| [Char](https://docs.microsoft.com/en-us/dotnet/api/system.char) | decimalPoint | Decimal point symbol.
| [Char](https://docs.microsoft.com/en-us/dotnet/api/system.char) | thousandSeparator | Thousands separator symbol.
| [Char](https://docs.microsoft.com/en-us/dotnet/api/system.char) | currencySymbol | Currency symbol.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | printCurrencySymbol | Print currency symbol.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | isFloatCurrencySymbol | (Not used).

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The value string edited according to the given edit word.
