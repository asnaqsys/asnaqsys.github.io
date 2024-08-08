---
title: "QueryCursor class             | QSYS API Reference Guide"
description: "Represents the SQL Query Cursor. "
last_modified_at: 2024-08-08T21:41:46Z
---

Represents the SQL Query Cursor.

**Namespace:** ASNA.QSys.Runtime.JobSupport
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [QueryCursor](#querycursordbconnection-string)([DbConnection](https://learn.microsoft.com/en-us/dotnet/api/system.data.common.dbconnection?view=net-8.0), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Initializes a new instance of QueryCursor class.
| [QueryCursor](#querycursorsqlpreparedstatement)([SqlPreparedStatement](/reference/runtime/qsys-runtime-job-support/sql-prepared-statement.html)) | Initializes a new instance of QueryCursor class.
| [QueryCursor](#querycursordbconnection-string-dbparm)([DbConnection](https://learn.microsoft.com/en-us/dotnet/api/system.data.common.dbconnection?view=net-8.0), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [DBParm\[\]](/reference/runtime/qsys-runtime-job-support/db-parm.html)) | Initializes a new instance of QueryCursor class.

### QueryCursor([DbConnection](https://learn.microsoft.com/en-us/dotnet/api/system.data.common.dbconnection?view=net-8.0), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Initializes a new instance of QueryCursor class.

```cs
QueryCursor(DbConnection, String)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DbConnection](https://learn.microsoft.com/en-us/dotnet/api/system.data.common.dbconnection?view=net-8.0) | sqlConnection | SQL Connection.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | SelectStatement | SELECT statement.

### QueryCursor([SqlPreparedStatement](/reference/runtime/qsys-runtime-job-support/sql-prepared-statement.html))

Initializes a new instance of QueryCursor class.

```cs
QueryCursor(SqlPreparedStatement)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [SqlPreparedStatement](/reference/runtime/qsys-runtime-job-support/sql-prepared-statement.html) | preparedStatement | Prepared statement initializer.

### QueryCursor([DbConnection](https://learn.microsoft.com/en-us/dotnet/api/system.data.common.dbconnection?view=net-8.0), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [DBParm\[\]](/reference/runtime/qsys-runtime-job-support/db-parm.html))

Initializes a new instance of QueryCursor class.

```cs
QueryCursor(DbConnection, String, DBParm[])
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DbConnection](https://learn.microsoft.com/en-us/dotnet/api/system.data.common.dbconnection?view=net-8.0) | sqlConnection | SQL Connection.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | selectStatementWithParms | SELECT Statement (with parameters).
| [DBParm\[\]](/reference/runtime/qsys-runtime-job-support/db-parm.html) | parameters | Parameter values.

## Properties

| Type | Name | Description
| --- | --- | --- 
| [QueryResults](/reference/runtime/qsys-runtime-job-support/query-results.html) | QueryResults | Gets the Cursor's Query Results. |
| [ScrollTypes](/reference/runtime/qsys-runtime-job-support/scroll-types.html) | ScrollType | Gets the Cursor's scroll type. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | selectStatement | Gets the SELECT statement. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | SelectStatement | Gets the SELECT statement. |
| [SQL_CommunicationsArea](/reference/runtime/qsys-runtime-job-support/sql-communications-area.html) | SQLCA | The SQL Communications Area for the Cursor. |

## Methods

| Signature | Description |
| --- | --- |
| [Close()](#void-close) | Closes the Cursor. Does not throw error if the cursor had not been opened.
| [FetchAbsolute](#bool-fetchabsoluteint-expectedresults-int-absoluterow)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Fetches rows until it gets to the indicated absolute row.
| [FetchRelative](#bool-fetchrelativeint-expectedresults-int-relativerowcount)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Fetches rows in a relative way.
| [Open()](#void-open) | Opens the Cursor. Throws exception if cursor already opened.
| [Open](#void-opendbparm--parameters)([DBParm\[\]](/reference/runtime/qsys-runtime-job-support/db-parm.html)) | Opens the Cursor using the parameters passed in.
| [SetSelectStatement](#void-setselectstatementstring-statement)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Initializes a new instance of SetSelectStatement class.

### void Close()

Closes the Cursor. Does not throw error if the cursor had not been opened.

```cs
void Close()
```

### bool FetchAbsolute([int expectedResults](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int absoluteRow](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Fetches rows until it gets to the indicated absolute row.

```cs
bool FetchAbsolute(int expectedResults, int absoluteRow)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | expectedResults | Expected row count read.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | absoluteRow | Absolute row number.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | True if the fetch was successful.

### bool FetchRelative([int expectedResults](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int relativeRowCount](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Fetches rows in a relative way.

```cs
bool FetchRelative(int expectedResults, int relativeRowCount)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | expectedResults | Expected number of rows read after operation.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | relativeRowCount | Number of rows - from current row.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | True if the fetch was successful.

### void Open()

Opens the Cursor. Throws exception if cursor already opened.

```cs
void Open()
```

### void Open([DBParm\[\] parameters](/reference/runtime/qsys-runtime-job-support/db-parm.html))

Opens the Cursor using the parameters passed in.

```cs
void Open(DBParm[] parameters)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DBParm\[\]](/reference/runtime/qsys-runtime-job-support/db-parm.html) | parameters | The array of parameters.

### void SetSelectStatement([string statement](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Initializes a new instance of SetSelectStatement class.

```cs
void SetSelectStatement(string statement)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | statement | SELECT statement.
