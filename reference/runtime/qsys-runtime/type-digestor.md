---
title: "TypeDigestor class            | QSYS API Reference Guide"
description: "Contains methods that aid in the parsing of the generic type arguments of fixed-sized types. "
last_modified_at: 2024-08-08T21:41:46Z
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
| [formatToType](#type-formattotypedatetimeformat-format)([DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html)) | Returns the type corresponding to a DateTimeFormat.
| [GetDateTimeObject](#ifixeddatetime-getdatetimeobjectdatetimedatakind-kind-datetimeformat-format-datetimeseparator-sep)([DateTimeDataKind](/reference/runtime/qsys-runtime/date-time-data-kind.html), [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html), [DateTimeSeparator](/reference/runtime/qsys-runtime/date-time-separator.html)) | Constructs a fixed date/time/timestamp object given its kind, format, and separator.
| [separatorToType](#type-separatortotypedatetimeseparator-separator)([DateTimeSeparator](/reference/runtime/qsys-runtime/date-time-separator.html)) | Returns the type corresponding to a DateTimeSeparator.

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
