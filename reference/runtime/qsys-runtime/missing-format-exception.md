---
title: "MissingFormatException class  | QSYS API Reference Guide"
description: "The program was compiled to use format -format-, but it was not found in file -filename-. "
last_modified_at: 2024-08-09T17:25:29Z
---

The program was compiled to use format -format-, but it was not found in file -filename-.

**Namespace:** ASNA.QSys.Runtime
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception) --> [RuntimeException](/reference/runtime/qsys-runtime/runtime-exception.html)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [MissingFormatException](#missingformatexceptionstring-string)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Constructor that takes the name of the non-existing record format and the offending file that caused the exception.

### MissingFormatException([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Constructor that takes the name of the non-existing record format and the offending file that caused the exception.

```cs
MissingFormatException(String, String)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | format | Record format name.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | file | Filename.
