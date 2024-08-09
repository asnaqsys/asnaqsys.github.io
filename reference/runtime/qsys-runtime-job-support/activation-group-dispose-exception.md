---
title: "ActivationGroupDisposeException class"
description: "The exception that is thrown when an program has a null activation group at dispose time. "
last_modified_at: 2024-08-09T17:25:29Z
---

The exception that is thrown when an program has a null activation group at dispose time.

**Namespace:** ASNA.QSys.Runtime.JobSupport
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception) --> [JobFrameworkException](/reference/runtime/qsys-runtime-job-support/job-framework-exception.html)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [ActivationGroupDisposeException](#activationgroupdisposeexceptionstring)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Initializes a new instance of the ActivationGroupDispose exception class.

### ActivationGroupDisposeException([String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Initializes a new instance of the ActivationGroupDispose exception class.

```cs
ActivationGroupDisposeException(String)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | program | The class name of the program being disposed.
