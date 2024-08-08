---
title: "DBScaledParm class            | QSYS API Reference Guide"
description: "Represents a parameter for a Scalar type. "
last_modified_at: 2024-08-08T21:41:46Z
---

Represents a parameter for a Scalar type.

**Namespace:** ASNA.QSys.Runtime.JobSupport
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [DBParm](/reference/runtime/qsys-runtime-job-support/db-parm.html)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [DBScaledParm](#dbscaledparmdbtype-int32-int32)([DbType](https://learn.microsoft.com/en-us/dotnet/api/system.data.dbtype?view=net-8.0), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Initializes a new instance of DBScaledParm class.
| [DBScaledParm](#dbscaledparmdbtype-object-int32-int32)([DbType](https://learn.microsoft.com/en-us/dotnet/api/system.data.dbtype?view=net-8.0), [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Initializes a new instance of DBScaledParm class.
| [DBScaledParm](#dbscaledparmdbtype-parameterdirection-object-int32-int32)([DbType](https://learn.microsoft.com/en-us/dotnet/api/system.data.dbtype?view=net-8.0), [ParameterDirection](https://learn.microsoft.com/en-us/dotnet/api/system.data.parameterdirection?view=net-8.0), [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Initializes a new instance of DBScaledParm class.

### DBScaledParm([DbType](https://learn.microsoft.com/en-us/dotnet/api/system.data.dbtype?view=net-8.0), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

Initializes a new instance of DBScaledParm class.

```cs
DBScaledParm(DbType, Int32, Int32)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DbType](https://learn.microsoft.com/en-us/dotnet/api/system.data.dbtype?view=net-8.0) | Type | Data Type.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | Length | Data Length.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | Scale | Data Scale.

### DBScaledParm([DbType](https://learn.microsoft.com/en-us/dotnet/api/system.data.dbtype?view=net-8.0), [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

Initializes a new instance of DBScaledParm class.

```cs
DBScaledParm(DbType, Object, Int32, Int32)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DbType](https://learn.microsoft.com/en-us/dotnet/api/system.data.dbtype?view=net-8.0) | Type | Data Type.
| [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) | Value | Initial data value.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | Length | Data Length.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | Scale | Data Scale.

### DBScaledParm([DbType](https://learn.microsoft.com/en-us/dotnet/api/system.data.dbtype?view=net-8.0), [ParameterDirection](https://learn.microsoft.com/en-us/dotnet/api/system.data.parameterdirection?view=net-8.0), [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

Initializes a new instance of DBScaledParm class.

```cs
DBScaledParm(DbType, ParameterDirection, Object, Int32, Int32)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DbType](https://learn.microsoft.com/en-us/dotnet/api/system.data.dbtype?view=net-8.0) | Type | Data Type.
| [ParameterDirection](https://learn.microsoft.com/en-us/dotnet/api/system.data.parameterdirection?view=net-8.0) | Direction | Parameter Direction.
| [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) | Value | Initial data value.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | Length | Data Length.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | Scale | Data Scale.
