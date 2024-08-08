---
title: "ActivationGroupProgramConstructorException class"
description: "The exception that is thrown when a program could not be constructed. "
last_modified_at: 2024-08-08T21:41:46Z
---

The exception that is thrown when a program could not be constructed.

**Namespace:** ASNA.QSys.Runtime.JobSupport
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception) --> [JobFrameworkException](/reference/runtime/qsys-runtime-job-support/job-framework-exception.html)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [ActivationGroupProgramConstructorException](#activationgroupprogramconstructorexceptionstring-string)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Initializes a new instance of the ActivationGroupProgramConstructor exception class.

### ActivationGroupProgramConstructorException([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Initializes a new instance of the ActivationGroupProgramConstructor exception class.

```cs
ActivationGroupProgramConstructorException(String, String)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | program | The class name of the program being constructed.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | cause | The reason the constructor failed.
