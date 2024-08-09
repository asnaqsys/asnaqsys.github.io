---
title: "BatchEntry class              | QSYS API Reference Guide"
description: "Represents a single entry in a batch processing system. This class provides the necessary properties and methods to manage the entry&#39;s data and st"
last_modified_at: 2024-08-09T17:25:29Z
---

Represents a single entry in a batch processing system. This class provides
the necessary properties and methods to manage the entry's data and state.

**Namespace:** ASNA.QSys.Runtime.JobSupport
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [BatchOptions](/reference/runtime/qsys-runtime-job-support/batch-options.html)
<br>
<br>

## Properties

| Type | Name | Description
| --- | --- | --- 
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | AssemblyLocation | Gets or sets the location of the assembly associated with the batch entry. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | BatchHostFolder | Gets or sets the folder path for the batch host. |
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | CreationTimestamp | Gets or sets the timestamp when the batch entry was created. |
| [DatabaseProfile](/reference/runtime/qsys-runtime-job-support/database-profile.html) | DBProfile | Gets or sets the database profile for the batch entry. |
| [DatabaseProfile](/reference/runtime/qsys-runtime-job-support/database-profile.html) | DBProfilePrint | Gets or sets the print database profile for the batch entry. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | DLORoot | Gets or sets the root for the Distributed Language Object (DLO). |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | IFSRootPath | Gets or sets the root path for the Integrated File System (IFS). |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | MonarchMessageFileFolder | Gets or sets the folder path for Monarch message files. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | OutputQueueRootPath | Gets or sets the root path for the output queue. |
| [List\<String\>](https://docs.microsoft.com/en-us/dotnet/api/system.collections.generic.list-1) | ParmList | Gets or sets the list of parameters for the batch entry. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | ProgramName | Gets or sets the name of the program associated with the batch entry. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | ScheduleDateString | Gets or sets the scheduled date for the batch entry as a string. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | ScheduleTimeString | Gets or sets the scheduled time for the batch entry as a string. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | Version | Gets or sets the version of the batch entry. |
