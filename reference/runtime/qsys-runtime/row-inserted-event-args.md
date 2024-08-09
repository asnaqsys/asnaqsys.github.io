---
title: "RowInsertedEventArgs class    | QSYS API Reference Guide"
description: "Holds information that the RowInsertedEvent requires. "
last_modified_at: 2024-08-09T17:25:29Z
---

Holds information that the RowInsertedEvent requires.

**Namespace:** ASNA.QSys.Runtime
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [EventArgs](https://learn.microsoft.com/en-us/dotnet/api/system.eventargs?view=net-8.0)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [RowInsertedEventArgs](#rowinsertedeventargsstring-int32)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Constructs a RowInsertedEventArgs object that contains information about row inserted.

### RowInsertedEventArgs([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

Constructs a RowInsertedEventArgs object that contains information about row inserted.

```cs
RowInsertedEventArgs(String, Int32)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatName | Record format name where the row was inserted.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | rrn | Relative record number of the inserted row.

## Properties

| Type | Name | Description
| --- | --- | --- 
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | formatName | Record format name where the row was inserted. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | rrn | Relative record number of the inserted row. |
