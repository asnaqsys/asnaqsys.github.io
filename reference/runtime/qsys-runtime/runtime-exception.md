---
title: "RuntimeException class        | QSYS API Reference Guide"
description: "Base class for all ASNA QSys Runtime generated exceptions. "
last_modified_at: 2024-08-08T21:41:46Z
---

Base class for all ASNA QSys Runtime generated exceptions.

**Namespace:** ASNA.QSys.Runtime
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [RuntimeException](#runtimeexceptionstring)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Basic constructor.
| [RuntimeException](#runtimeexceptionstring-exception)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception)) | Constructor with inner exception.

### RuntimeException([String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Basic constructor.

```cs
RuntimeException(String)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | message | Simple message explaining the cause of the exception.

### RuntimeException([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception))

Constructor with inner exception.

```cs
RuntimeException(String, Exception)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | message | Simple message further explaining the inner exception.
| [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception) | innerException | Original exception.
