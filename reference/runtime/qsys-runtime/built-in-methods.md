---
title: "BuiltInMethods class          | QSYS API Reference Guide"
description: "Contains extension methods for handling Built-in functions according to RPG semantics. "
last_modified_at: 2024-08-08T21:41:46Z
---

Contains extension methods for handling Built-in functions according to RPG semantics.

**Namespace:** ASNA.QSys.Runtime
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>

## Methods

| Signature | Description |
| --- | --- |
| [BIInt](#int-biintdecimal-num-bool-halfadjust)([Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Convert to Integer with half adjust.
| [BIInt](#int-biintfloat-num-bool-halfadjust)([Single](https://learn.microsoft.com/en-us/dotnet/api/system.single?view=net-8.0), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Convert to Integer with half adjust.
| [BIInt](#int-biintdouble-num-bool-halfadjust)([Double](https://learn.microsoft.com/en-us/dotnet/api/system.double?view=net-8.0), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Convert to Integer with half adjust.
| [BIInt](#int-biintstring-num-bool-halfadjust)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Convert to Integer with half adjust.
| [BIInt\<TLen\>](#int-biint-tlen-fixedstring-tlen-num-bool-halfadjust)([FixedString\<TLen\>](/reference/runtime/qsys-runtime/fixed-string-1.html), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Convert to Integer with half adjust.
| [BIUns](#int-biunsdecimal-num-bool-halfadjust)([Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Convert to Unsigned Integer with half adjust.
| [BIUns](#int-biunsint-num-bool-halfadjust)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Convert to Unsigned Integer with half adjust.
| [BIUns](#int-biunsfloat-num-bool-halfadjust)([Single](https://learn.microsoft.com/en-us/dotnet/api/system.single?view=net-8.0), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Convert to Unsigned Integer with half adjust.
| [BIUns](#int-biunsdouble-num-bool-halfadjust)([Double](https://learn.microsoft.com/en-us/dotnet/api/system.double?view=net-8.0), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Convert to Unsigned Integer with half adjust.
| [BIUns](#int-biunsstring-num-bool-halfadjust)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Convert to Unsigned Integer with half adjust.
| [BIUns\<TLen\>](#int-biuns-tlen-fixedstring-tlen-num-bool-halfadjust)([FixedString\<TLen\>](/reference/runtime/qsys-runtime/fixed-string-1.html), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Convert to Unsigned Integer with half adjust.

### int BIInt([decimal num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [bool halfAdjust](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Convert to Integer with half adjust.

```cs
int BIInt(decimal num, bool halfAdjust)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | num | Input decimal number.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | halfAdjust | True if half-adjust is requested; False otherwise.

#### Returns

| Type | Description
| --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | The number converted.

### int BIInt([float num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [bool halfAdjust](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Convert to Integer with half adjust.

```cs
int BIInt(float num, bool halfAdjust)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Single](https://learn.microsoft.com/en-us/dotnet/api/system.single?view=net-8.0) | num | Input floating number.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | halfAdjust | True if half-adjust is requested; False otherwise.

#### Returns

| Type | Description
| --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | The number converted.

### int BIInt([double num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [bool halfAdjust](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Convert to Integer with half adjust.

```cs
int BIInt(double num, bool halfAdjust)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Double](https://learn.microsoft.com/en-us/dotnet/api/system.double?view=net-8.0) | num | Input double number.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | halfAdjust | True if half-adjust is requested; False otherwise.

#### Returns

| Type | Description
| --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | The number converted.

### int BIInt([string num](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [bool halfAdjust](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Convert to Integer with half adjust.

```cs
int BIInt(string num, bool halfAdjust)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | num | Input number as string.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | halfAdjust | True if half-adjust is requested; False otherwise.

#### Returns

| Type | Description
| --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | The number converted.

### int BIInt\<TLen\>([FixedString\<TLen\> num](/reference/runtime/qsys-runtime/fixed-string-1.html), [bool halfAdjust](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Convert to Integer with half adjust.

```cs
int BIInt<TLen>(FixedString<TLen> num, bool halfAdjust)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [FixedString\<TLen\>](/reference/runtime/qsys-runtime/fixed-string-1.html) | num | Input fixed-string number.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | halfAdjust | True if half-adjust is requested; False otherwise.

#### Returns

| Type | Description
| --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | The number converted.

### int BIUns([decimal num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [bool halfAdjust](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Convert to Unsigned Integer with half adjust.

```cs
int BIUns(decimal num, bool halfAdjust)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | num | Input decimal number.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | halfAdjust | True if half-adjust is requested; False otherwise.

#### Returns

| Type | Description
| --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | The number converted.

### int BIUns([int num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [bool halfAdjust](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Convert to Unsigned Integer with half adjust.

```cs
int BIUns(int num, bool halfAdjust)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | num | Input integer number.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | halfAdjust | True if half-adjust is requested; False otherwise.

#### Returns

| Type | Description
| --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | The number converted.

### int BIUns([float num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [bool halfAdjust](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Convert to Unsigned Integer with half adjust.

```cs
int BIUns(float num, bool halfAdjust)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Single](https://learn.microsoft.com/en-us/dotnet/api/system.single?view=net-8.0) | num | Input floating number.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | halfAdjust | True if half-adjust is requested; False otherwise.

#### Returns

| Type | Description
| --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | The number converted.

### int BIUns([double num](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [bool halfAdjust](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Convert to Unsigned Integer with half adjust.

```cs
int BIUns(double num, bool halfAdjust)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Double](https://learn.microsoft.com/en-us/dotnet/api/system.double?view=net-8.0) | num | Input double number.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | halfAdjust | True if half-adjust is requested; False otherwise.

#### Returns

| Type | Description
| --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | The number converted.

### int BIUns([string num](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [bool halfAdjust](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Convert to Unsigned Integer with half adjust.

```cs
int BIUns(string num, bool halfAdjust)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | num | Input number as string.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | halfAdjust | True if half-adjust is requested; False otherwise.

#### Returns

| Type | Description
| --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | The number converted.

### int BIUns\<TLen\>([FixedString\<TLen\> num](/reference/runtime/qsys-runtime/fixed-string-1.html), [bool halfAdjust](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Convert to Unsigned Integer with half adjust.

```cs
int BIUns<TLen>(FixedString<TLen> num, bool halfAdjust)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [FixedString\<TLen\>](/reference/runtime/qsys-runtime/fixed-string-1.html) | num | Input number as fixed-string.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | halfAdjust | True if half-adjust is requested; False otherwise.

#### Returns

| Type | Description
| --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | The number converted.
