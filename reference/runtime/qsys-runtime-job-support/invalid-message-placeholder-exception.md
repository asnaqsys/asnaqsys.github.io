---
title: "InvalidMessagePlaceholderException class"
description: "The exception that is thrown when an message string is missing matching curly braces on a placeholder. "
last_modified_at: 2024-08-08T21:41:46Z
---

The exception that is thrown when an message string is missing matching curly braces on a placeholder.

**Namespace:** ASNA.QSys.Runtime.JobSupport
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception) --> [JobFrameworkException](/reference/runtime/qsys-runtime-job-support/job-framework-exception.html)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [InvalidMessagePlaceholderException](#invalidmessageplaceholderexceptionstring)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Initializes a new instance of the InvalidMessagePlaceholder exception class.

### InvalidMessagePlaceholderException([String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Initializes a new instance of the InvalidMessagePlaceholder exception class.

```cs
InvalidMessagePlaceholderException(String)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | msgID | The message id with the invalid placeholder.
