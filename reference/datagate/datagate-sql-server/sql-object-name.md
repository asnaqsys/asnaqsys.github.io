---
title: SqlObjectName class
description: "Represents a SQL object name. "
last_modified_at: 2024-06-26T20:26:58Z
---

Represents a SQL object name.

**Namespace:** ASNA.DataGate.SqlServer
**Assembly:** ASNA.QSys.DataGate.Client.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>

## Remarks
This class is used to encapsulate the name of a SQL object, such as a table or a column. It provides methods to parse and format SQL object names.

<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [SqlObjectName](#sqlobjectnamestring)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Initializes a new instance of the  class with the specified object name.
| [SqlObjectName](#sqlobjectnamestring-string)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Initializes a new instance of the  class with the specified owner and object names.
| [SqlObjectName](#sqlobjectnamestring-string-string)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Initializes a new instance of the  class with the specified database, owner, and object names.
| [SqlObjectName](#sqlobjectnamestring-string-string-string)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Initializes a new instance of the  class with the specified server, database, owner, and object names.

### SqlObjectName([String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Initializes a new instance of the  class with the specified object name.

```cs
SqlObjectName(String)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | name | The name of the SQL object.

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

## Properties

| Type | Name | Description
| --- | --- | --- 
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | Database | Gets the name of the database. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | Object | Gets the name of the object. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | Owner | Gets the name of the owner. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | Server | Gets the name of the server. |

## Methods

| Signature | Description |
| --- | --- |
| [Parse](#sqlobjectname-parsestring-input)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Parses a string into a SqlObjectName.

### SqlObjectName Parse([string input](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Parses a string into a SqlObjectName.

```cs
SqlObjectName Parse(string input)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | input | The string to parse.

#### Returns

| Type | Description
| --- | ---
| [SqlObjectName](/reference/datagate/datagate-sql-server/sql-object-name.html) | A SqlObjectName that represents the parsed string.
