---
title: "DBParm class                  | QSYS API Reference Guide"
description: "Represents a SQL Parameter (used as base to specific parameter type) "
last_modified_at: 2024-08-08T21:41:46Z
---

Represents a SQL Parameter (used as base to specific parameter type)

**Namespace:** ASNA.QSys.Runtime.JobSupport
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [DBParm](#dbparmdbtype-parameterdirection-object)([DbType](https://learn.microsoft.com/en-us/dotnet/api/system.data.dbtype?view=net-8.0), [ParameterDirection](https://learn.microsoft.com/en-us/dotnet/api/system.data.parameterdirection?view=net-8.0), [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | Initializes a new instance of DBParm parameter.

### DBParm([DbType](https://learn.microsoft.com/en-us/dotnet/api/system.data.dbtype?view=net-8.0), [ParameterDirection](https://learn.microsoft.com/en-us/dotnet/api/system.data.parameterdirection?view=net-8.0), [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object))

Initializes a new instance of DBParm parameter.

```cs
DBParm(DbType, ParameterDirection, Object)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DbType](https://learn.microsoft.com/en-us/dotnet/api/system.data.dbtype?view=net-8.0) | Type | Data Type.
| [ParameterDirection](https://learn.microsoft.com/en-us/dotnet/api/system.data.parameterdirection?view=net-8.0) | Direction | Parameter direction.
| [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) | Value | Parameter Value.
