---
title: "NoDbNameException Constructors"
description: "Initializes a new instance of the NoDbNameException class."
---

## Definition

**Namespace:** ASNA.DataGate.Common  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Initializes a new instance of the NoDbNameException class.

## Overloads

| Name | Description |
| --- | --- |
| [NoDbNameException](#nodbnameexception)() | Initializes a new instance of the NoDbNameException class. |
| [NoDbNameException](#nodbnameexception-string)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Initializes a new instance of the NoDbNameException class with a specified database name. |
| [NoDbNameException](#nodbnameexception-string-exception)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception)) | Initializes a new instance of the NoDbNameException class with a specified database name and a reference to the inner exception that is the cause of this exception. |

<a id="nodbnameexception"></a>
### NoDbNameException()

Initializes a new instance of the NoDbNameException class.

```cs
NoDbNameException()
```

<a id="nodbnameexception-string"></a>
### NoDbNameException([String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Initializes a new instance of the NoDbNameException class with a specified database name.

```cs
NoDbNameException(String)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | dbname | The name of the database that caused the exception.

<a id="nodbnameexception-string-exception"></a>
### NoDbNameException([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception))

Initializes a new instance of the NoDbNameException class with a specified database name and a reference to the inner exception that is the cause of this exception.

```cs
NoDbNameException(String, Exception)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | dbname | The name of the database that caused the exception.
| [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception) | inner | The exception that is the cause of the current exception, or a null reference if no inner exception is specified.

## See Also
- [NoDbNameException class](no-db-name-exception.html)
