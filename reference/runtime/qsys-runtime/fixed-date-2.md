---
title: "FixedDate<T1, T2> struct      | QSYS API Reference Guide"
description: "Holds a fixed-date value in the specified format and with the given separator. "
last_modified_at: 2024-08-09T16:18:25Z
---

Holds a fixed-date value in the specified format and with the given separator.

**Namespace:** ASNA.QSys.Runtime
**Assembly:** ASNA.QSys.Runtime.dll

<br>
<br>

## Properties

| Type | Name | Description
| --- | --- | --- 
| [DateOnly](https://learn.microsoft.com/en-us/dotnet/api/system.dateonly?view=net-8.0) | DateValue | Gets the value of this FixedDate as a DateOnly value. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | Day | Returns the day in this FixedDate value. |
| [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html) | Format | IFixedDateTime Format implementation. Returns the format for this FixedDate value. |
| [DateTimeDataKind](/reference/runtime/qsys-runtime/date-time-data-kind.html) | Kind | IFixedDateTime Kind implementation. Returns DateTimeDataKind.Date. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | Length | Gets the length of the FixedDate value, given its format and separator. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | Month | Returns the month in this FixedDate value. |
| [DateTimeSeparator](/reference/runtime/qsys-runtime/date-time-separator.html) | Separator | IFixedDateTime Separator implementation. Returns the separator for this FixedDate value. |
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | Value | Gets the value of this FixedDate as a System.DateTime value. |
| [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) | ValueAsObject | Returns the value of this FixedDate as an object. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | Year | Returns the year in this FixedDate value. |

## Methods

| Signature | Description |
| --- | --- |
| [CompareTo](#int-comparetoobject-obj)([Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | Compare To object.
| [Convert](#ifixedsizetype-datetime-convertdatetime-value)([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime)) | Convert to IFixedSizeType.
| [ToNumericString()](#string-tonumericstring) | Convert to numeric string.
| [ToString()](#string-tostring) | Convert ToString.
| [ToString](#string-tostringstring-format)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Convert to String.
| [ToString](#string-tostringdatetimeformat-format-datetimeseparator-separator)([DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html), [DateTimeSeparator](/reference/runtime/qsys-runtime/date-time-separator.html)) | Convert to string.

### int CompareTo([object obj](https://docs.microsoft.com/en-us/dotnet/api/system.object))

Compare To object.

```cs
int CompareTo(object obj)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) | obj | Object to compare against.

#### Returns

| Type | Description
| --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | A 32-bit signed integer that indicates whether this instance precedes, follows, or appears in the same position in the sort order as the obj parameter.

### IFixedSizeType\<DateTime\> Convert([DateTime value](https://docs.microsoft.com/en-us/dotnet/api/system.datetime))

Convert to IFixedSizeType.

```cs
IFixedSizeType<DateTime> Convert(DateTime value)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | value | DateTime value to convert.

#### Returns

| Type | Description
| --- | ---
| [IFixedSizeType`1](/reference/runtime/qsys-runtime/i-fixed-size-type-1.html) | The IFixedSizeType result.

### string ToNumericString()

Convert to numeric string.

```cs
string ToNumericString()
```

### string ToString()

Convert ToString.

```cs
string ToString()
```

### string ToString([string format](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Convert to String.

```cs
string ToString(string format)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | format | Input format.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The converted string result.

### string ToString([DateTimeFormat format](/reference/datagate/datagate-common/date-time-format.html), [DateTimeSeparator separator](/reference/runtime/qsys-runtime/date-time-separator.html))

Convert to string.

```cs
string ToString(DateTimeFormat format, DateTimeSeparator separator)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html) | format | Input format.
| [DateTimeSeparator](/reference/runtime/qsys-runtime/date-time-separator.html) | separator | Input separator.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The converted string result.
