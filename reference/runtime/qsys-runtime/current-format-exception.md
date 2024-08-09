---
title: "CurrentFormatException class  | QSYS API Reference Guide"
description: "-Format name- is not the current record format in the DataSet exception. "
last_modified_at: 2024-08-09T17:25:29Z
---

-Format name- is not the current record format in the DataSet exception.

**Namespace:** ASNA.QSys.Runtime
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception) --> [RuntimeException](/reference/runtime/qsys-runtime/runtime-exception.html)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [CurrentFormatException](#currentformatexceptionstring)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Constructor that takes the -format name- different than the current record format in the DataSet, causing an exception.

### CurrentFormatException([String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Constructor that takes the -format name- different than the current record format in the DataSet, causing an exception.

```cs
CurrentFormatException(String)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatName | Record format name.
