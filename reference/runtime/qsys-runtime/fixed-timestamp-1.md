---
title: "FixedTimestamp<T> struct      | QSYS API Reference Guide"
description: "Holds a fixed-timestamp value with the given separator. "
last_modified_at: 2024-08-08T21:41:46Z
---

Holds a fixed-timestamp value with the given separator.

**Namespace:** ASNA.QSys.Runtime
**Assembly:** ASNA.QSys.Runtime.dll

<br>
<br>

## Properties

| Type | Name | Description
| --- | --- | --- 
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | Day | Returns the day in this FixedTimestamp value. |
| [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html) | Format | IFixedDateTime Format implementation. Returns DateTimeFormat.ISO. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | Hour | Returns the hour in this FixedTimestamp value. |
| [DateTimeDataKind](/reference/runtime/qsys-runtime/date-time-data-kind.html) | Kind | IFixedDateTime Kind implementation. Returns DateTimeDataKind.Timestamp. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | Length | Gets the length of the FixedTimestamp value, given its separator. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | Milisecond | Returns the milliseconds in this FixedTimestamp value. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | Minute | Returns the minutes in this FixedTimestamp value. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | Month | Returns the month in this FixedTimestamp value. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | Second | Returns the seconds in this FixedTimestamp value. |
| [DateTimeSeparator](/reference/runtime/qsys-runtime/date-time-separator.html) | Separator | IFixedDateTime Separator implementation. Returns the separator for this FixedTimestamp value. |
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | Value | Gets the value of this FixedTimestamp as a System.DateTime value. |
| [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) | ValueAsObject | Returns the value of this FixedTimestamp as an object. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | Year | Returns the year in this FixedTimestamp value. |

## Methods

| Signature | Description |
| --- | --- |
| [CompareTo](#int-comparetoobject-obj)([Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | Compares this instance to a specified DateTime or FixedSize type and returns an indication of their relative values.
| [Convert](#ifixedsizetype-datetime-convertdatetime-value)([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime)) | Convert a DateTime to a FixedTimestamp of the same separator.
| [ToNumericString()](#string-tonumericstring) | Convert to numeric string representation of the FixedTimestamp, according to its format with no separators.
| [ToString()](#string-tostring) | Convert to the string representation of the FixedTimestamp, according to its format and separator.
| [ToString](#string-tostringdatetimeseparator-separator)([DateTimeSeparator](/reference/runtime/qsys-runtime/date-time-separator.html)) | Convert to the string of the FixedTimestamp, according to the given separator.

### int CompareTo([object obj](https://docs.microsoft.com/en-us/dotnet/api/system.object))

Compares this instance to a specified DateTime or FixedSize type and returns an indication of their relative values.

```cs
int CompareTo(object obj)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) | obj | The object to compare against.

#### Returns

| Type | Description
| --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | A signed number indicating the relative values of this instance and input value. If object cannot be compared, it throws exception.

### IFixedSizeType\<DateTime\> Convert([DateTime value](https://docs.microsoft.com/en-us/dotnet/api/system.datetime))

Convert a DateTime to a FixedTimestamp of the same separator.

```cs
IFixedSizeType<DateTime> Convert(DateTime value)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | value | The DateTime value to convert.

#### Returns

| Type | Description
| --- | ---
| [IFixedSizeType`1](/reference/runtime/qsys-runtime/i-fixed-size-type-1.html) | A new FixedTimestamp value with the same separator.

### string ToNumericString()

Convert to numeric string representation of the FixedTimestamp, according to its format with no separators.

```cs
string ToNumericString()
```

### string ToString()

Convert to the string representation of the FixedTimestamp, according to its format and separator.

```cs
string ToString()
```

### string ToString([DateTimeSeparator separator](/reference/runtime/qsys-runtime/date-time-separator.html))

Convert to the string of the FixedTimestamp, according to the given separator.

```cs
string ToString(DateTimeSeparator separator)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DateTimeSeparator](/reference/runtime/qsys-runtime/date-time-separator.html) | separator | DateTimeSeparator of the FixedTimestamp.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The string representation of the FixedTimestamp value, with the given separator.
