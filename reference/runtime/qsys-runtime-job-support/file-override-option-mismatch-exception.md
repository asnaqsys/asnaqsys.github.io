---
title: "FileOverrideOptionMismatchException class"
description: "The exception that is thrown when a file override has an option value that does not match expected by the named option. "
last_modified_at: 2024-08-09T16:18:25Z
---

The exception that is thrown when a file override has an option value that does not match expected by the named option.

**Namespace:** ASNA.QSys.Runtime.JobSupport
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception) --> [JobFrameworkException](/reference/runtime/qsys-runtime-job-support/job-framework-exception.html)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [FileOverrideOptionMismatchException](#fileoverrideoptionmismatchexceptionstring-string)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Initializes a new instance of the FileOverrideOptionMismatch exception class.

### FileOverrideOptionMismatchException([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Initializes a new instance of the FileOverrideOptionMismatch exception class.

```cs
FileOverrideOptionMismatchException(String, String)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | type | The expected value type.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | optionName | The option with the invalid value.
