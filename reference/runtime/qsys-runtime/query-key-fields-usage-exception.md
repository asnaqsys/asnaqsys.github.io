---
title: "QueryKeyFieldsUsageException class"
description: "Expecting: &#39;*ASCEND&#39;, &#39;*DESCEND&#39; or &#39;*ABSVAL&#39; but found -usage- exception. "
last_modified_at: 2024-08-09T17:25:29Z
---

Expecting: '*ASCEND', '*DESCEND' or '*ABSVAL' but found -usage- exception.

**Namespace:** ASNA.QSys.Runtime
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception) --> [RuntimeException](/reference/runtime/qsys-runtime/runtime-exception.html)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [QueryKeyFieldsUsageException](#querykeyfieldsusageexceptionstring)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Constructor that takes the invalid usage string. It sets a hard-coded exception message related to the invalid usage.

### QueryKeyFieldsUsageException([String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Constructor that takes the invalid usage string. It sets a hard-coded exception message related to the invalid usage.

```cs
QueryKeyFieldsUsageException(String)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | usage | Offending usage.
