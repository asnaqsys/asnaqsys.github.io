---
title: "EditWord class                | QSYS API Reference Guide"
description: "Provides methods to format numeric values according to Edit Word "
last_modified_at: 2024-08-09T16:18:58Z
---

Provides methods to format numeric values according to Edit Word

**Namespace:** ASNA.QSys.Expo.Model
**Assembly:** ASNA.QSys.Expo.Model.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>

## Remarks

Provides support to give presentation to numeric fields according to [IBM i Edit Word](https://www.ibm.com/docs/en/i/7.2?topic=words-summary-coding-rules-edit) formatting rules. 


## Methods

| Signature | Description |
| --- | --- |
| [Apply](#string-applydecimal-numeric-int-decimals-int-length-string-editwordstring)([Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Gets a string value representing the given numeric value after formatting it according to an Edit Word
| [ApplyEditWord](#string-applyeditwordstring-editwordstring-string-valuestring-char-decimalpoint-char-thousandseparator-char-currencysymbol-bool-printcurrencysymbol)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Char](https://docs.microsoft.com/en-us/dotnet/api/system.char), [Char](https://docs.microsoft.com/en-us/dotnet/api/system.char), [Char](https://docs.microsoft.com/en-us/dotnet/api/system.char), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Gets a string value representing the given numeric value after formatting it according to an Edit Word

### string Apply([decimal numeric](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [int decimals](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int length](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [string editwordString](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Gets a string value representing the given numeric value after formatting it according to an Edit Word

```cs
string Apply(decimal numeric, int decimals, int length, string editwordString)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | numeric | input numeric value
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | decimals | field decimal positions
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | length | field length
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | editwordString | Edit Word

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | the formatted value as string

### string ApplyEditWord([string editwordString](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string valueString](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [char decimalPoint](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/char), [char thousandSeparator](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/char), [char currencySymbol](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/char), [bool printCurrencySymbol](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Gets a string value representing the given numeric value after formatting it according to an Edit Word

```cs
string ApplyEditWord(string editwordString, string valueString, char decimalPoint, char thousandSeparator, char currencySymbol, bool printCurrencySymbol)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | editwordString | input Edit Word
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | valueString | input value in a string
| [Char](https://docs.microsoft.com/en-us/dotnet/api/system.char) | decimalPoint | decimal point symbol
| [Char](https://docs.microsoft.com/en-us/dotnet/api/system.char) | thousandSeparator | thousands separator symbol
| [Char](https://docs.microsoft.com/en-us/dotnet/api/system.char) | currencySymbol | currency symbol
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | printCurrencySymbol | currency symbol

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | the formatted string
