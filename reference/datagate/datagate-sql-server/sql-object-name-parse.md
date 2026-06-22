---
title: "SqlObjectName.Parse Method"
description: "Parses a string into a SqlObjectName."
---

## Definition

**Namespace:** ASNA.DataGate.SqlServer  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Parses a string into a SqlObjectName.

<a id="sqlobjectname-parse-string-input"></a>
## SqlObjectName Parse(string input)

Parses a string into a SqlObjectName.

#### Remarks
This method is used to convert a string into a SqlObjectName. The string should be in the format of a SQL object name, such as "server.database.schema.object". If the string cannot be parsed, an exception is thrown.

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

## See Also
- [SqlObjectName class](sql-object-name.html)
