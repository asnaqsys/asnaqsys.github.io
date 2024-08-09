---
title: "SqlPreparedStatement class    | QSYS API Reference Guide"
description: "Used to implement SQL PREPARE statements. "
last_modified_at: 2024-08-09T17:25:29Z
---

Used to implement SQL PREPARE statements.

**Namespace:** ASNA.QSys.Runtime.JobSupport
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [SqlPreparedStatement](#sqlpreparedstatementdbconnection-string-dbparm)([DbConnection](https://learn.microsoft.com/en-us/dotnet/api/system.data.common.dbconnection?view=net-8.0), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [DBParm\[\]](/reference/runtime/qsys-runtime-job-support/db-parm.html)) | Initializes a new instance of SqlPreparedStatement.
| [SqlPreparedStatement](#sqlpreparedstatementdbconnection-string)([DbConnection](https://learn.microsoft.com/en-us/dotnet/api/system.data.common.dbconnection?view=net-8.0), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Initializes a new instance of SqlPreparedStatement.

### SqlPreparedStatement([DbConnection](https://learn.microsoft.com/en-us/dotnet/api/system.data.common.dbconnection?view=net-8.0), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [DBParm\[\]](/reference/runtime/qsys-runtime-job-support/db-parm.html))

Initializes a new instance of SqlPreparedStatement.

```cs
SqlPreparedStatement(DbConnection, String, DBParm[])
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DbConnection](https://learn.microsoft.com/en-us/dotnet/api/system.data.common.dbconnection?view=net-8.0) | sqlConnection | Database Connection.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | sqlText | SQL command text.
| [DBParm\[\]](/reference/runtime/qsys-runtime-job-support/db-parm.html) | parameters | Values corresponding to the variables used in the SQL command 

### SqlPreparedStatement([DbConnection](https://learn.microsoft.com/en-us/dotnet/api/system.data.common.dbconnection?view=net-8.0), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Initializes a new instance of SqlPreparedStatement.

```cs
SqlPreparedStatement(DbConnection, String)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DbConnection](https://learn.microsoft.com/en-us/dotnet/api/system.data.common.dbconnection?view=net-8.0) | sqlConnection | Database Connection.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | sqlText | SQL command text.

## Properties

| Type | Name | Description
| --- | --- | --- 
| [IDbCommand](https://learn.microsoft.com/en-us/dotnet/api/system.data.idbcommand?view=net-8.0) | cmd | Gets the IDbCommand command representing the Prepared Statement. |
| [SQL_CommunicationsArea](/reference/runtime/qsys-runtime-job-support/sql-communications-area.html) | SQLCA | Gets the SQL Communications Area instance. |
