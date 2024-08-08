---
title: "Job class                     | QSYS API Reference Guide"
description: "Defines the core behavior of a Job that provides an environment to submit, control, and keep track of Program activation and execution. "
last_modified_at: 2024-08-08T21:41:46Z
---

Defines the core behavior of a Job that provides an environment to submit, control, and keep track of Program activation and execution.

**Namespace:** ASNA.QSys.Runtime.JobSupport
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [Job()](#job) | Called from constructors in derived classes to initializes the Job class with a configuration from appsettings. 
| [Job](#jobjobconfig)([JobConfig](/reference/runtime/qsys-runtime-job-support/job-config.html)) | Called from constructors in derived classes to initializes the Job class with a Job Configuration. 

### Job()

Called from constructors in derived classes to initializes the Job class with a configuration from appsettings. 

```cs
Job()
```

### Job([JobConfig](/reference/runtime/qsys-runtime-job-support/job-config.html))

Called from constructors in derived classes to initializes the Job class with a Job Configuration. 

```cs
Job(JobConfig)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [JobConfig](/reference/runtime/qsys-runtime-job-support/job-config.html) | jobConfig | The configuration values for the job.

## Properties

| Type | Name | Description
| --- | --- | --- 
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | AccountingCode | Gets or sets a user defined string. |
| [ActivationGroup](/reference/runtime/qsys-runtime-job-support/activation-group.html) | ActivationGroup | Gets the Job's activation group. |
| [ActivationManager](/reference/runtime/qsys-runtime-job-support/activation-manager.html) | ActivationManager | Gets the Job's activation manager. |
| [DbConnection](https://learn.microsoft.com/en-us/dotnet/api/system.data.common.dbconnection?view=net-8.0) | ADO_Connection | Gets the ADO connection used for 'embedded SQL' |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | ADO_ConnectionString | Gets or sets the ADO Connection String. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | BatchHostFolder | Gets the Folder path to the directory where the Message Files are located. |
| [Job](/reference/runtime/qsys-runtime-job-support/job.html) | CurrentJob | Gets the Job associated with the calling thread. |
| [Database](/reference/runtime/qsys-runtime/database.html) | Database | Gets the main DataGate Database associated with the Job. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | DefaultOutputQueue | Gets or Sets the name of the default print Output Queue. |
| [DocumentLibraryObject](/reference/runtime/qsys-runtime-job-support/document-library-object.html) | DLO | Gets the Job's document library object facility. |
| [ExecuteState](/reference/runtime/qsys-runtime-job-support/execute-state.html) | ExecuteState | Always returns the State 'Running'. |
| [IntegratedFileSystem](/reference/runtime/qsys-runtime-job-support/integrated-file-system.html) | IFS | Gets the Job's integrated file system facility. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | JobQueueBaseQueuesPath | Gets or sets the folder path root locating the job queues directory. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | JobQueueEntryExtension | Gets the file extension used for job queue entries. |
| [LocalDataCollection](/reference/runtime/qsys-runtime-job-support/local-data-collection.html) | LDC | Gets the Job's Local Data Collection. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | MessageFileFolder | Gets or sets the Folder path to the directory where the Message Files are located. |
| [List\<String\>](https://docs.microsoft.com/en-us/dotnet/api/system.collections.generic.list-1) | NamespaceList | Gets the Namespace List for dynamic program calls |
| [Database](/reference/runtime/qsys-runtime/database.html) | PrinterDB | Gets the DataGate Database for Printer Files associated with the Job. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | PsdsJobName | Gets or sets the Job's Name portion of the full job name. |
| [Decimal](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types) | PsdsJobNumber | Gets or sets the Job's Number portion of the full job name. Job's Number is unique within a Monarch Application Server. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | PsdsJobUser | Gets or sets the Job's User name portion of the full job name. |
| [Spooler](/reference/runtime/qsys-runtime-job-support/spooler.html) | Spooler | Gets the Job's print output spooler. |
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | StartupMoment | Gets the timestamp of when the Job was started. Precision up to microseconds. |
| [JobStats](/reference/runtime/qsys-runtime-job-support/job-stats.html) | Stats | Gets the Job' Statistics. May return NULL if job has no Job Services. |
| [JobStatus](/reference/runtime/qsys-runtime-job-support/job-status.html) | Status | Gets a copy of the Job's Status. |

## Methods

| Signature | Description |
| --- | --- |
| [Dispose](#void-disposebool-disposing)([Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Releases the resources used by the current instance of the Job class.
| [EndPrograms()](#void-endprograms) | Deactivates all programs in the job and calls Dispose().
| [getADO_Connection()](#dbconnection-getado-connection) | Gets the ADO connection used for 'embedded SQL'
| [getDatabase()](#database-getdatabase) | When overridden in a derived class, gets the main DataGate Database associated with the Job.
| [GetInvokedMessageQueue](#messagequeue-getinvokedmessagequeuestring-programqueueid)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Gets the message queue associated with the newest invocation of a program.
| [GetLdaField](#string-getldafieldint-start-int-length)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Gets a value stored in the LDA.
| [getPrinterDB()](#database-getprinterdb) | Gets the DataGate Database for Printer Files associated with the Job.
| [GetSwitch](#char-getswitchint-iswitch)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Gets the value of one of the 8 job switches.
| [GetSwitches()](#string-getswitches) | Gets a string representing the values of all 8 job's switches.
| [ReclaimResources](#void-reclaimresourcesbool-caller)([Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Reclaim the resources on the Job's default activation group.
| [RetrieveSystemValue](#object-retrievesystemvaluestring-sysvalname)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Gets the value of an attribute of the current environment.
| [RetrieveUserProfile](#object-retrieveuserprofilestring-keyname-string-userprofilename)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Gets the name of a user.
| [SerializeLdaToBase64String()](#string-serializeldatobase64string) | Converts the value of the LDA to a string representation that is encoded with base-64 digits.
| [SetLdaField](#void-setldafieldint-start-int-length-string-newvalue)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Stores a value in the LDA.
| [SetSwitch](#void-setswitchint-iswitch-char-value)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Char](https://docs.microsoft.com/en-us/dotnet/api/system.char)) | Sets the value of one of the 8 job switches to '0' or '1'.
| [SetSwitches](#void-setswitchesstring-switchesstr)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Sets the first n job switches to the values of the characters passed in a string.
| [ShutDown()](#void-shutdown) | End the job's execution by ending all of its active programs and disposing itself.

### void Dispose([bool disposing](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Releases the resources used by the current instance of the Job class.

```cs
void Dispose(bool disposing)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | disposing | true to release managed and unmanaged resources; false to release only unmanaged resources.

### void EndPrograms()

Deactivates all programs in the job and calls Dispose().

```cs
void EndPrograms()
```

### DbConnection getADO_Connection()

Gets the ADO connection used for 'embedded SQL'

```cs
DbConnection getADO_Connection()
```

### Database getDatabase()

When overridden in a derived class, gets the main DataGate Database associated with the Job.

```cs
Database getDatabase()
```

### MessageQueue GetInvokedMessageQueue([string programQueueId](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Gets the message queue associated with the newest invocation of a program.

```cs
MessageQueue GetInvokedMessageQueue(string programQueueId)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | programQueueId | A string with the format 'Relation ProgramName'. Program is a program name or '*' for the current program. Relation is optional, use '*PRV' for previous entry to Program or '*SAME' for Program.

#### Returns

| Type | Description
| --- | ---
| [MessageQueue](/reference/runtime/qsys-runtime-job-support/message-queue.html) | If found, the message queue associated with the program; otherwise null.

### string GetLdaField([int start](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int length](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Gets a value stored in the LDA.

```cs
string GetLdaField(int start, int length)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | start | The one-based index into the location within the LDA where the value is stored.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | length | The length in characters of the value to retrieve.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The requested field value.

### Database getPrinterDB()

Gets the DataGate Database for Printer Files associated with the Job.

```cs
Database getPrinterDB()
```

### char GetSwitch([int iSwitch](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Gets the value of one of the 8 job switches.

```cs
char GetSwitch(int iSwitch)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | iSwitch | The requested switch, should be between 1 and 8.

#### Returns

| Type | Description
| --- | ---
| [Char](https://docs.microsoft.com/en-us/dotnet/api/system.char) | The switch value of '0' or '1' for the requested switch, otherwise '0'.

### string GetSwitches()

Gets a string representing the values of all 8 job's switches.

```cs
string GetSwitches()
```

### void ReclaimResources([bool caller](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Reclaim the resources on the Job's default activation group.

```cs
void ReclaimResources(bool caller)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | caller | true to include the resource of the module's program making this call; otherwise, false.

### object RetrieveSystemValue([string sysValName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Gets the value of an attribute of the current environment.

```cs
object RetrieveSystemValue(string sysValName)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | sysValName | A string with the name of of the attribute to return.

#### Returns

| Type | Description
| --- | ---
| [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) | The value of the attribute requested.

### object RetrieveUserProfile([string keyName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string userProfileName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Gets the name of a user.

```cs
object RetrieveUserProfile(string keyName, string userProfileName)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | keyName | A string with the value "RTNUSRPRF".
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | userProfileName | The name of a user or the special value "*CURRENT" to get the current user.

#### Returns

| Type | Description
| --- | ---
| [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) | The userProfileName value or the name of the current user.

### string SerializeLdaToBase64String()

Converts the value of the LDA to a string representation that is encoded with base-64 digits.

```cs
string SerializeLdaToBase64String()
```

### void SetLdaField([int start](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int length](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [string newValue](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Stores a value in the LDA.

```cs
void SetLdaField(int start, int length, string newValue)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | start | The one-based index into the location within the LDA where newValue will be stored.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | length | The length in characters of the value to store.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | newValue | The string value to store in the LDA.

### void SetSwitch([int iSwitch](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [char value](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/char))

Sets the value of one of the 8 job switches to '0' or '1'.

```cs
void SetSwitch(int iSwitch, char value)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | iSwitch | The requested switch, should be between 1 and 8.
| [Char](https://docs.microsoft.com/en-us/dotnet/api/system.char) | value | '1' to set switch to '1', any other value sets the switch to '0'.

### void SetSwitches([string switchesStr](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Sets the first n job switches to the values of the characters passed in a string.

```cs
void SetSwitches(string switchesStr)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | switchesStr | A string of up to 8 '1' or '0' values. Switches are assigned left to right to switches 1 up to 8. Switches with unpassed values are not modified. 

### void ShutDown()

End the job's execution by ending all of its active programs and disposing itself.

```cs
void ShutDown()
```
