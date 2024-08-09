---
title: "DateTimeOps class             | QSYS API Reference Guide"
description: "Defines operations with RPG semantics on System.DateTime values. "
last_modified_at: 2024-08-09T17:25:29Z
---

Defines operations with RPG semantics on System.DateTime values.

**Namespace:** ASNA.QSys.Runtime
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>

## Methods

| Signature | Description |
| --- | --- |
| [AddDateAndTime](#datetime-adddateandtimedatetime-date-datetime-time)([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime)) | Merge the date portion of a DateTime value with the time portion of another.
| [AddDuration](#datetime-adddurationdatetime-datetime-double-duration-int-durationcode-bool-justthetime)([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [Double](https://learn.microsoft.com/en-us/dotnet/api/system.double?view=net-8.0), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | RPG's ADDDUR. Adds a duration span to a DateTime value.
| [ComputeDifference](#int-computedifferencedatetime-datetime1-datetime-datetime2-bool-ismonths)([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Compute the difference, in years or months, between two DateTime values.
| [ConvertJulianToFormattedTimeDecimal](#decimal-convertjuliantoformattedtimedecimaldatetime-thedatetime-int-digits)([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Convert a DateTime value to numeric in Julian format in 12 or 14 digits, according to RPG's specifications.
| [ConvertJulianToNumericString](#string-convertjuliantonumericstringdatetime-thedate)([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime)) | Convert a DateTime value to a string in Julian format without separators.
| [ConvertJulianToString](#string-convertjuliantostringdatetime-thedate-string-separator)([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Convert a DateTime value to a string in Julian format using separators.
| [ConvertStampToDate](#datetime-convertstamptodatedatetime-thestamp)([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime)) | Copy the date portion of theStamp to theDate.
| [ConvertStampToTime](#datetime-convertstamptotimedatetime-thestamp)([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime)) | Copy the time portion of theStamp to theTime. 
| [ConvertStampToUSATime](#datetime-convertstamptousatimedatetime-thestamp)([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime)) | Convert to *USA time (no seconds).
| [ConvertStringToJulian](#datetime-convertstringtojulianstring-thestring-string-separator)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Parse a string representing a Julian date with separator, returning its DateTime equivalent.
| [CopyDateToStamp](#datetime-copydatetostampdatetime-thedate-datetime-thestamp)([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime)) | Copy theDate to the date portion of theStamp. 
| [CopyTimeToStamp](#datetime-copytimetostampdatetime-thetime-datetime-thestamp)([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime)) | Copy theTime to the time portion of theStamp. 
| [DiffDuration](#double-diffdurationdatetime-datetime1-datetime-datetime2-int-durationcode)([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Subtract two DateTime objects giving the result in the specified duration.
| [GetCommonDate()](#datetime-getcommondate) | Get the date portion of the Job startup date.
| [GetCommonDateTime()](#datetime-getcommondatetime) | Get the Job startup DateTime value.
| [GetCommonDay()](#int-getcommonday) | Get the Job startup day of the month.
| [GetCommonDayAsDecimal()](#decimal-getcommondayasdecimal) | Get the Job startup day of the month as a decimal.
| [GetCommonMonth()](#int-getcommonmonth) | Get the Job startup month.
| [GetCommonMonthAsDecimal()](#decimal-getcommonmonthasdecimal) | Get the Job startup month as a decimal.
| [GetCommonYear()](#int-getcommonyear) | Get the Job startup year.
| [GetCommonYear2()](#int-getcommonyear2) | Get the Job startup two-digit year.
| [GetCommonYearAsDecimal2()](#decimal-getcommonyearasdecimal2) | Get the Job startup two-digit year as a decimal.
| [GetCommonYearAsDecimal4()](#decimal-getcommonyearasdecimal4) | Get the Job startup year as a decimal.
| [GetInitialDate](#decimal-getinitialdatedatetimeformat-format)([DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html)) | Gets the value of *DATE/UDATE depending on the given format. Use the proper format to obtain either a 6 (UDATE) or an 8 (*DATE) digit value.
| [NormalizeYY](#datetime-normalizeyydatetime-formatdate)([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime)) | Normalize the year portion of a DateTime value taken as a a two-digit year to the proper year in the range 1940 - 2039.
| [SubtractDuration](#datetime-subtractdurationdatetime-datetime-double-duration-int-durationcode-bool-justthetime)([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [Double](https://learn.microsoft.com/en-us/dotnet/api/system.double?view=net-8.0), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | RPG's SUBDUR. Subtracts a duration span from a DateTime value.
| [TruncToMicroseconds](#datetime-trunctomicrosecondsdatetime-thestamp)([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime)) | Truncate theStamp to the closest Microsecond (make it ISO format).

### DateTime AddDateAndTime([DateTime date](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTime time](https://docs.microsoft.com/en-us/dotnet/api/system.datetime))

Merge the date portion of a DateTime value with the time portion of another.

```cs
DateTime AddDateAndTime(DateTime date, DateTime time)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | date | The DateTime holding a date value.
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | time | The DateTime holding a time value.

#### Returns

| Type | Description
| --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | The merged date/time values.

### DateTime AddDuration([DateTime dateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [double duration](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [int durationCode](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [bool justTheTime](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

RPG's ADDDUR. Adds a duration span to a DateTime value.

```cs
DateTime AddDuration(DateTime dateTime, double duration, int durationCode, bool justTheTime)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | dateTime | The DateTime value.
| [Double](https://learn.microsoft.com/en-us/dotnet/api/system.double?view=net-8.0) | duration | The duraction span.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | durationCode | The duration code (see: ASNA.QSys.Runtime.DateTimeOps.DurationCode)
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | justTheTime | True if the DateTime value represents an RPG time.

#### Returns

| Type | Description
| --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | The result of adding the specified duration to dateTime.

### int ComputeDifference([DateTime dateTime1](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTime dateTime2](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [bool isMonths](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Compute the difference, in years or months, between two DateTime values.

```cs
int ComputeDifference(DateTime dateTime1, DateTime dateTime2, bool isMonths)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | dateTime1 | The minuend.
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | dateTime2 | The subtrahend.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | isMonths | True to compute the difference in months.

#### Returns

| Type | Description
| --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | The difference, in years or months, between the two given DateTime values.

### decimal ConvertJulianToFormattedTimeDecimal([DateTime theDateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [int digits](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Convert a DateTime value to numeric in Julian format in 12 or 14 digits, according to RPG's specifications.

```cs
decimal ConvertJulianToFormattedTimeDecimal(DateTime theDateTime, int digits)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | theDateTime | The DateTime value.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | digits | Number of digits in the result. Must be 12 or 14.

#### Returns

| Type | Description
| --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | The decimal number representation of theDateTime in Julian format.

### string ConvertJulianToNumericString([DateTime theDate](https://docs.microsoft.com/en-us/dotnet/api/system.datetime))

Convert a DateTime value to a string in Julian format without separators.

```cs
string ConvertJulianToNumericString(DateTime theDate)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | theDate | The DateTime value.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The string representing the date portion of theDate in Julian format without separators.

### string ConvertJulianToString([DateTime theDate](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [string separator](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Convert a DateTime value to a string in Julian format using separators.

```cs
string ConvertJulianToString(DateTime theDate, string separator)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | theDate | The DateTime value.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | separator | The separator.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The string representing the date portion of theDate in Julian format using separators.

### DateTime ConvertStampToDate([DateTime theStamp](https://docs.microsoft.com/en-us/dotnet/api/system.datetime))

Copy the date portion of theStamp to theDate.

```cs
DateTime ConvertStampToDate(DateTime theStamp)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | theStamp | ConvertStampToDate param .

#### Returns

| Type | Description
| --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | ConvertStampToDate returns.

### DateTime ConvertStampToTime([DateTime theStamp](https://docs.microsoft.com/en-us/dotnet/api/system.datetime))

Copy the time portion of theStamp to theTime. 

```cs
DateTime ConvertStampToTime(DateTime theStamp)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | theStamp | ConvertStampToTime param theStamp.

#### Returns

| Type | Description
| --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | ConvertStampToTime returns.

### DateTime ConvertStampToUSATime([DateTime theStamp](https://docs.microsoft.com/en-us/dotnet/api/system.datetime))

Convert to *USA time (no seconds).

```cs
DateTime ConvertStampToUSATime(DateTime theStamp)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | theStamp | ConvertStampToUSATime param theStamp.

#### Returns

| Type | Description
| --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | ConvertStampToUSATime returns.

### DateTime ConvertStringToJulian([string theString](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string separator](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Parse a string representing a Julian date with separator, returning its DateTime equivalent.

```cs
DateTime ConvertStringToJulian(string theString, string separator)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | theString | The string representing a Julian date.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | separator | The separator used in theString.

#### Returns

| Type | Description
| --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | The DateTime value equivalent to theString interpreted as a Julian date.

### DateTime CopyDateToStamp([DateTime theDate](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTime theStamp](https://docs.microsoft.com/en-us/dotnet/api/system.datetime))

Copy theDate to the date portion of theStamp. 

```cs
DateTime CopyDateToStamp(DateTime theDate, DateTime theStamp)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | theDate | CopyDateToStamp param theDate.
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | theStamp | CopyDateToStamp param theStamp.

#### Returns

| Type | Description
| --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | CopyDateToStamp returns.

### DateTime CopyTimeToStamp([DateTime theTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTime theStamp](https://docs.microsoft.com/en-us/dotnet/api/system.datetime))

Copy theTime to the time portion of theStamp. 

```cs
DateTime CopyTimeToStamp(DateTime theTime, DateTime theStamp)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | theTime | CopyTimeToStamp param theTime.
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | theStamp | CopyTimeToStamp param theStamp.

#### Returns

| Type | Description
| --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | CopyTimeToStamp returns.

### double DiffDuration([DateTime dateTime1](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [DateTime dateTime2](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [int durationCode](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Subtract two DateTime objects giving the result in the specified duration.

```cs
double DiffDuration(DateTime dateTime1, DateTime dateTime2, int durationCode)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | dateTime1 | The minuend.
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | dateTime2 | The subtrahend.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | durationCode | The duration code, as an integer (see: ASNA.QSys.Runtime.DateTimeOps.DurationCode). 

#### Returns

| Type | Description
| --- | ---
| [Double](https://learn.microsoft.com/en-us/dotnet/api/system.double?view=net-8.0) | The double number representing difference between the two DateTime values expressed in the given durationCode.

### DateTime GetCommonDate()

Get the date portion of the Job startup date.

```cs
DateTime GetCommonDate()
```

### DateTime GetCommonDateTime()

Get the Job startup DateTime value.

```cs
DateTime GetCommonDateTime()
```

### int GetCommonDay()

Get the Job startup day of the month.

```cs
int GetCommonDay()
```

### decimal GetCommonDayAsDecimal()

Get the Job startup day of the month as a decimal.

```cs
decimal GetCommonDayAsDecimal()
```

### int GetCommonMonth()

Get the Job startup month.

```cs
int GetCommonMonth()
```

### decimal GetCommonMonthAsDecimal()

Get the Job startup month as a decimal.

```cs
decimal GetCommonMonthAsDecimal()
```

### int GetCommonYear()

Get the Job startup year.

```cs
int GetCommonYear()
```

### int GetCommonYear2()

Get the Job startup two-digit year.

```cs
int GetCommonYear2()
```

### decimal GetCommonYearAsDecimal2()

Get the Job startup two-digit year as a decimal.

```cs
decimal GetCommonYearAsDecimal2()
```

### decimal GetCommonYearAsDecimal4()

Get the Job startup year as a decimal.

```cs
decimal GetCommonYearAsDecimal4()
```

### decimal GetInitialDate([DateTimeFormat format](/reference/datagate/datagate-common/date-time-format.html))

Gets the value of *DATE/UDATE depending on the given format. Use the proper format to obtain either a 6 (UDATE) or an 8 (*DATE) digit value.

```cs
decimal GetInitialDate(DateTimeFormat format)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html) | format | The DateTimeFormat value that represents the *DATE/UDATE value.

#### Returns

| Type | Description
| --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | The decimal number representing *DATE/UDATE for the given format.

### DateTime NormalizeYY([DateTime formatDate](https://docs.microsoft.com/en-us/dotnet/api/system.datetime))

Normalize the year portion of a DateTime value taken as a a two-digit year to the proper year in the range 1940 - 2039.

```cs
DateTime NormalizeYY(DateTime formatDate)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | formatDate | The DateTime value.

#### Returns

| Type | Description
| --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | The DateTime value with the year in the 1940-2039 range.

### DateTime SubtractDuration([DateTime dateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [double duration](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [int durationCode](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [bool justTheTime](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

RPG's SUBDUR. Subtracts a duration span from a DateTime value.

```cs
DateTime SubtractDuration(DateTime dateTime, double duration, int durationCode, bool justTheTime)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | dateTime | The DateTime value.
| [Double](https://learn.microsoft.com/en-us/dotnet/api/system.double?view=net-8.0) | duration | The duraction span.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | durationCode | The duration code, as an integer (see: ASNA.QSys.Runtime.DateTimeOps.DurationCode)
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | justTheTime | True if the DateTime value represents an RPG time.

#### Returns

| Type | Description
| --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | The result of subtracting the specified duration to dateTime.

### DateTime TruncToMicroseconds([DateTime theStamp](https://docs.microsoft.com/en-us/dotnet/api/system.datetime))

Truncate theStamp to the closest Microsecond (make it ISO format).

```cs
DateTime TruncToMicroseconds(DateTime theStamp)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | theStamp | TruncToMicroseconds param theStamp.

#### Returns

| Type | Description
| --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | TruncToMicroseconds returns.
