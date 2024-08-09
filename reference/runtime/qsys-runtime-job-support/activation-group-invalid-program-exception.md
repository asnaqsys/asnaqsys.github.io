---
title: "ActivationGroupInvalidProgramException class"
description: "The exception that is thrown when an activation could not be created because the program is invalid. "
last_modified_at: 2024-08-09T17:25:29Z
---

The exception that is thrown when an activation could not be created because the program is invalid.

**Namespace:** ASNA.QSys.Runtime.JobSupport
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception) --> [JobFrameworkException](/reference/runtime/qsys-runtime-job-support/job-framework-exception.html)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [ActivationGroupInvalidProgramException](#activationgroupinvalidprogramexceptionstring-string)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Initializes a new instance of the ActivationGroupInvalidProgram exception class.

### ActivationGroupInvalidProgramException([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Initializes a new instance of the ActivationGroupInvalidProgram exception class.

```cs
ActivationGroupInvalidProgramException(String, String)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | program | The class name of the program being called.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | cause | The reason the program is invalid.
