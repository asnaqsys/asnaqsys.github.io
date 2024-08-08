---
title: "ActivationGroupInvalidCreatorException class"
description: "The exception that is thrown when an activation group&#39;s dynamic creator is being overwritten. "
last_modified_at: 2024-08-08T21:41:46Z
---

The exception that is thrown when an activation group's dynamic creator is being overwritten.

**Namespace:** ASNA.QSys.Runtime.JobSupport
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception) --> [JobFrameworkException](/reference/runtime/qsys-runtime-job-support/job-framework-exception.html)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [ActivationGroupInvalidCreatorException](#activationgroupinvalidcreatorexceptionstring-string)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Initializes a new instance of the ActivationGroupInvalidCreator exception class.

### ActivationGroupInvalidCreatorException([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Initializes a new instance of the ActivationGroupInvalidCreator exception class.

```cs
ActivationGroupInvalidCreatorException(String, String)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | programName | The name of the program being used as the attempted new dynamic creator.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | activationGroupName | The name of the activation group being overwritten.
