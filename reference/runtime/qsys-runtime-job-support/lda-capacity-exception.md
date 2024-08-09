---
title: "LDACapacityException class    | QSYS API Reference Guide"
description: "The exception that is thrown when a field being get or set on the LDA is beyond the LDA length. "
last_modified_at: 2024-08-09T17:25:29Z
---

The exception that is thrown when a field being get or set on the LDA is beyond the LDA length.

**Namespace:** ASNA.QSys.Runtime.JobSupport
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception) --> [JobFrameworkException](/reference/runtime/qsys-runtime-job-support/job-framework-exception.html)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [LDACapacityException](#ldacapacityexceptionint32)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Initializes a new instance of the LDACapacity exception class.

### LDACapacityException([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

Initializes a new instance of the LDACapacity exception class.

```cs
LDACapacityException(Int32)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | capacity | The maximum capacity length of the LDA.
