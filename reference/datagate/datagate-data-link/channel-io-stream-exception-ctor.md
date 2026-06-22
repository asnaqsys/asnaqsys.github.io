---
title: "ChannelIOStreamException Constructors"
description: "Initializes a new instance of the class."
---

## Definition

**Namespace:** ASNA.DataGate.DataLink  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Initializes a new instance of the class.

## Overloads

| Name | Description |
| --- | --- |
| [ChannelIOStreamException](#channeliostreamexception)() | Initializes a new instance of the class. |
| [ChannelIOStreamException](#channeliostreamexception-string)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Initializes a new instance of the class with a specified error message. |
| [ChannelIOStreamException](#channeliostreamexception-string-exception)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception)) | Initializes a new instance of the class with a specified error message and a reference to the inner exception that is the cause of this exception. |
| [ChannelIOStreamException](#channeliostreamexception-exception)([Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception)) | Initializes a new instance of the class with a reference to the inner exception that is the cause of this exception. |

<a id="channeliostreamexception"></a>
### ChannelIOStreamException()

Initializes a new instance of the  class.

```cs
ChannelIOStreamException()
```

<a id="channeliostreamexception-string"></a>
### ChannelIOStreamException([String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Initializes a new instance of the  class with a specified error message.

```cs
ChannelIOStreamException(String)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | message | The message that describes the error.

<a id="channeliostreamexception-string-exception"></a>
### ChannelIOStreamException([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception))

Initializes a new instance of the  class with a specified error message and a reference to the inner exception that is the cause of this exception.

```cs
ChannelIOStreamException(String, Exception)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | message | The error message that explains the reason for the exception.
| [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception) | innerException | The exception that is the cause of the current exception, or a null reference if no inner exception is specified.

<a id="channeliostreamexception-exception"></a>
### ChannelIOStreamException([Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception))

Initializes a new instance of the  class with a reference to the inner exception that is the cause of this exception.

```cs
ChannelIOStreamException(Exception)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception) | inner | The exception that is the cause of the current exception.

## See Also
- [ChannelIOStreamException class](channel-io-stream-exception.html)
