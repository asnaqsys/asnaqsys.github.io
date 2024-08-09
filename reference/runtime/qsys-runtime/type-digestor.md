---
title: "TypeDigestor class            | QSYS API Reference Guide"
description: "Contains methods that aid in the parsing of the generic type arguments of fixed-sized types. "
last_modified_at: 2024-08-09T17:25:29Z
---

Contains methods that aid in the parsing of the generic type arguments of fixed-sized types.

**Namespace:** ASNA.QSys.Runtime
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>

## Methods

| Signature | Description |
| --- | --- |
| [computeCharLength](#void-computecharlengthtype-tlen-int32-length)([Type](https://docs.microsoft.com/en-us/dotnet/api/system.type), [Int32&](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Given the ILen type that represents the length of a FixedString type, computes the actual value for the length.
| [computeDecimalLength](#void-computedecimallengthtype-tdigits-type-tdecimals-int32-digits-int32-decimals)([Type](https://docs.microsoft.com/en-us/dotnet/api/system.type), [Type](https://docs.microsoft.com/en-us/dotnet/api/system.type), [Int32&](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32&](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Given the INumber types that represent the digits and decimals of a FixedDecimal type, computes the actual values for digits and decimals.
| [computeDim](#void-computedimtype-tdim-int32-dim)([Type](https://docs.microsoft.com/en-us/dotnet/api/system.type), [Int32&](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Given the IDim type that represents the dimension of a FixedArray type, computes the actual value for the dimension.
| [formatToType](#type-formattotypedatetimeformat-format)([DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html)) | Returns the type corresponding to a DateTimeFormat.
| [GetDateTimeObject](#ifixeddatetime-getdatetimeobjectdatetimedatakind-kind-datetimeformat-format-datetimeseparator-sep)([DateTimeDataKind](/reference/runtime/qsys-runtime/date-time-data-kind.html), [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html), [DateTimeSeparator](/reference/runtime/qsys-runtime/date-time-separator.html)) | Constructs a fixed date/time/timestamp object given its kind, format, and separator.
| [parseDateTimeType](#void-parsedatetimetypedatetimedatakind-kind-type-tformat-type-tseparator-datetimeformat-format-datetimeseparator-separator-bool-replacedefault)([DateTimeDataKind](/reference/runtime/qsys-runtime/date-time-data-kind.html), [Type](https://docs.microsoft.com/en-us/dotnet/api/system.type), [Type](https://docs.microsoft.com/en-us/dotnet/api/system.type), [DateTimeFormat&](/reference/datagate/datagate-common/date-time-format.html), [DateTimeSeparator&](/reference/runtime/qsys-runtime/date-time-separator.html), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Finds the format and separator enum values of a fixed date/time/timestamp given the kind, IDateTimeFormat, and IDateTimeSeparator.
| [separatorToType](#type-separatortotypedatetimeseparator-separator)([DateTimeSeparator](/reference/runtime/qsys-runtime/date-time-separator.html)) | Returns the type corresponding to a DateTimeSeparator.

### void computeCharLength([Type tLen](https://docs.microsoft.com/en-us/dotnet/api/system.type), [Int32& length](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

Given the ILen type that represents the length of a FixedString type, computes the actual value for the length.

```cs
void computeCharLength(Type tLen, Int32& length)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Type](https://docs.microsoft.com/en-us/dotnet/api/system.type) | tLen | The ILen type that represents the length.
| [Int32&](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | length | The numeric value of tLen.

### void computeDecimalLength([Type tDigits](https://docs.microsoft.com/en-us/dotnet/api/system.type), [Type tDecimals](https://docs.microsoft.com/en-us/dotnet/api/system.type), [Int32& digits](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32& decimals](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

Given the INumber types that represent the digits and decimals of a FixedDecimal type, computes the actual values for digits and decimals.

```cs
void computeDecimalLength(Type tDigits, Type tDecimals, Int32& digits, Int32& decimals)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Type](https://docs.microsoft.com/en-us/dotnet/api/system.type) | tDigits | The INumber type that represents the digits.
| [Type](https://docs.microsoft.com/en-us/dotnet/api/system.type) | tDecimals | The INumber type that represents the decimal positions.
| [Int32&](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | digits | The numeric value of tDigits.
| [Int32&](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | decimals | The numeric value of tDecimals.

### void computeDim([Type tDim](https://docs.microsoft.com/en-us/dotnet/api/system.type), [Int32& dim](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

Given the IDim type that represents the dimension of a FixedArray type, computes the actual value for the dimension.

```cs
void computeDim(Type tDim, Int32& dim)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Type](https://docs.microsoft.com/en-us/dotnet/api/system.type) | tDim | The IDim type that represents the dimension.
| [Int32&](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | dim | The numeric value of tDim.

### Type formatToType([DateTimeFormat format](/reference/datagate/datagate-common/date-time-format.html))

Returns the type corresponding to a DateTimeFormat.

```cs
Type formatToType(DateTimeFormat format)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html) | format | The DateTimeFormat value for which to return the corresponding type.

#### Returns

| Type | Description
| --- | ---
| [Type](https://docs.microsoft.com/en-us/dotnet/api/system.type) | The Type object corresponding to the format parameter value.

### IFixedDateTime GetDateTimeObject([DateTimeDataKind kind](/reference/runtime/qsys-runtime/date-time-data-kind.html), [DateTimeFormat format](/reference/datagate/datagate-common/date-time-format.html), [DateTimeSeparator sep](/reference/runtime/qsys-runtime/date-time-separator.html))

Constructs a fixed date/time/timestamp object given its kind, format, and separator.

```cs
IFixedDateTime GetDateTimeObject(DateTimeDataKind kind, DateTimeFormat format, DateTimeSeparator sep)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DateTimeDataKind](/reference/runtime/qsys-runtime/date-time-data-kind.html) | kind | The DateTimeDataKind to construct.
| [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html) | format | The DateTimeFormat of the date/time/timestamp object. This parameter is ignored when constructing a FixedTimestamp object.
| [DateTimeSeparator](/reference/runtime/qsys-runtime/date-time-separator.html) | sep | The DateTimeSeparator of the date/time/timestamp object

#### Returns

| Type | Description
| --- | ---
| [IFixedDateTime](/reference/runtime/qsys-runtime/i-fixed-date-time.html) | The constructed fixed date/time/timestamp object.

### void parseDateTimeType([DateTimeDataKind kind](/reference/runtime/qsys-runtime/date-time-data-kind.html), [Type Tformat](https://docs.microsoft.com/en-us/dotnet/api/system.type), [Type Tseparator](https://docs.microsoft.com/en-us/dotnet/api/system.type), [DateTimeFormat& format](/reference/datagate/datagate-common/date-time-format.html), [DateTimeSeparator& separator](/reference/runtime/qsys-runtime/date-time-separator.html), [bool replaceDefault](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Finds the format and separator enum values of a fixed date/time/timestamp given the kind, IDateTimeFormat, and IDateTimeSeparator.

```cs
void parseDateTimeType(DateTimeDataKind kind, Type Tformat, Type Tseparator, DateTimeFormat& format, DateTimeSeparator& separator, bool replaceDefault)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DateTimeDataKind](/reference/runtime/qsys-runtime/date-time-data-kind.html) | kind | The DateTimeDataKind to use to find the separator when the Tseparator parameter is typeof(_Default).
| [Type](https://docs.microsoft.com/en-us/dotnet/api/system.type) | Tformat | The IDatetimeFormat type that represents the fixed date/time/timestamp format.
| [Type](https://docs.microsoft.com/en-us/dotnet/api/system.type) | Tseparator | The IDateTimeSeparator type that represents the fixed date/time/timestamp separator.
| [DateTimeFormat&](/reference/datagate/datagate-common/date-time-format.html) | format | Returs the DateTimeFormat enum value correspoding to the given parameteres.
| [DateTimeSeparator&](/reference/runtime/qsys-runtime/date-time-separator.html) | separator | Returs the DateTimeSeparator enum value correspoding to the given parameteres.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | replaceDefault | True to convert the default separator into the actual separator according to the date/time kind and its format. True is the default.

### Type separatorToType([DateTimeSeparator separator](/reference/runtime/qsys-runtime/date-time-separator.html))

Returns the type corresponding to a DateTimeSeparator.

```cs
Type separatorToType(DateTimeSeparator separator)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DateTimeSeparator](/reference/runtime/qsys-runtime/date-time-separator.html) | separator | The DateTimeSeparator value for which to return the corresponding type.

#### Returns

| Type | Description
| --- | ---
| [Type](https://docs.microsoft.com/en-us/dotnet/api/system.type) | The Type object corresponding to the separator parameter value.
