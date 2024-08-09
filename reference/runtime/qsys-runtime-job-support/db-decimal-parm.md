---
title: "DBDecimalParm class           | QSYS API Reference Guide"
description: "Represents a parameter for a decimal type. "
last_modified_at: 2024-08-09T16:18:25Z
---

Represents a parameter for a decimal type.

**Namespace:** ASNA.QSys.Runtime.JobSupport
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [DBParm](/reference/runtime/qsys-runtime-job-support/db-parm.html) --> [DBScaledParm](/reference/runtime/qsys-runtime-job-support/db-scaled-parm.html)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [DBDecimalParm](#dbdecimalparmdecimal-int32-int32)([Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Initializes a new instance of DBDecimalParm class.

### DBDecimalParm([Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

Initializes a new instance of DBDecimalParm class.

```cs
DBDecimalParm(Decimal, Int32, Int32)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | Value | Initial decimal value.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | Length | Decimal value fixed length.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | Scale | Decimal value scale.
