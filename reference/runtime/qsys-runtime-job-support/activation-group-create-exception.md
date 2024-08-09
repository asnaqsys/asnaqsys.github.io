---
title: "ActivationGroupCreateException class"
description: "The exception that is thrown when an activation could not be found or created. "
last_modified_at: 2024-08-09T16:18:25Z
---

The exception that is thrown when an activation could not be found or created.

**Namespace:** ASNA.QSys.Runtime.JobSupport
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception) --> [JobFrameworkException](/reference/runtime/qsys-runtime-job-support/job-framework-exception.html)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [ActivationGroupCreateException](#activationgroupcreateexceptionstring-string)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Initializes a new instance of the ActivationGroupCreate exception class.

### ActivationGroupCreateException([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Initializes a new instance of the ActivationGroupCreate exception class.

```cs
ActivationGroupCreateException(String, String)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | groupName | The name of the activation group.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | program | The class name of the program being called.
