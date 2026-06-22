---
title: "EndStreamModeException Constructors"
description: "Initializes a new instance of the class."
---

## Definition

**Namespace:** ASNA.DataGate.DataLink  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Initializes a new instance of the class.

## Overloads

| Name | Description |
| --- | --- |
| [EndStreamModeException](#endstreammodeexception)() | Initializes a new instance of the class. |
| [EndStreamModeException](#endstreammodeexception-string)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Initializes a new instance of the class with a specified error message. |
| [EndStreamModeException](#endstreammodeexception-string-exception)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception)) | Initializes a new instance of the class with a specified error message and a reference to the inner exception that is the cause of this exception. |

<a id="endstreammodeexception"></a>
### EndStreamModeException()

Initializes a new instance of the  class.

```cs
EndStreamModeException()
```

<a id="endstreammodeexception-string"></a>
### EndStreamModeException([String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Initializes a new instance of the  class with a specified error message.

```cs
EndStreamModeException(String)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | message | The message that describes the error.

<a id="endstreammodeexception-string-exception"></a>
### EndStreamModeException([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception))

Initializes a new instance of the  class with a specified error message and a reference to the inner exception that is the cause of this exception.

```cs
EndStreamModeException(String, Exception)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | message | The error message that explains the reason for the exception.
| [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception) | innerException | The exception that is the cause of the current exception, or a null reference if no inner exception is specified.

## See Also
- [EndStreamModeException class](end-stream-mode-exception.html)
