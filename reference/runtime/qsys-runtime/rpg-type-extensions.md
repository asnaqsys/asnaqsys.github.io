---
title: "RpgTypeExtensions class       | QSYS API Reference Guide"
description: "Provides extension methods for RPG types, including methods for moving and manipulating fixed-length strings and decimal numbers. "
last_modified_at: 2024-08-08T21:41:46Z
---

Provides extension methods for RPG types, including methods for moving and manipulating fixed-length strings and decimal numbers.

**Namespace:** ASNA.QSys.Runtime
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>

## Methods

| Signature | Description |
| --- | --- |
| [RemoveDate](#datetime-removedatedatetime-from)([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime)) | RemoveDate extension.
| [RemoveTime](#datetime-removetimedatetime-from)([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime)) | RemoveTime extension.

### DateTime RemoveDate([DateTime from](https://docs.microsoft.com/en-us/dotnet/api/system.datetime))

RemoveDate extension.

```cs
DateTime RemoveDate(DateTime from)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | from | RemoveDate from param.

#### Returns

| Type | Description
| --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | DateTime result.

### DateTime RemoveTime([DateTime from](https://docs.microsoft.com/en-us/dotnet/api/system.datetime))

RemoveTime extension.

```cs
DateTime RemoveTime(DateTime from)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | from | RemoveTime from param.

#### Returns

| Type | Description
| --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | DateTime result.
