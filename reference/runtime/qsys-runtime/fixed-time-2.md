---
title: "FixedTime<T1, T2> struct      | QSYS API Reference Guide"
description: "Holds a fixed-time value in the specified format and with the given separator. "
last_modified_at: 2024-08-09T16:18:25Z
---

Holds a fixed-time value in the specified format and with the given separator.

**Namespace:** ASNA.QSys.Runtime
**Assembly:** ASNA.QSys.Runtime.dll

<br>
<br>

## Properties

| Type | Name | Description
| --- | --- | --- 
| [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html) | Format | IFixedDateTime Format implementation. Returns the format for this FixedTime value. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | Hour | Returns the hour in this FixedTime value. |
| [DateTimeDataKind](/reference/runtime/qsys-runtime/date-time-data-kind.html) | Kind | IFixedDateTime Kind implementation. Returns DateTimeDataKind.Time. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | Length | Gets the length of the FixedTime value, given its format and separator. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | Minute | Returns the minutes in this FixedTime value. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | Second | Returns the seconds in this FixedTime value. |
| [DateTimeSeparator](/reference/runtime/qsys-runtime/date-time-separator.html) | Separator | IFixedDateTime Separator implementation. Returns the separator for this FixedTime value. |
| [TimeOnly](https://learn.microsoft.com/en-us/dotnet/api/system.timeonly?view=net-8.0) | TimeValue | Gets the value of this FixedTime as a TimeOnly value. |
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | Value | Gets the value of this FixedTime as a System.DateTime value. |
| [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) | ValueAsObject | Returns the value of this FixedTime as an object. |

## Methods

| Signature | Description |
| --- | --- |
| [CompareTo](#int-comparetoobject-obj)([Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | Compares the current instance with another object of the same type and returns an integer that indicates whether the current instance precedes, follows, or occurs in the same position in the sort order as the other object.
| [Convert](#ifixedsizetype-datetime-convertdatetime-value)([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime)) | Convert a DateTime to a FixedTime of the same format and separator.
| [ToNumericString()](#string-tonumericstring) | Convert to numeric string representation of the FixedTime, according to its format with no separators.
| [ToString()](#string-tostring) | Convert to the string representation of the FixedTime, according to its format and separator.
| [ToString](#string-tostringdatetimeformat-format-datetimeseparator-separator)([DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html), [DateTimeSeparator](/reference/runtime/qsys-runtime/date-time-separator.html)) | Convert to the string of the FixedTime, according to the given format and separator.

### int CompareTo([object obj](https://docs.microsoft.com/en-us/dotnet/api/system.object))

Compares the current instance with another object of the same type and returns an integer that indicates whether the current instance precedes, follows, or occurs in the same position in the sort order as the other object.

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
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | A value that indicates the relative order of the objects being compared.

### IFixedSizeType\<DateTime\> Convert([DateTime value](https://docs.microsoft.com/en-us/dotnet/api/system.datetime))

Convert a DateTime to a FixedTime of the same format and separator.

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
| [IFixedSizeType`1](/reference/runtime/qsys-runtime/i-fixed-size-type-1.html) | A new FixedTime value with the same format and separator.

### string ToNumericString()

Convert to numeric string representation of the FixedTime, according to its format with no separators.

```cs
string ToNumericString()
```

### string ToString()

Convert to the string representation of the FixedTime, according to its format and separator.

```cs
string ToString()
```

### string ToString([DateTimeFormat format](/reference/datagate/datagate-common/date-time-format.html), [DateTimeSeparator separator](/reference/runtime/qsys-runtime/date-time-separator.html))

Convert to the string of the FixedTime, according to the given format and separator.

```cs
string ToString(DateTimeFormat format, DateTimeSeparator separator)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html) | format | DateTimeFormat of the FixedTime.
| [DateTimeSeparator](/reference/runtime/qsys-runtime/date-time-separator.html) | separator | DateTimeSeparator of the FixedTime.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The string representation of the FixedTime value, with the given format and separator.
