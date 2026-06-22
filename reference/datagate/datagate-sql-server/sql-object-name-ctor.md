---
title: "SqlObjectName Constructors"
description: "Initializes a new instance of the class with the specified object name."
---

## Definition

**Namespace:** ASNA.DataGate.SqlServer  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Initializes a new instance of the class with the specified object name.

## Overloads

| Name | Description |
| --- | --- |
| [SqlObjectName](#sqlobjectname-string)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Initializes a new instance of the class with the specified object name. |
| [SqlObjectName](#sqlobjectname-string-string)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Initializes a new instance of the class with the specified owner and object names. |
| [SqlObjectName](#sqlobjectname-string-string-string)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Initializes a new instance of the class with the specified database, owner, and object names. |
| [SqlObjectName](#sqlobjectname-string-string-string-string)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Initializes a new instance of the class with the specified server, database, owner, and object names. |

<a id="sqlobjectname-string"></a>
### SqlObjectName([String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Initializes a new instance of the  class with the specified object name.

```cs
SqlObjectName(String)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | name | The name of the SQL object.

<a id="sqlobjectname-string-string"></a>
### SqlObjectName([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Initializes a new instance of the  class with the specified owner and object names.

```cs
SqlObjectName(String, String)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | owner | The name of the owner.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | name | The name of the object.

<a id="sqlobjectname-string-string-string"></a>
### SqlObjectName([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Initializes a new instance of the  class with the specified database, owner, and object names.

```cs
SqlObjectName(String, String, String)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | database | The name of the database.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | owner | The name of the owner.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | name | The name of the object.

<a id="sqlobjectname-string-string-string-string"></a>
### SqlObjectName([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Initializes a new instance of the  class with the specified server, database, owner, and object names.

```cs
SqlObjectName(String, String, String, String)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | server | The name of the server.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | database | The name of the database.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | owner | The name of the owner.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | name | The name of the object.

## See Also
- [SqlObjectName class](sql-object-name.html)
