---
title: "BatchJob class                | QSYS API Reference Guide"
description: "Defines the core behavior of a batch job. "
last_modified_at: 2024-08-09T17:25:29Z
---

Defines the core behavior of a batch job.

**Namespace:** ASNA.QSys.Runtime.JobSupport
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [Job](/reference/runtime/qsys-runtime-job-support/job.html)
<br>
<br>

## Methods

| Signature | Description |
| --- | --- |
| [CreateJobConfig](#jobconfig-createjobconfigbatchentry-batchentry)([BatchEntry](/reference/runtime/qsys-runtime-job-support/batch-entry.html)) | Creates a JobConfig from a BatchEntry.
| [Dispose](#void-disposebool-disposing)([Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Releases the resources used by the current instance of the Job class.
| [Execute](#void-executemethodinfo-entrymethod-list-string-parmameterlist)([MethodInfo](https://learn.microsoft.com/en-us/dotnet/api/system.reflection.methodinfo?view=net-8.0), [List\<String\>](https://docs.microsoft.com/en-us/dotnet/api/system.collections.generic.list-1)) | Execute a program with a parameter list.
| [getADO_Connection()](#dbconnection-getado-connection) | Gets the ADO connection used for 'embedded SQL'
| [getDatabase()](#database-getdatabase) | Gets the main DataGate Database associated with the Job.
| [getPrinterDB()](#database-getprinterdb) | Gets the DataGate Database for Printer Files associated with the Job.
| [LogAbnormalTermination](#void-logabnormalterminationstring-error-exception-e)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception)) | Log abnormal termination.
| [openDataConnections](#void-opendataconnectionsbatchentry-batchentry)([BatchEntry](/reference/runtime/qsys-runtime-job-support/batch-entry.html)) | New and populate a JobConfig from a BatchEntry
| [Setup](#void-setupbatchentry-batchentry)([BatchEntry](/reference/runtime/qsys-runtime-job-support/batch-entry.html)) | Setup a job with the options in the BatchEntry.

### JobConfig CreateJobConfig([BatchEntry batchEntry](/reference/runtime/qsys-runtime-job-support/batch-entry.html))

Creates a JobConfig from a BatchEntry.

```cs
JobConfig CreateJobConfig(BatchEntry batchEntry)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [BatchEntry](/reference/runtime/qsys-runtime-job-support/batch-entry.html) | batchEntry | The input BatchEntry.

#### Returns

| Type | Description
| --- | ---
| [JobConfig](/reference/runtime/qsys-runtime-job-support/job-config.html) | A initialized JobConfig.

### void Dispose([bool disposing](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Releases the resources used by the current instance of the Job class.

```cs
void Dispose(bool disposing)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | disposing | true to release managed and unmanaged resources; false to release only unmanaged resources.

### void Execute([MethodInfo entryMethod](https://learn.microsoft.com/en-us/dotnet/api/system.reflection.methodinfo?view=net-8.0), [List\<string\> parmameterList](https://docs.microsoft.com/en-us/dotnet/api/system.collections.generic.list-1))

Execute a program with a parameter list.

```cs
void Execute(MethodInfo entryMethod, List<string> parmameterList)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [MethodInfo](https://learn.microsoft.com/en-us/dotnet/api/system.reflection.methodinfo?view=net-8.0) | entryMethod | The *ENTRY method info for the program to be executed.
| [List\<String\>](https://docs.microsoft.com/en-us/dotnet/api/system.collections.generic.list-1) | parmameterList | The parameter list to be passed to the program.

### DbConnection getADO_Connection()

Gets the ADO connection used for 'embedded SQL'

```cs
DbConnection getADO_Connection()
```

### Database getDatabase()

Gets the main DataGate Database associated with the Job.

```cs
Database getDatabase()
```

### Database getPrinterDB()

Gets the DataGate Database for Printer Files associated with the Job.

```cs
Database getPrinterDB()
```

### void LogAbnormalTermination([string error](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [Exception e](https://docs.microsoft.com/en-us/dotnet/api/system.exception))

Log abnormal termination.

```cs
void LogAbnormalTermination(string error, Exception e)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | error | Error message to log, may be null.
| [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception) | e | Exception to log, may be null.

### void openDataConnections([BatchEntry batchEntry](/reference/runtime/qsys-runtime-job-support/batch-entry.html))

New and populate a JobConfig from a BatchEntry

```cs
void openDataConnections(BatchEntry batchEntry)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [BatchEntry](/reference/runtime/qsys-runtime-job-support/batch-entry.html) | batchEntry | The source BatchEntry

### void Setup([BatchEntry batchEntry](/reference/runtime/qsys-runtime-job-support/batch-entry.html))

Setup a job with the options in the BatchEntry.

```cs
void Setup(BatchEntry batchEntry)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [BatchEntry](/reference/runtime/qsys-runtime-job-support/batch-entry.html) | batchEntry | The BatchEntry with the options for the job.
