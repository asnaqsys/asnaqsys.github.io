---
title: QueryFileNotOpenException class
---

Query File -filename- is not open exception.

**Namespace:** ASNA.QSys.Runtime
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception) --> [RuntimeException](/reference/runtime/qsys-runtime/runtime-exception.html)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [QueryFileNotOpenException](#queryfilenotopenexceptionstring)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Constructor that takes the name of the quey file that not being opened, caused an exception.

### QueryFileNotOpenException([String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Constructor that takes the name of the quey file that not being opened, caused an exception.

```cs
QueryFileNotOpenException(String)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | FileName | Offending query filename.
