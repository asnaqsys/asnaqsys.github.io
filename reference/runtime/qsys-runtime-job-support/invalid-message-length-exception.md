---
title: "InvalidMessageLengthException class"
description: "The exception that is thrown when the replacement data length does not correspond to placeholder length. "
last_modified_at: 2024-08-09T17:25:29Z
---

The exception that is thrown when the replacement data length does not correspond to placeholder length.

**Namespace:** ASNA.QSys.Runtime.JobSupport
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception) --> [JobFrameworkException](/reference/runtime/qsys-runtime-job-support/job-framework-exception.html)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [InvalidMessageLengthException](#invalidmessagelengthexceptionstring)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Initializes a new instance of the InvalidMessageLength exception class.

### InvalidMessageLengthException([String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Initializes a new instance of the InvalidMessageLength exception class.

```cs
InvalidMessageLengthException(String)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | msgID | The message id with the invalid placeholder length.
