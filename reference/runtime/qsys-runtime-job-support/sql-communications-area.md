---
title: "SQL_CommunicationsArea class  | QSYS API Reference Guide"
description: "Implements SQLCA (SQL communications area) "
last_modified_at: 2024-08-09T17:25:29Z
---

Implements SQLCA (SQL communications area)

**Namespace:** ASNA.QSys.Runtime.JobSupport
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [SQL_CommunicationsArea](#sql-communicationsareastring)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Initializes a new SQL_CommunicationsArea class instance.
| [SQL_CommunicationsArea](#sql-communicationsareastring-sqlexception)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [SqlException](https://learn.microsoft.com/en-us/dotnet/api/system.data.sqlclient.sqlexception?view=net-8.0)) | Initializes a new SQL_CommunicationsArea class instance for the last SQL operation that caused Error condition.
| [SQL_CommunicationsArea](#sql-communicationsareastring-int32-string)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Initializes a new SQL_CommunicationsArea class instance for the last SQL operation.
| [SQL_CommunicationsArea](#sql-communicationsareastring-int32-string-exception)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception)) | Initializes a new SQL_CommunicationsArea class instance for the last SQL operation that caused an Error condition.

### SQL_CommunicationsArea([String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Initializes a new SQL_CommunicationsArea class instance.

```cs
SQL_CommunicationsArea(String)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | cmdText | The SQL command.

### SQL_CommunicationsArea([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [SqlException](https://learn.microsoft.com/en-us/dotnet/api/system.data.sqlclient.sqlexception?view=net-8.0))

Initializes a new SQL_CommunicationsArea class instance for the last SQL operation that caused Error condition.

```cs
SQL_CommunicationsArea(String, SqlException)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | cmdText | The SQL command.
| [SqlException](https://learn.microsoft.com/en-us/dotnet/api/system.data.sqlclient.sqlexception?view=net-8.0) | sqlException | The Exception thrown by the .NET SQL Engine.

### SQL_CommunicationsArea([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Initializes a new SQL_CommunicationsArea class instance for the last SQL operation.

```cs
SQL_CommunicationsArea(String, Int32, String)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | cmdText | The SQL command.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | iSeriesCode | The resulting Code as defined by IBM i.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | iSeriesState | The resulting State as defined by IBM i.

### SQL_CommunicationsArea([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception))

Initializes a new SQL_CommunicationsArea class instance for the last SQL operation that caused an Error condition.

```cs
SQL_CommunicationsArea(String, Int32, String, Exception)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | cmdText | The SQL command.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | iSeriesCode | The resulting Code as defined by IBM i.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | iSeriesState | >The resulting State as defined by IBM i.
| [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception) | e | >The Exception thrown by the .NET SQL Engine.

## Properties

| Type | Name | Description
| --- | --- | --- 
| [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception) | SQL_Exception | Gets or Sets the .NET equivalent Exception thrown by the SQL Engine during execution of last SQL operation. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | SQLCOD | Gets or sets the the SQL return code: 0 = successful execution, positive = successful execution but with warnings, negative = error condition. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | SQLCODE | SQLCOD alias added to RPG ILE. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | SqlCommandText | Gets or Sets the SQL command text used in the last SQl operation. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | SQLSTATE | SQLSTT alias added to RPG ILE. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | SQLSTT | Gets or Sets the result of SQL Procedure execution. The Message or Code uses a 5 character numeric value. |
