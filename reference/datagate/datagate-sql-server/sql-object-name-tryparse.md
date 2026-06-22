---
title: "SqlObjectName.TryParse Method"
description: "Tries to parse a string into a SqlObjectName."
---

## Definition

**Namespace:** ASNA.DataGate.SqlServer  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Tries to parse a string into a SqlObjectName.

<a id="bool-tryparse-string-input-sqlobjectname-output"></a>
## bool TryParse(string input, SqlObjectName& output)

Tries to parse a string into a SqlObjectName.

#### Remarks
This method is used to convert a string into a SqlObjectName. The string should be in the format of a SQL object name, such as "server.database.schema.object". If the string cannot be parsed, the method returns false and assigns null to the result parameter.

```cs
bool TryParse(string input, SqlObjectName& output)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | input | The string to parse.
| [SqlObjectName&](/reference/datagate/datagate-sql-server/sql-object-name.html) | output | When this method returns, contains the SqlObjectName equivalent to the string contained in input, if the conversion succeeded, or null if the conversion failed.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | True if the input was converted successfully; otherwise, false.

## See Also
- [SqlObjectName class](sql-object-name.html)
