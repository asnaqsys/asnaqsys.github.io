---
title: "DatabaseAttributes class      | QSYS API Reference Guide"
description: "Database properties, as reported by ISourceProvider.DatabaseAttributes. "
last_modified_at: 2024-08-09T17:25:07Z
---

Database properties, as reported by ISourceProvider.DatabaseAttributes.

**Namespace:** ASNA.DataGate.Providers
**Assembly:** ASNA.QSys.DataGate.Client.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>
## Thread Safety

Any public static (Shared) members of this type are safe for multithreaded operations. Any instance members are not guaranteed to be thread safe.


## Constructors

| Name | Description |
| --- | --- |
| [DatabaseAttributes](#databaseattributesstring-string-string-string-string-string-int32-int32-boolean)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Initializes a new instance of the DatabaseAttributes class with the specified parameters.

### DatabaseAttributes([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Initializes a new instance of the DatabaseAttributes class with the specified parameters.

```cs
DatabaseAttributes(String, String, String, String, String, String, Int32, Int32, Boolean)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | database | The database name.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | proxyName | The proxy name.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | proxyVersion | The proxy version.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | operatingSystem | The operating system.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | hardware | The hardware.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | label | The label.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | totalSeats | The total number of seats.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | busySeats | The number of busy seats.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | secure | Whether the connection is secure.

## Properties

| Type | Name | Description
| --- | --- | --- 
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | BusySeats | Gets or sets the number of busy seats. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | Database | Gets or sets the name of the database. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | Hardware | Gets or sets the hardware information. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | OperatingSystem | Gets or sets the operating system. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | OriginalLabel | Gets or sets the original label. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | ProxyName | Gets or sets the name of the proxy. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | ProxyVersion | Gets or sets the version of the proxy. |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | Secure | Gets or sets a value indicating whether the connection is secure. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | TotalSeats | Gets or sets the total number of seats. |
