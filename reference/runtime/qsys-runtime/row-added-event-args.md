---
title: "RowAddedEventArgs class       | QSYS API Reference Guide"
description: "Holds information that the RowAddedEvent requires. "
last_modified_at: 2024-08-08T21:41:46Z
---

Holds information that the RowAddedEvent requires.

**Namespace:** ASNA.QSys.Runtime
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [EventArgs](https://learn.microsoft.com/en-us/dotnet/api/system.eventargs?view=net-8.0)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [RowAddedEventArgs](#rowaddedeventargsstring)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Constructs a RowAddedEventArgs object that contains information about row added.

### RowAddedEventArgs([String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Constructs a RowAddedEventArgs object that contains information about row added.

```cs
RowAddedEventArgs(String)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatName | Record format name where the row was added.

## Properties

| Type | Name | Description
| --- | --- | --- 
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | formatName | Record format name where the row was added. |
