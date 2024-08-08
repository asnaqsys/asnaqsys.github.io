---
title: "JobStatus class               | QSYS API Reference Guide"
description: "Represents the status of a job. "
last_modified_at: 2024-08-08T21:41:46Z
---

Represents the status of a job.

**Namespace:** ASNA.QSys.Runtime.JobSupport
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [JobStatus()](#jobstatus) | Initializes a new instance of the JobStatus class.

### JobStatus()

Initializes a new instance of the JobStatus class.

```cs
JobStatus()
```

## Properties

| Type | Name | Description
| --- | --- | --- 
| [ExecuteState](/reference/runtime/qsys-runtime-job-support/execute-state.html) | ExecuteState | Gets or sets the ExecutionState for the job. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | Function | Gets the function, or additional information of the job's status. |
| [ExecStatus](/reference/runtime/qsys-runtime-job-support/exec-status.html) | Status | Gets the execution status of the job. |
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | StatusStamp | Gets the execution status of the job. |

## Methods

| Signature | Description |
| --- | --- |
| [Clone()](#jobstatus-clone) | Creates and returns an identical copy of the current job status.
| [GetFormattedString()](#string-getformattedstring) | Gets a string with the status of the job.
| [SetStatus](#void-setstatusexecstatus-newexecstatus-string-newfunction)([ExecStatus](/reference/runtime/qsys-runtime-job-support/exec-status.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Sets the new status of the Job.

### JobStatus Clone()

Creates and returns an identical copy of the current job status.

```cs
JobStatus Clone()
```

### string GetFormattedString()

Gets a string with the status of the job.

```cs
string GetFormattedString()
```

### void SetStatus([ExecStatus newExecStatus](/reference/runtime/qsys-runtime-job-support/exec-status.html), [string newFunction](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Sets the new status of the Job.

```cs
void SetStatus(ExecStatus newExecStatus, string newFunction)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [ExecStatus](/reference/runtime/qsys-runtime-job-support/exec-status.html) | newExecStatus | The execution status of the job.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | newFunction | The function, or additional information, of the job'status.
