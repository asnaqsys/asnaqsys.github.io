---
title: "FieldNotFoundException class  | QSYS API Reference Guide"
description: "-Field name- was not found in format -record format name- of -filename-. "
last_modified_at: 2024-08-08T21:41:46Z
---

-Field name- was not found in format -record format name- of -filename-.

**Namespace:** ASNA.QSys.Runtime
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception) --> [RuntimeException](/reference/runtime/qsys-runtime/runtime-exception.html)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [FieldNotFoundException](#fieldnotfoundexceptionstring-string-string)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Constructor that takes the non-existing field name on a particular record format of a file that cause the exception.

### FieldNotFoundException([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Constructor that takes the non-existing field name on a particular record format of a file that cause the exception.

```cs
FieldNotFoundException(String, String, String)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | field | Field name.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | format | Format name.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | file | Filename.
