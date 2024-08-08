---
title: "LDALengthException class      | QSYS API Reference Guide"
description: "The exception that is thrown when a field being get or set from the LDA has a negative length. "
last_modified_at: 2024-08-08T21:41:46Z
---

The exception that is thrown when a field being get or set from the LDA has a negative length.

**Namespace:** ASNA.QSys.Runtime.JobSupport
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception) --> [JobFrameworkException](/reference/runtime/qsys-runtime-job-support/job-framework-exception.html)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [LDALengthException](#ldalengthexceptionint32)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Initializes a new instance of the LDALength exception class.

### LDALengthException([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

Initializes a new instance of the LDALength exception class.

```cs
LDALengthException(Int32)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | length | The invalid length of the LDA field.
