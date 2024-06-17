---
title: MessageQueueNotFoundException class
description: The exception that is thrown when a program message queue is not found in the invocation stack.
---

The exception that is thrown when a program message queue is not found in the invocation stack.

**Namespace:** ASNA.QSys.Runtime.JobSupport
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception) --> [JobFrameworkException](/reference/runtime/qsys-runtime-job-support/job-framework-exception.html)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [MessageQueueNotFoundException](#messagequeuenotfoundexceptionstring)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Initializes a new instance of the MessageQueueNotFound exception class.

### MessageQueueNotFoundException([String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Initializes a new instance of the MessageQueueNotFound exception class.

```cs
MessageQueueNotFoundException(String)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | queue | The program queue specification.
