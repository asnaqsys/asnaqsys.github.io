---
title: "DatabaseCycleFile class       | QSYS API Reference Guide"
description: "Database file that participates in the RPG program Cycle. When a Cycle file record is read from the Database, the file buffer values are not immediate"
last_modified_at: 2024-08-09T16:18:25Z
---

Database file that participates in the RPG program Cycle. When a Cycle file record is read from the Database,
the file buffer values are not immediately copied into the program fields. The RPG cycle explicitly issues a LoadBuffer call
at the proper time within the cycle to load the buffer into the program fields.

**Namespace:** ASNA.QSys.Runtime
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [FileBase](/reference/runtime/qsys-runtime/file-base.html) --> [DatabaseFileBase](/reference/runtime/qsys-runtime/database-file-base.html) --> [DatabaseFile](/reference/runtime/qsys-runtime/database-file.html)
<br>
<br>

## Properties

| Type | Name | Description
| --- | --- | --- 
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | IsPrimary | Gets value indicating that file is a Primary file, otherwise is Secondary. |

## Methods

| Signature | Description |
| --- | --- |
| [LoadBuffer()](#void-loadbuffer) | Copies data from the cycle file buffer to the program fields.
| [open](#void-opendatabase-database-accessmode-accessmode-bool-iscachewrite-bool-iscommit-servercursors-servercursor)([Database](/reference/runtime/qsys-runtime/database.html), [AccessMode](/reference/datagate/datagate-common/access-mode.html), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [ServerCursors](/reference/datagate/datagate-common/server-cursors.html)) | Opens the file.
| [Read()](#void-read) | Reads the next record into the cycle file buffer.

### void LoadBuffer()

Copies data from the cycle file buffer to the program fields.

```cs
void LoadBuffer()
```

### void open([Database database](/reference/runtime/qsys-runtime/database.html), [AccessMode accessMode](/reference/datagate/datagate-common/access-mode.html), [bool isCacheWrite](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [bool isCommit](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [ServerCursors serverCursor](/reference/datagate/datagate-common/server-cursors.html))

Opens the file.

```cs
void open(Database database, AccessMode accessMode, bool isCacheWrite, bool isCommit, ServerCursors serverCursor)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Database](/reference/runtime/qsys-runtime/database.html) | database | Database object.
| [AccessMode](/reference/datagate/datagate-common/access-mode.html) | accessMode | Access mode.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | isCacheWrite | True is writes are to be cached.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | isCommit | True if file participates in commitment control.
| [ServerCursors](/reference/datagate/datagate-common/server-cursors.html) | serverCursor | Server cursor type.

### void Read()

Reads the next record into the cycle file buffer.

```cs
void Read()
```
