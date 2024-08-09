---
title: "OutOfProcessBatchJob class    | QSYS API Reference Guide"
description: "Defines the core behavior of an out of process batch job. "
last_modified_at: 2024-08-09T16:18:25Z
---

Defines the core behavior of an out of process batch job.

**Namespace:** ASNA.QSys.Runtime.JobSupport
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [Job](/reference/runtime/qsys-runtime-job-support/job.html) --> [BatchJob](/reference/runtime/qsys-runtime-job-support/batch-job.html)
<br>
<br>

## Methods

| Signature | Description |
| --- | --- |
| [Run](#void-runstring--args)([String\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Instantiates the job and runs the initial program.

### void Run([String\[\] args](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Instantiates the job and runs the initial program.

```cs
void Run(String[] args)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.string) | args | Initial program parameters.
