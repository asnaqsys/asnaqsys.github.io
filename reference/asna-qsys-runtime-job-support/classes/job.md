---
title: Job Class
---

Defines the core behavior of a Job that provides an environment to submit, control, and keep track of Program activation and execution.

**Namespace:** ASNA.QSys.Runtime.JobSupport <br/>
**Assembly:** ASNA.QSys.Runtime

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> Job

<br>
<br>

## Remarks

Defines the core behavior of a Job that provides an environment to submit, control, and keep track of Program activation and execution.

[//]: # ($$TODO: Complete the Remarks section.)

<br>
<br>

## Constructor

| Name |  Description 
| --- | --- 
| **Job**( [JobConfig](/reference/asna-qsys-runtime-job-support/classes/job-config.html) ) | Called from constructors in derived classes to initializes the Job class with a Job Configuration.

<br>

### Job( [JobConfig](/reference/asna-qsys-runtime-job-support/classes/job-config.html) )

Called from constructors in derived classes to initializes the Job class with a Job Configuration.

```cs
Job( ASNA.QSys.Runtime.JobSupport.JobConfig jobConfig );
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [JobConfig](/reference/asna-qsys-runtime-job-support/classes/job-config.html) | jobConfig | The configuration values for the job. 

<br>


<br>
<br>

## Properties

| Type | Name | Description | Indexer
| --- | --- | --- | --- 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | AccountingCode | Gets or sets a user defined string. | 
| [ActivationGroup](/reference/asna-qsys-runtime-job-support/classes/activation-group.html) | ActivationGroup | Gets the Job's activation group. | 
| [ActivationManager](/reference/asna-qsys-runtime-job-support/classes/activation-manager.html) | ActivationManager | Gets the Job's activation manager. | 
| [DbConnection](https://docs.microsoft.com/en-us/dotnet/api/system.data.common.dbconnection) | ADO_Connection | Gets the ADO connection used for 'embedded SQL' | 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | ADO_ConnectionString | Gets or sets the ADO Connection String. | 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | BatchHostFolder | Gets the Folder path to the directory where the Message Files are located. | 
| [Job](/reference/asna-qsys-runtime-job-support/classes/job.html) | CurrentJob | Gets the Job associated with the calling thread. | 
| [Database](/reference/asna-qsys-runtime/classes/database.html) | Database | Gets the main DataGate Database associated with the Job. | 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | DefaultOutputQueue | Gets or Sets the name of the default print Output Queue. | 
| [DocumentLibraryObject](/reference/asna-qsys-runtime-job-support/classes/document-library-object.html) | DLO | Gets the Job's document library object facility. | 
| [ExecuteState](/reference/asna-qsys-runtime-job-support/classes/execute-state.html) | ExecuteState | Always returns the State 'Running'. | 
| [IntergratedFileSystem](/reference/asna-qsys-runtime-job-support/classes/intergrated-file-system.html) | IFS | Gets the Job's integrated file system facility. | 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | JobQueueBaseQueuesPath | Gets or sets the folder path root locating the job queues directory. | 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | JobQueueEntryExtension | Gets the file extension used for job queue entries. | 
| [LocalDataCollection](/reference/asna-qsys-runtime-job-support/classes/local-data-collection.html) | LDC | Gets the Job's Local Data Collection. | 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | MessageFileFolder | Gets or sets the Folder path to the directory where the Message Files are located. | 
| [List](https://docs.microsoft.com/en-us/dotnet/api/system.collections.generic.list-1) | NamespaceList | Gets the Namespace List for dynamic program calls | 
| [Database](/reference/asna-qsys-runtime/classes/database.html) | PrinterDB | Gets the DataGate Database for Printer Files associated with the Job. | 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | PsdsJobName | Gets or sets the Job's Name portion of the full job name. | 
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | PsdsJobNumber | Gets or sets the Job's Number portion of the full job name. Job's Number is unique within a Monarch Application Server. | 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | PsdsJobUser | Gets or sets the Job's User name portion of the full job name. | 
| [Spooler](/reference/asna-qsys-runtime-job-support/classes/spooler.html) | Spooler | Gets the Job's print output spooler. | 
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | StartupMoment | Gets the timestamp of when the Job was started. Precision up to microseconds. | 
| [JobStats](/reference/asna-qsys-runtime-job-support/classes/job-stats.html) | Stats | Gets the Job' Statistics. May return NULL if job has no Job Services. | 
| [JobStatus](/reference/asna-qsys-runtime-job-support/classes/job-status.html) | Status | Gets a copy of the Job's Status. | 

<br>
<br>

## Methods

| Type | Name | Description | Return Description 
| --- | --- | --- | --- 
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [Dispose](#disposeboolean)([Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Releases the resources used by the current instance of the Job class. | 
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [EndPrograms](#endprograms)() | Deactivates all programs in the job and calls Dispose(). | 
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | [Equals](https://docs.microsoft.com/en-us/dotnet/api/system.object.equals)([Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | Determines whether the specified object is equal to the current object.<br>(Inherited from [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | true if the specified object is equal to the current object; otherwise, false.
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [Finalize](https://docs.microsoft.com/en-us/dotnet/api/system.object.finalize)() | Allows an object to try to free resources and perform other cleanup operations before it is reclaimed by garbage collection.<br>(Inherited from [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | 
| [DbConnection](https://docs.microsoft.com/en-us/dotnet/api/system.data.common.dbconnection) | [getADO_Connection](#getado_connection)() | Gets the ADO connection used for 'embedded SQL' | Always returns NULL.
| [Database](/reference/asna-qsys-runtime/classes/database.html) | [getDatabase](#getdatabase)() | When overridden in a derived class, gets the main DataGate Database associated with the Job. | Returns de Database instance for the Job.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | [GetHashCode](https://docs.microsoft.com/en-us/dotnet/api/system.object.gethashcode)() | Serves as the default hash function.<br>(Inherited from [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | A hash code for the current object.
| [MessageQueue](/reference/asna-qsys-runtime-job-support/classes/message-queue.html) | [GetInvokedMessageQueue](#getinvokedmessagequeuestring)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Gets the message queue associated with the newest invocation of a program. | If found, the message queue associated with the program; otherwise null.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [GetLdaField](#getldafieldint32-int32)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Gets a value stored in the LDA. | The requested field value.
| [Database](/reference/asna-qsys-runtime/classes/database.html) | [getPrinterDB](#getprinterdb)() | Gets the DataGate Database for Printer Files associated with the Job. | Returns the main Database.
| [Char](https://docs.microsoft.com/en-us/dotnet/api/system.char) | [GetSwitch](#getswitchint32)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Gets the value of one of the 8 job switches. | The switch value of '0' or '1' for the requested switch, otherwise '0'.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [GetSwitches](#getswitches)() | Gets a string representing the values of all 8 job's switches. | A '1' or '0' for each switch. The value of switch 1 is the leftmost position of the string, switch 8 is in the last position.
| [Type](https://docs.microsoft.com/en-us/dotnet/api/system.type) | [GetType](https://docs.microsoft.com/en-us/dotnet/api/system.object.gettype)() | Gets the Type of the current instance.<br>(Inherited from [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | The exact runtime type of the current instance.
| [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) | [MemberwiseClone](https://docs.microsoft.com/en-us/dotnet/api/system.object.memberwiseclone)() | Creates a shallow copy of the current Object.<br>(Inherited from [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | A shallow copy of the current Object.
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [ReclaimResources](#reclaimresourcesboolean)([Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Reclaim the resources on the Job's default activation group. | 
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | [ReferenceEquals](https://docs.microsoft.com/en-us/dotnet/api/system.object.referenceequals)([Object](https://docs.microsoft.com/en-us/dotnet/api/system.object), [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | Determines whether the specified Object instances are the same instance.<br>(Inherited from [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | true if objA is the same instance as objB or if both are null; otherwise, false.
| [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) | [RetrieveSystemValue](#retrievesystemvaluestring)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Gets the value of an attribute of the current environment. | The value of the attribute requested.
| [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) | [RetrieveUserProfile](#retrieveuserprofilestring-string)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Gets the name of a user. | The userProfileName value or the name of the current user.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [SerializeLdaToBase64String](#serializeldatobase64string)() | Converts the value of the LDA to a string representation that is encoded with base-64 digits. | The string representation, in base 64, of the contents of the LDA.
| [NameValueCollection](https://docs.microsoft.com/en-us/dotnet/api/system.collections.specialized.namevaluecollection) | [SetEnvironmentFromJobQueueEntry](#setenvironmentfromjobqueueentry)() | This method does not do anything useful, it simply returns an empty dictionary.  It will be removed soon. | Returns an empty dictionary.
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [SetLdaField](#setldafieldint32-int32-string)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Stores a value in the LDA. | 
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [SetSwitch](#setswitchint32-char)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Char](https://docs.microsoft.com/en-us/dotnet/api/system.char)) | Sets the value of one of the 8 job switches to '0' or '1'. | 
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [SetSwitches](#setswitchesstring)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Sets the first n job switches to the values of the characters passed in a string. | 
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [ShutDown](#shutdown)() | End the job's execution by ending all of its active programs and disposing itself. | 
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | [ToString](https://docs.microsoft.com/en-us/dotnet/api/system.object.tostring)() | Returns a string that represents the current object.<br>(Inherited from [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | A string that represents the current object.

<br>
<br>

### Dispose([Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Releases the resources used by the current instance of the Job class.

```cs
Dispose(Boolean disposing);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | disposing | true to release managed and unmanaged resources; false to release only unmanaged resources. 


<br>
<br>

### EndPrograms()

Deactivates all programs in the job and calls Dispose().

```cs
EndPrograms();
```


<br>
<br>

### getADO_Connection()

Gets the ADO connection used for 'embedded SQL'

```cs
getADO_Connection();
```

#### Returns

[DbConnection](https://docs.microsoft.com/en-us/dotnet/api/system.data.common.dbconnection)

Always returns NULL.


<br>
<br>

### getDatabase()

When overridden in a derived class, gets the main DataGate Database associated with the Job.

```cs
getDatabase();
```

#### Returns

[Database](/reference/asna-qsys-runtime/classes/database.html)

Returns de Database instance for the Job.


<br>
<br>

### GetInvokedMessageQueue([String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Gets the message queue associated with the newest invocation of a program.

```cs
GetInvokedMessageQueue(String programQueueId);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | programQueueId | A string with the format 'Relation ProgramName'. Program is a program name or '*' for the current program. Relation is optional, use '*PRV' for previous entry to Program or '*SAME' for Program. 

#### Returns

[MessageQueue](/reference/asna-qsys-runtime-job-support/classes/message-queue.html)

If found, the message queue associated with the program; otherwise null.


<br>
<br>

### GetLdaField([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

Gets a value stored in the LDA.

```cs
GetLdaField(Int32 start, Int32 length);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | start | The one-based index into the location within the LDA where the value is stored. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | length | The length in characters of the value to retrieve. 

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

The requested field value.


<br>
<br>

### getPrinterDB()

Gets the DataGate Database for Printer Files associated with the Job.

```cs
getPrinterDB();
```

#### Returns

[Database](/reference/asna-qsys-runtime/classes/database.html)

Returns the main Database.


<br>
<br>

### GetSwitch([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

Gets the value of one of the 8 job switches.

```cs
GetSwitch(Int32 iSwitch);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | iSwitch | The requested switch, should be between 1 and 8. 

#### Returns

[Char](https://docs.microsoft.com/en-us/dotnet/api/system.char)

The switch value of '0' or '1' for the requested switch, otherwise '0'.


<br>
<br>

### GetSwitches()

Gets a string representing the values of all 8 job's switches.

```cs
GetSwitches();
```

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

A '1' or '0' for each switch. The value of switch 1 is the leftmost position of the string, switch 8 is in the last position.


<br>
<br>

### ReclaimResources([Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Reclaim the resources on the Job's default activation group.

```cs
ReclaimResources(Boolean caller);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | caller | true to include the resource of the module's program making this call; otherwise, false. 


<br>
<br>

### RetrieveSystemValue([String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Gets the value of an attribute of the current environment.

```cs
RetrieveSystemValue(String sysValName);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | sysValName | A string with the name of of the attribute to return. 

#### Returns

[Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)

The value of the attribute requested.


<br>
<br>

### RetrieveUserProfile([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Gets the name of a user.

```cs
RetrieveUserProfile(String keyName, String userProfileName);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | keyName | A string with the value "RTNUSRPRF". 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | userProfileName | The name of a user or the special value "*CURRENT" to get the current user. 

#### Returns

[Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)

The userProfileName value or the name of the current user.


<br>
<br>

### SerializeLdaToBase64String()

Converts the value of the LDA to a string representation that is encoded with base-64 digits.

```cs
SerializeLdaToBase64String();
```

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

The string representation, in base 64, of the contents of the LDA.


<br>
<br>

### SetEnvironmentFromJobQueueEntry()

This method does not do anything useful, it simply returns an empty dictionary.  It will be removed soon.

```cs
SetEnvironmentFromJobQueueEntry();
```

#### Returns

[NameValueCollection](https://docs.microsoft.com/en-us/dotnet/api/system.collections.specialized.namevaluecollection)

Returns an empty dictionary.


<br>
<br>

### SetLdaField([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Stores a value in the LDA.

```cs
SetLdaField(Int32 start, Int32 length, String newValue);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | start | The one-based index into the location within the LDA where newValue will be stored. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | length | The length in characters of the value to store. 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | newValue | The string value to store in the LDA. 


<br>
<br>

### SetSwitch([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Char](https://docs.microsoft.com/en-us/dotnet/api/system.char))

Sets the value of one of the 8 job switches to '0' or '1'.

```cs
SetSwitch(Int32 iSwitch, Char value);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | iSwitch | The requested switch, should be between 1 and 8. 
| [Char](https://docs.microsoft.com/en-us/dotnet/api/system.char) | value | '1' to set switch to '1', any other value sets the switch to '0'. 


<br>
<br>

### SetSwitches([String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Sets the first n job switches to the values of the characters passed in a string.

```cs
SetSwitches(String switchesStr);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | switchesStr | A string of up to 8 '1' or '0' values. Switches are assigned left to right to switches 1 up to 8. Switches with un-passed values are not modified.  


<br>
<br>

### ShutDown()

End the job's execution by ending all of its active programs and disposing itself.

```cs
ShutDown();
```


<br>
<br>

