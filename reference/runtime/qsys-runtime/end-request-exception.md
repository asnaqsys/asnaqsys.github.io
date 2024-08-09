---
title: "EndRequestException class     | QSYS API Reference Guide"
description: "The exception that is thrown for an EndRequest operation. "
last_modified_at: 2024-08-09T16:18:25Z
---

The exception that is thrown for an EndRequest operation.

**Namespace:** ASNA.QSys.Runtime
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception) --> [RuntimeException](/reference/runtime/qsys-runtime/runtime-exception.html) --> [EndOperationException](/reference/runtime/qsys-runtime/end-operation-exception.html)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [EndRequestException](#endrequestexceptionstring-int32-exception)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception)) | Initializes a new instance of the EndRequestException class.

### EndRequestException([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception))

Initializes a new instance of the EndRequestException class.

```cs
EndRequestException(String, Int32, Exception)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | Message | A message associated with the exception.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | value | A user provided value, defaults to 0.
| [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception) | InnerException | Original exception.

## Properties

| Type | Name | Description
| --- | --- | --- 
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | Value | User provided value. |
