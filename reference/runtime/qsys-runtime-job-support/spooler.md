---
title: "Spooler class                 | QSYS API Reference Guide"
description: "Provides the infrastructure to manage spooled output from print files.  "
last_modified_at: 2024-08-09T17:25:29Z
---

Provides the infrastructure to manage spooled output from print files. 

**Namespace:** ASNA.QSys.Runtime.JobSupport
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>

## Methods

| Signature | Description |
| --- | --- |
| [ClearQueue](#void-clearqueuestring-queuename)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Remove all the spool files from an output queue.
| [CopyFileToDatabaseFile](#void-copyfiletodatabasefilestring-spoolfilename-string-todatabasefile-string-job-string-spoolnumber-string-createddate-string-tomember-bool-replacerecords-spoolercontrolcharacter-controlcharacter)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [SpoolerControlCharacter](/reference/runtime/qsys-runtime-job-support/spooler-control-character.html)) | Copies a Spooled File to a Database File.
| [CopyFileToTextWriter](#void-copyfiletotextwriterstring-spoolfilename-textwriter-totextwriter-string-job-string-spoolnumber-string-createddate-spoolercontrolcharacter-controlcharacter)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [TextWriter](https://learn.microsoft.com/en-us/dotnet/api/system.io.textwriter?view=net-8.0), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [SpoolerControlCharacter](/reference/runtime/qsys-runtime-job-support/spooler-control-character.html)) | Copies a Spooled File to a TextWriter.
| [CreateQueue](#void-createqueuestring-queuename)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Create a new output queue.
| [DeleteFile](#void-deletefilestring-spoolfilename-string-jobid-string-spoolnumber)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Delete a spool file.
| [DeleteQueue](#void-deletequeuestring-queuename)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Delete an output queue.
| [ExistsQueue](#bool-existsqueuestring-queuename)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Check for the existence of an output queue.
| [GetNewFilePath](#string-getnewfilepathstring-printerfile)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Gets the file path for a new spool file to be produced by the printer file name.
| [HoldFile](#void-holdfilestring-spoolfilename-string-jobid-string-spoolnumber)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Mark a spool file to be held.
| [HoldQueue](#void-holdqueuestring-queuename)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Hold an output queue. No spool file will be printed.
| [MoveFile](#void-movefilestring-spoolfilename-string-jobid-string-spoolnumber-string-newqueuename)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Move a spool file to a new output queue.
| [PrintQueue](#void-printqueuestring-queuename)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Produce a new spool file with the information about the spool files in an output queue.
| [ReleaseFile](#void-releasefilestring-spoolfilename-string-jobid-string-spoolnumber)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Mark a spool file as Released so that it can be sent to a printer.
| [ReleaseQueue](#void-releasequeuestring-queuename)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Release an output queue so that printing can continue.
| [RenameQueue](#void-renamequeuestring-queuename-string-newname)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Rename an output queue.
| [SaveFile](#void-savefilestring-spoolfilename-string-jobid-string-spoolnumber)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Mark a spool file as saved. 
| [SetFileFormType](#void-setfileformtypestring-spoolfilename-string-jobid-string-spoolnumber-string-newformtype)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Set a spool file's form type.
| [SetFileSaveAfter](#void-setfilesaveafterstring-spoolfilename-string-jobid-string-spoolnumber-bool-newvalue)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Mark a spooled file to be saved, or not, after being printed.
| [SetFileUserData](#void-setfileuserdatastring-spoolfilename-string-jobid-string-spoolnumber-string-newuserdata)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Set the value of the user data for a spool file.

### void ClearQueue([string queueName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Remove all the spool files from an output queue.

```cs
void ClearQueue(string queueName)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | queueName | The name of the output queue to be cleared.

### void CopyFileToDatabaseFile([string spoolFileName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string toDatabaseFile](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string job](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string spoolNumber](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string createdDate](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string toMember](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [bool replaceRecords](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [SpoolerControlCharacter controlCharacter](/reference/runtime/qsys-runtime-job-support/spooler-control-character.html))

Copies a Spooled File to a Database File.

```cs
void CopyFileToDatabaseFile(string spoolFileName, string toDatabaseFile, string job, string spoolNumber, string createdDate, string toMember, bool replaceRecords, SpoolerControlCharacter controlCharacter)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | spoolFileName | Name of the Spooled File.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | toDatabaseFile | Possibly qualified database file name [Library/]File.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | job | Job ID. Use "*" for current Job otherwise "JobNumber/JobUser/JobName".
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | spoolNumber | Use "*LAST" otherwise an integer number.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | createdDate | Only valid value is "*ONLY".
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | toMember | Name of database file Member, you can also use "*FIRST".
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | replaceRecords | Delete any records in the database file member prior to copying.
| [SpoolerControlCharacter](/reference/runtime/qsys-runtime-job-support/spooler-control-character.html) | controlCharacter | Manner in which control characters will be represented in the database.

### void CopyFileToTextWriter([string spoolFileName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [TextWriter toTextWriter](https://learn.microsoft.com/en-us/dotnet/api/system.io.textwriter?view=net-8.0), [string job](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string spoolNumber](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string createdDate](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [SpoolerControlCharacter controlCharacter](/reference/runtime/qsys-runtime-job-support/spooler-control-character.html))

Copies a Spooled File to a TextWriter.


#### Remarks
This base implentation throws a NotImplementedException exception.

```cs
void CopyFileToTextWriter(string spoolFileName, TextWriter toTextWriter, string job, string spoolNumber, string createdDate, SpoolerControlCharacter controlCharacter)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | spoolFileName | Name of the Spooled File.
| [TextWriter](https://learn.microsoft.com/en-us/dotnet/api/system.io.textwriter?view=net-8.0) | toTextWriter | TextWriter to 'receive' the spoolfile text.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | job | Job ID. Use "*" for current Job otherwise "JobNumber/JobUser/JobName".
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | spoolNumber | Use "*LAST" otherwise an integer number.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | createdDate | Only valid value is "*ONLY".
| [SpoolerControlCharacter](/reference/runtime/qsys-runtime-job-support/spooler-control-character.html) | controlCharacter | Manner in which control characters will be represented in the database. Defaults to None.

### void CreateQueue([string queueName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Create a new output queue.

```cs
void CreateQueue(string queueName)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | queueName | The name of the output queue to be created.

### void DeleteFile([string spoolFileName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string jobId](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string spoolNumber](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Delete a spool file.

```cs
void DeleteFile(string spoolFileName, string jobId, string spoolNumber)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | spoolFileName | Spool file name.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | jobId | The job identifier that created the spool file.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | spoolNumber | The spool file number.

### void DeleteQueue([string queueName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Delete an output queue.

```cs
void DeleteQueue(string queueName)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | queueName | The name of the output queue to be deleted.

### bool ExistsQueue([string queueName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Check for the existence of an output queue.

```cs
bool ExistsQueue(string queueName)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | queueName | The name of the output queue to be checked.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | true if the output queue exists; otherwise false.

### string GetNewFilePath([string printerFile](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Gets the file path for a new spool file to be produced by the printer file name.

```cs
string GetNewFilePath(string printerFile)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | printerFile | The name of the printer file that will produce the spool file.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The file path of the spool file for the given 

### void HoldFile([string spoolFileName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string jobId](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string spoolNumber](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Mark a spool file to be held.

```cs
void HoldFile(string spoolFileName, string jobId, string spoolNumber)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | spoolFileName | Spool file name.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | jobId | The job identifier that created the spool file.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | spoolNumber | The spool file number.

### void HoldQueue([string queueName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Hold an output queue. No spool file will be printed.

```cs
void HoldQueue(string queueName)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | queueName | The name of the output queue to be held.

### void MoveFile([string spoolFileName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string jobId](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string spoolNumber](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string newQueueName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Move a spool file to a new output queue.

```cs
void MoveFile(string spoolFileName, string jobId, string spoolNumber, string newQueueName)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | spoolFileName | Spool file name.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | jobId | The job identifier that created the spool file.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | spoolNumber | The spool file number.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | newQueueName | The name of the output queue to have the spool file.

### void PrintQueue([string queueName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Produce a new spool file with the information about the spool files in an output queue.

```cs
void PrintQueue(string queueName)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | queueName | The name of the output queue to be printed.

### void ReleaseFile([string spoolFileName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string jobId](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string spoolNumber](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Mark a spool file as Released so that it can be sent to a printer.

```cs
void ReleaseFile(string spoolFileName, string jobId, string spoolNumber)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | spoolFileName | Spool file name.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | jobId | The job identifier that created the spool file.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | spoolNumber | The spool file number.

### void ReleaseQueue([string queueName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Release an output queue so that printing can continue.

```cs
void ReleaseQueue(string queueName)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | queueName | The name of the output queue to be released.

### void RenameQueue([string queueName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string newName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Rename an output queue.

```cs
void RenameQueue(string queueName, string newName)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | queueName | The name of the output queue to be renamed.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | newName | The new name of the output queue.

### void SaveFile([string spoolFileName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string jobId](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string spoolNumber](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Mark a spool file as saved. 

```cs
void SaveFile(string spoolFileName, string jobId, string spoolNumber)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | spoolFileName | Spool file name.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | jobId | The job identifier that created the spool file.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | spoolNumber | The spool file number.

### void SetFileFormType([string spoolFileName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string jobId](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string spoolNumber](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string newFormType](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Set a spool file's form type.

```cs
void SetFileFormType(string spoolFileName, string jobId, string spoolNumber, string newFormType)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | spoolFileName | Spool file name.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | jobId | The job identifier that created the spool file.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | spoolNumber | The spool file number.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | newFormType | The new form type for the spool file.

### void SetFileSaveAfter([string spoolFileName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string jobId](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string spoolNumber](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [bool newValue](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Mark a spooled file to be saved, or not, after being printed.

```cs
void SetFileSaveAfter(string spoolFileName, string jobId, string spoolNumber, bool newValue)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | spoolFileName | Spool file name.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | jobId | The job identifier that created the spool file.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | spoolNumber | The spool file number.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | newValue | true to save the file after being printed; otherwise false.

### void SetFileUserData([string spoolFileName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string jobId](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string spoolNumber](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string newUserData](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Set the value of the user data for a spool file.

```cs
void SetFileUserData(string spoolFileName, string jobId, string spoolNumber, string newUserData)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | spoolFileName | Spool file name.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | jobId | The job identifier that created the spool file.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | spoolNumber | The spool file number.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | newUserData | The new value of the user data.
