---
title: "InvalidInputAttemptException class"
description: "Invalid input attempt on format : -record format name- on file: -filename- exception. "
last_modified_at: 2024-08-09T16:18:25Z
---

Invalid input attempt on format : -record format name- on file: -filename- exception.

**Namespace:** ASNA.QSys.Runtime
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception) --> [RuntimeException](/reference/runtime/qsys-runtime/runtime-exception.html)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [InvalidInputAttemptException](#invalidinputattemptexceptionstring-string)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Constructor that takes -record format name- and -filename- attempting invalid input.

### InvalidInputAttemptException([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Constructor that takes -record format name- and -filename- attempting invalid input.

```cs
InvalidInputAttemptException(String, String)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatName | Offending record format name.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | fileName | Offending filename.
