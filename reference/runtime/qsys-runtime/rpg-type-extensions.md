---
title: "RpgTypeExtensions class       | QSYS API Reference Guide"
description: "Provides extension methods for RPG types, including methods for moving and manipulating fixed-length strings and decimal numbers. "
last_modified_at: 2024-08-09T17:25:29Z
---

Provides extension methods for RPG types, including methods for moving and manipulating fixed-length strings and decimal numbers.

**Namespace:** ASNA.QSys.Runtime
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>

## Methods

| Signature | Description |
| --- | --- |
| [MoveL\<TDig, TDec, TLen\>](#decimal-movel-tdig-tdec-tlen-fixedstring-tlen-s-fixeddecimal-tdig-tdec-decnum-bool-pad)([FixedString\<TLen\>](/reference/runtime/qsys-runtime/fixed-string-1.html), [FixedDecimal\<TDig, TDec\>](/reference/runtime/qsys-runtime/fixed-decimal-2.html), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | MoveL extension.
| [MoveR\<TDig, TDec, TLen\>](#decimal-mover-tdig-tdec-tlen-fixedstring-tlen-s-fixeddecimal-tdig-tdec-decnum-bool-pad)([FixedString\<TLen\>](/reference/runtime/qsys-runtime/fixed-string-1.html), [FixedDecimal\<TDig, TDec\>](/reference/runtime/qsys-runtime/fixed-decimal-2.html), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | MoveR extension.
| [RemoveDate](#datetime-removedatedatetime-from)([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime)) | RemoveDate extension.
| [RemoveTime](#datetime-removetimedatetime-from)([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime)) | RemoveTime extension.

### decimal MoveL\<TDig, TDec, TLen\>([FixedString\<TLen\> s](/reference/runtime/qsys-runtime/fixed-string-1.html), [FixedDecimal\<TDig, TDec\> decNum](/reference/runtime/qsys-runtime/fixed-decimal-2.html), [bool pad](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

MoveL extension.

```cs
decimal MoveL<TDig, TDec, TLen>(FixedString<TLen> s, FixedDecimal<TDig, TDec> decNum, bool pad)
```

### decimal MoveR\<TDig, TDec, TLen\>([FixedString\<TLen\> s](/reference/runtime/qsys-runtime/fixed-string-1.html), [FixedDecimal\<TDig, TDec\> decNum](/reference/runtime/qsys-runtime/fixed-decimal-2.html), [bool pad](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

MoveR extension.

```cs
decimal MoveR<TDig, TDec, TLen>(FixedString<TLen> s, FixedDecimal<TDig, TDec> decNum, bool pad)
```

### DateTime RemoveDate([DateTime from](https://docs.microsoft.com/en-us/dotnet/api/system.datetime))

RemoveDate extension.

```cs
DateTime RemoveDate(DateTime from)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | from | RemoveDate from param.

#### Returns

| Type | Description
| --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | DateTime result.

### DateTime RemoveTime([DateTime from](https://docs.microsoft.com/en-us/dotnet/api/system.datetime))

RemoveTime extension.

```cs
DateTime RemoveTime(DateTime from)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | from | RemoveTime from param.

#### Returns

| Type | Description
| --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | DateTime result.
