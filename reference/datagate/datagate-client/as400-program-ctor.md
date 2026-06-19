---
title: "As400Program Constructors"
description: "Initializes a new instance of the class."
---

## Definition

**Namespace:** ASNA.DataGate.Client  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Initializes a new instance of the class.

## Overloads

| Name | Description |
| --- | --- |
| [As400Program](#as400program)() | Initializes a new instance of the class. |
| [As400Program](#as400program-adgconnection)([AdgConnection](/reference/datagate/datagate-client/adg-connection.html)) | Initializes a new instance of the class with the specified connection. |
| [As400Program](#as400program-adgconnection-string)([AdgConnection](/reference/datagate/datagate-client/adg-connection.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Initializes a new instance of the class with the specified connection and program path. |

<a id="as400program"></a>
### As400Program()

Initializes a new instance of the  class.

```cs
As400Program()
```

<a id="as400program-adgconnection"></a>
### As400Program([AdgConnection](/reference/datagate/datagate-client/adg-connection.html))

Initializes a new instance of the  class with the specified connection.

```cs
As400Program(AdgConnection)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [AdgConnection](/reference/datagate/datagate-client/adg-connection.html) | connection | The connection to be used by the program.

<a id="as400program-adgconnection-string"></a>
### As400Program([AdgConnection](/reference/datagate/datagate-client/adg-connection.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Initializes a new instance of the  class with the specified connection and program path.

```cs
As400Program(AdgConnection, String)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [AdgConnection](/reference/datagate/datagate-client/adg-connection.html) | connection | The connection to be used by the program.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | programPath | The path of the program to be executed.

## See Also
- [As400Program class](as400-program.html)
