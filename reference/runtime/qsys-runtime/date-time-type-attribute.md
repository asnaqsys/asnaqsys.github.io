---
title: "DateTimeTypeAttribute class   | QSYS API Reference Guide"
description: "A non-RPG class may stamp a System.DateTime member with this attribute to be considered as a fixed-sized date/time/timestamp field by a consumer RPG p"
last_modified_at: 2024-08-09T17:25:29Z
---

A non-RPG class may stamp a System.DateTime member with this attribute to be considered as a fixed-sized date/time/timestamp field by a consumer RPG program.

**Namespace:** ASNA.QSys.Runtime
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [Attribute](https://docs.microsoft.com/en-us/dotnet/api/system.attribute)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [DateTimeTypeAttribute](#datetimetypeattributeint32-int32-int32)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Initializes a DateTimeTypeAttribute object. This attribute describes the implied fixed date/time kind, format, and separator of a DateTime value.

### DateTimeTypeAttribute([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

Initializes a DateTimeTypeAttribute object. This attribute describes the implied fixed date/time kind, format, and separator of a DateTime value.

```cs
DateTimeTypeAttribute(Int32, Int32, Int32)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | kind | The DateTimeDataKind of this item.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | format | The DateTimeFormat of this item.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | separator | The DateTimeSeparator of this item.

## Properties

| Type | Name | Description
| --- | --- | --- 
| [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html) | Format | Gets the DateTimeFormat (*ISO, *USA, *HMS, etc.) of this item. |
| [DateTimeDataKind](/reference/runtime/qsys-runtime/date-time-data-kind.html) | Kind | Gets the DateTimeDataKind (date, time, or timestamp) of this item. |
| [DateTimeSeparator](/reference/runtime/qsys-runtime/date-time-separator.html) | Separator | Gets the DateTimeSeparator ('/', '.', ':', etc.) of this item. |
