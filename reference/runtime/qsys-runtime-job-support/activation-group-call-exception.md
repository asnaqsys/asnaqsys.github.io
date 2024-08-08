---
title: "ActivationGroupCallException class"
description: "The exception that is thrown when an program is to be activated in the caller&#39;s activation but the caller activation group could not be found. "
last_modified_at: 2024-08-08T21:41:46Z
---

The exception that is thrown when an program is to be activated in the caller's activation but the caller activation group could not be found.

**Namespace:** ASNA.QSys.Runtime.JobSupport
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception) --> [JobFrameworkException](/reference/runtime/qsys-runtime-job-support/job-framework-exception.html)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [ActivationGroupCallException](#activationgroupcallexceptionstring-string)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Initializes a new instance of the ActivationGroupCall exception class.

### ActivationGroupCallException([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Initializes a new instance of the ActivationGroupCall exception class.

```cs
ActivationGroupCallException(String, String)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | program | The class name of the program being called.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | caller | The class name of the caller.
