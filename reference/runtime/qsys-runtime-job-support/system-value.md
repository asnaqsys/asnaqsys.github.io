---
title: "SystemValue class             | QSYS API Reference Guide"
description: "Provides System Value attributes. "
last_modified_at: 2024-08-08T21:41:46Z
---

Provides System Value attributes.

**Namespace:** ASNA.QSys.Runtime.JobSupport
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>

## Properties

| Type | Name | Description
| --- | --- | --- 
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | QCENTURY | Returns Century value for the system date Char(1). '0' indicated years 19 XX.'1' indicates years 20 XX. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | QCURSYM | Returns Currency symbol Char(1). |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | QDATE | Returns System date Char(6). |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | QDATETIME | Returns - System date and time Char(20).This is the date and time for the local system time as a single value.Retrieving or changing this value is similar to retrieving or changing QDATE and QTIME in a single operation.The format of the field isYYYYMMDDHHNNSSXXXXXX where YYYY is the year, MM is the month, DD is the day, HH is the hours, NN is the minutes, SS is the seconds, and XXXXXX is the microseconds.      |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | QDATFMT | Returns Date format Char(3). |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | QDATSEP | Returns Date separator Char(1). |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | QDAY | Returns Day of the month Char(2). Day of the year if the system date format is Julian. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | QDAYOFWEEK | Returns The day of the week Char(4). *SUN - Sunday*MON - Monday*TUE - Tuesday*WED - Wednesday*THU - Thursday*FRI - Friday*SAT - Saturday |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | QHOUR | Returns Hour of the day Char(2). |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | QMINUTE | Returns Minute of the hour Char(2). |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | QMONTH | Returns Month of the year Char(2). Not used for Julian dates. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | QSECOND | Returns Second of the minute Char(2). |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | QTIME | Returns Time of day Char(9). |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | QTIMSEP | Returns Time separator Char(1). |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | QTIMZON | Returns Time zone Char(10). For example: QN0600UTCS - GMT-6 - US Central Standard Time. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | QYEAR | Returns Year Char(2). |
