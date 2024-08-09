---
title: "DuplicateFieldException class | QSYS API Reference Guide"
description: "Field -field- was specified more than once in -specification- exception. "
last_modified_at: 2024-08-09T17:25:29Z
---

Field -field- was specified more than once in -specification- exception.

**Namespace:** ASNA.QSys.Runtime
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception) --> [RuntimeException](/reference/runtime/qsys-runtime/runtime-exception.html)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [DuplicateFieldException](#duplicatefieldexceptionstring-string)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Constructor that takes the name of the offending field name, which is specified more than once causing an exception.

### DuplicateFieldException([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Constructor that takes the name of the offending field name, which is specified more than once causing an exception.

```cs
DuplicateFieldException(String, String)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | field | Offending field name.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | specification | Field specification.
