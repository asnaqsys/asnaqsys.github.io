---
title: "RecordAsBuffer class          | QSYS API Reference Guide"
description: "Defines operations to move data between a file record, a row in a dataset, and a string buffer. "
last_modified_at: 2024-08-09T17:25:29Z
---

Defines operations to move data between a file record, a row in a dataset, and a string buffer.

**Namespace:** ASNA.QSys.Runtime
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>

## Methods

| Signature | Description |
| --- | --- |
| [BufferToRecord](#bool-buffertorecorddatarow-row-string-buffer)([DataRow](https://learn.microsoft.com/en-us/dotnet/api/system.data.datarow?view=net-8.0), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Deserialize a string containing a record of RPG-encoded data into a DataRow.
| [BufferToRecord](#bool-buffertorecordadgdataset-dataset-string-formatname-string-buffer)([AdgDataSet](/reference/datagate/datagate-client/adg-data-set.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Deserialize a string containing a record of RPG-encoded data into a DataRow.
| [GetDateFormatString](#string-getdateformatstringdatetimeformat-format)([DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html)) | Creates the string pattern to format a fixed date value.
| [GetDateFormatStringNoSeparator](#string-getdateformatstringnoseparatordatetimeformat-format)([DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html)) | Creates the string pattern to format a fixed date value without a separator character.
| [GetDateFormatStringNoSeparator](#string-getdateformatstringnoseparatorstring-format)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Creates the string pattern to format a fixed date value without a separator character.
| [GetFormatString](#string-getformatstringstring-subtype-string-kind)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Creates the string pattern to format a fixed date/time/timestamp value.
| [GetFormatString](#string-getformatstringint-subtype-string-kind)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Creates the string pattern to format a fixed date/time/timestamp value.
| [GetFormatStringNoSeparator](#string-getformatstringnoseparatorint-subtype-string-kind)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Creates the string pattern to format a fixed date/time/timestamp value without a separator character.
| [GetTimeFormatString](#string-gettimeformatstringdatetimeformat-format)([DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html)) | Creates the string pattern to format a fixed time value.
| [GetTimestampFormatString()](#string-gettimestampformatstring) | Creates the string pattern to format a fixed timestamp value.
| [RecordToBuffer](#stringbuilder-recordtobufferadgdataset-dataset-string-formatname)([AdgDataSet](/reference/datagate/datagate-client/adg-data-set.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Returns a StringBuilder object with the contents of a file record, intepreting the datarow column contents as fixed-format values.

### bool BufferToRecord([DataRow row](https://learn.microsoft.com/en-us/dotnet/api/system.data.datarow?view=net-8.0), [string buffer](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Deserialize a string containing a record of RPG-encoded data into a DataRow.

```cs
bool BufferToRecord(DataRow row, string buffer)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DataRow](https://learn.microsoft.com/en-us/dotnet/api/system.data.datarow?view=net-8.0) | row | The DataRow to load with data.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | buffer | The string buffer contianing the data.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | True if the operation is successful.

### bool BufferToRecord([AdgDataSet dataSet](/reference/datagate/datagate-client/adg-data-set.html), [string formatName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string buffer](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Deserialize a string containing a record of RPG-encoded data into a DataRow.

```cs
bool BufferToRecord(AdgDataSet dataSet, string formatName, string buffer)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [AdgDataSet](/reference/datagate/datagate-client/adg-data-set.html) | dataSet | The AdgDataSet object that contains the table row to load.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatName | The name of the table.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | buffer | The string buffer contianing the data.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | True if the operation is successful.

### string GetDateFormatString([DateTimeFormat format](/reference/datagate/datagate-common/date-time-format.html))

Creates the string pattern to format a fixed date value.

```cs
string GetDateFormatString(DateTimeFormat format)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html) | format | The DateTimeFormat enum value for the requested fixed date format.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The string pattern for the requested fixed date format.

### string GetDateFormatStringNoSeparator([DateTimeFormat format](/reference/datagate/datagate-common/date-time-format.html))

Creates the string pattern to format a fixed date value without a separator character.

```cs
string GetDateFormatStringNoSeparator(DateTimeFormat format)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html) | format | The DateTimeFormat enum value for the requested fixed date format.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The string pattern for the requested fixed date format, with no separator character.

### string GetDateFormatStringNoSeparator([string format](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Creates the string pattern to format a fixed date value without a separator character.

```cs
string GetDateFormatStringNoSeparator(string format)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | format | The DateTimeFormat enum value as a string.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The string pattern for the requested fixed date format, with no separator character.

### string GetFormatString([string subType](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string kind](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Creates the string pattern to format a fixed date/time/timestamp value.

```cs
string GetFormatString(string subType, string kind)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | subType | The DateTimeFormat enum value as a string.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | kind | The kind as a string, one of "DATE", "TIME", or "TIMESTAMP".

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The string pattern for the requested fixed date/time/timestamp format.

### string GetFormatString([int subType](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [string kind](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Creates the string pattern to format a fixed date/time/timestamp value.

```cs
string GetFormatString(int subType, string kind)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | subType | The DateTimeFormat enum value as an integer.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | kind | The kind as a string, one of "DATE", "TIME", or "TIMESTAMP".

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The string pattern for the requested fixed date/time/timestamp format.

### string GetFormatStringNoSeparator([int subType](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [string kind](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Creates the string pattern to format a fixed date/time/timestamp value without a separator character.

```cs
string GetFormatStringNoSeparator(int subType, string kind)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | subType | The DateTimeFormat enum value as an integer.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | kind | The kind as a string, one of "DATE", "TIME", or "TIMESTAMP".

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The string pattern for the requested fixed date/time/timestamp format, with no separator character.

### string GetTimeFormatString([DateTimeFormat format](/reference/datagate/datagate-common/date-time-format.html))

Creates the string pattern to format a fixed time value.

```cs
string GetTimeFormatString(DateTimeFormat format)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html) | format | The DateTimeFormat enum value for the requested fixed time format.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The string pattern for the requested fixed time format.

### string GetTimestampFormatString()

Creates the string pattern to format a fixed timestamp value.

```cs
string GetTimestampFormatString()
```

### StringBuilder RecordToBuffer([AdgDataSet dataSet](/reference/datagate/datagate-client/adg-data-set.html), [string formatName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Returns a StringBuilder object with the contents of a file record, intepreting the datarow column contents as fixed-format values.

```cs
StringBuilder RecordToBuffer(AdgDataSet dataSet, string formatName)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [AdgDataSet](/reference/datagate/datagate-client/adg-data-set.html) | dataSet | The AdgDataSet object where the record exists.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatName | The name of the record format.

#### Returns

| Type | Description
| --- | ---
| [StringBuilder](https://learn.microsoft.com/en-us/dotnet/api/system.text.stringbuilder?view=net-8.0) | The StringBuilder object with the contents of the record format.
