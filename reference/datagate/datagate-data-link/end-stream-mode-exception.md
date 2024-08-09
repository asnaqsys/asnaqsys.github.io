---
title: "EndStreamModeException class  | QSYS API Reference Guide"
description: "Represents errors that occur when the end of a stream mode is reached unexpectedly. "
last_modified_at: 2024-08-09T17:25:07Z
---

Represents errors that occur when the end of a stream mode is reached unexpectedly.

**Namespace:** ASNA.DataGate.DataLink
**Assembly:** ASNA.QSys.DataGate.Client.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [EndStreamModeException()](#endstreammodeexception) | Initializes a new instance of the  class.
| [EndStreamModeException](#endstreammodeexceptionstring)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Initializes a new instance of the  class with a specified error message.
| [EndStreamModeException](#endstreammodeexceptionstring-exception)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception)) | Initializes a new instance of the  class with a specified error message and a reference to the inner exception that is the cause of this exception.

### EndStreamModeException()

Initializes a new instance of the  class.

```cs
EndStreamModeException()
```

### EndStreamModeException([String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Initializes a new instance of the  class with a specified error message.

```cs
EndStreamModeException(String)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | message | The message that describes the error.

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
