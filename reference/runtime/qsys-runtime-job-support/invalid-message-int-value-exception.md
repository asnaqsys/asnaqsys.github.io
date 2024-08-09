---
title: "InvalidMessageIntValueException class"
description: "The exception that is thrown when an exception placeholder integer is not an integer value string. "
last_modified_at: 2024-08-09T17:25:29Z
---

The exception that is thrown when an exception placeholder integer is not an integer value string.

**Namespace:** ASNA.QSys.Runtime.JobSupport
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception) --> [JobFrameworkException](/reference/runtime/qsys-runtime-job-support/job-framework-exception.html)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [InvalidMessageIntValueException](#invalidmessageintvalueexceptionstring)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Initializes a new instance of the InvalidMessageIntValue exception class.

### InvalidMessageIntValueException([String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Initializes a new instance of the InvalidMessageIntValue exception class.

```cs
InvalidMessageIntValueException(String)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | msgID | The message id with the invalid placeholder length.
