---
title: "DatabaseAttributes class"
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
| [DatabaseAttributes](database-attributes-ctor.html#databaseattributes-string-string-string-string-string-string-int32-int32-boolean)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Initializes a new instance of the DatabaseAttributes class with the specified parameters.

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

