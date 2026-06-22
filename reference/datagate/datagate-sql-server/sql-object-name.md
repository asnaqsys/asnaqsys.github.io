---
title: "SqlObjectName class"
description: "Represents a SQL object name. "
last_modified_at: 2024-08-09T17:25:07Z
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
| [SqlObjectName](sql-object-name-ctor.html#sqlobjectname-string)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Initializes a new instance of the  class with the specified object name.
| [SqlObjectName](sql-object-name-ctor.html#sqlobjectname-string-string)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Initializes a new instance of the  class with the specified owner and object names.
| [SqlObjectName](sql-object-name-ctor.html#sqlobjectname-string-string-string)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Initializes a new instance of the  class with the specified database, owner, and object names.
| [SqlObjectName](sql-object-name-ctor.html#sqlobjectname-string-string-string-string)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Initializes a new instance of the  class with the specified server, database, owner, and object names.

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
| [Parse](sql-object-name-parse.html#sqlobjectname-parse-string-input)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Parses a string into a SqlObjectName.
| [TryParse](sql-object-name-tryparse.html#bool-tryparse-string-input-sqlobjectname-output)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [SqlObjectName&](/reference/datagate/datagate-sql-server/sql-object-name.html)) | Tries to parse a string into a SqlObjectName.

