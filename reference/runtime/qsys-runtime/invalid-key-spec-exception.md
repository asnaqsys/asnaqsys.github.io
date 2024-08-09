---
title: "InvalidKeySpecException class | QSYS API Reference Guide"
description: "Key part -name- is invalid exception. "
last_modified_at: 2024-08-09T16:18:25Z
---

Key part -name- is invalid exception.

**Namespace:** ASNA.QSys.Runtime
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception) --> [RuntimeException](/reference/runtime/qsys-runtime/runtime-exception.html) --> [FieldNotFoundException](/reference/runtime/qsys-runtime/field-not-found-exception.html)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [InvalidKeySpecException](#invalidkeyspecexceptionstring-string-string)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Constructor that takes the name of the offending key-part on a record format of a particular filename that cause an exception.

### InvalidKeySpecException([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Constructor that takes the name of the offending key-part on a record format of a particular filename that cause an exception.

```cs
InvalidKeySpecException(String, String, String)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | keyPart | Key-part name.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | format | Record format name.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | file | Filename.
