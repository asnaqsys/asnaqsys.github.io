---
title: "DBStrParm class               | QSYS API Reference Guide"
description: "Represents a String SQL Parameter. "
last_modified_at: 2024-08-09T17:25:29Z
---

Represents a String SQL Parameter.

**Namespace:** ASNA.QSys.Runtime.JobSupport
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [DBParm](/reference/runtime/qsys-runtime-job-support/db-parm.html)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [DBStrParm](#dbstrparmdbtype-int32)([DbType](https://learn.microsoft.com/en-us/dotnet/api/system.data.dbtype?view=net-8.0), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Initializes a new instance of DBStrParm class.
| [DBStrParm](#dbstrparmdbtype-object-int32)([DbType](https://learn.microsoft.com/en-us/dotnet/api/system.data.dbtype?view=net-8.0), [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Initializes a new instance of DBStrParm class.
| [DBStrParm](#dbstrparmdbtype-parameterdirection-object-int32)([DbType](https://learn.microsoft.com/en-us/dotnet/api/system.data.dbtype?view=net-8.0), [ParameterDirection](https://learn.microsoft.com/en-us/dotnet/api/system.data.parameterdirection?view=net-8.0), [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Initializes a new instance of DBStrParm class.

### DBStrParm([DbType](https://learn.microsoft.com/en-us/dotnet/api/system.data.dbtype?view=net-8.0), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

Initializes a new instance of DBStrParm class.

```cs
DBStrParm(DbType, Int32)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DbType](https://learn.microsoft.com/en-us/dotnet/api/system.data.dbtype?view=net-8.0) | Type | Data Type.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | Size | String fixed length.

### DBStrParm([DbType](https://learn.microsoft.com/en-us/dotnet/api/system.data.dbtype?view=net-8.0), [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

Initializes a new instance of DBStrParm class.

```cs
DBStrParm(DbType, Object, Int32)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DbType](https://learn.microsoft.com/en-us/dotnet/api/system.data.dbtype?view=net-8.0) | Type | Data Type.
| [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) | Value | Initial string value.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | Size | String fixed length.

### DBStrParm([DbType](https://learn.microsoft.com/en-us/dotnet/api/system.data.dbtype?view=net-8.0), [ParameterDirection](https://learn.microsoft.com/en-us/dotnet/api/system.data.parameterdirection?view=net-8.0), [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

Initializes a new instance of DBStrParm class.

```cs
DBStrParm(DbType, ParameterDirection, Object, Int32)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DbType](https://learn.microsoft.com/en-us/dotnet/api/system.data.dbtype?view=net-8.0) | Type | Data Type.
| [ParameterDirection](https://learn.microsoft.com/en-us/dotnet/api/system.data.parameterdirection?view=net-8.0) | Direction | Parameter Direction.
| [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) | Value | Initial Value.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | Size | String fixed length.
