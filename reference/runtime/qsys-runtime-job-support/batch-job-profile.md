---
title: "BatchJobProfile class         | QSYS API Reference Guide"
description: "Provides the facilities to configure and launch a batch job. "
last_modified_at: 2024-08-09T16:18:25Z
---

Provides the facilities to configure and launch a batch job.

**Namespace:** ASNA.QSys.Runtime.JobSupport
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [BatchJobProfile](#batchjobprofilebatchoptions-string-object)([BatchOptions](/reference/runtime/qsys-runtime-job-support/batch-options.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Object\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | Initializes a new instance of the BatchJobProfile class using the batch options, program and program parameters.
| [BatchJobProfile](#batchjobprofilestring-object)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Object\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | Initializes a new instance of the BatchJobProfile class using the program and program parameters with batch default options.

### BatchJobProfile([BatchOptions](/reference/runtime/qsys-runtime-job-support/batch-options.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Object\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.object))

Initializes a new instance of the BatchJobProfile class using the batch options, program and program parameters.

```cs
BatchJobProfile(BatchOptions, String, Object[])
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [BatchOptions](/reference/runtime/qsys-runtime-job-support/batch-options.html) | options | The configuration options for the new Job.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | programName | Program to run in the new Job.
| [Object\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.object) | parmList | List of parameters to be passed to the initial program.

### BatchJobProfile([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Object\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.object))

Initializes a new instance of the BatchJobProfile class using the program and program parameters with batch default options.

```cs
BatchJobProfile(String, Object[])
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | programName | Program to run in the new Job.
| [Object\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.object) | parmList | List of parameters to be passed to the initial program.

## Properties

| Type | Name | Description
| --- | --- | --- 
| [BatchOptions](/reference/runtime/qsys-runtime-job-support/batch-options.html) | BatchOptions | Get the options for the new batch job. |

## Methods

| Signature | Description |
| --- | --- |
| [StartInProcess()](#void-startinprocess) | Starts the new job on a separate thread in the current process.
| [StartOutOfProcess()](#void-startoutofprocess) | Starts the new job on a new process.
| [Submit](#void-submitstring-jobqueuename-string-jobqueuepriority-string-scheduledatestring-string-scheduletimestring)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Enqueues the batch job.

### void StartInProcess()

Starts the new job on a separate thread in the current process.

```cs
void StartInProcess()
```

### void StartOutOfProcess()

Starts the new job on a new process.

```cs
void StartOutOfProcess()
```

### void Submit([string JobQueueName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string JobQueuePriority](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string ScheduleDateString](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string ScheduleTimeString](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Enqueues the batch job.

```cs
void Submit(string JobQueueName, string JobQueuePriority, string ScheduleDateString, string ScheduleTimeString)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | JobQueueName | The name of the queue to receive the job request.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | JobQueuePriority | The priority of the batch job in the job queue. 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | ScheduleDateString | The date when the new job becomes eligible to run. Special values include: *CURRENT, *MON->*SUN, *MONTHSTR and *MONTHEND.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | ScheduleTimeString | The time of day when the new job becomes eligible to run. Special value: *CURRENT.
