---
title: "JobConfig class               | QSYS API Reference Guide"
description: "Holds configuration values for the creation of new jobs. "
last_modified_at: 2024-08-09T16:18:25Z
---

Holds configuration values for the creation of new jobs.

**Namespace:** ASNA.QSys.Runtime.JobSupport
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>

## Properties

| Type | Name | Description
| --- | --- | --- 
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | BatchHostPath | Gets or Sets the directory path where the Batch Host executable is located in the system. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | DefaultOutputQueue | Gets or Sets the name of the default Output Queue. Defaults to "QPRINT" |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | DlsRootName | Gets or Sets the name of the directory, located within the IFSRootPath, where the Document Library Objects are located. Defaults to "QDLS" |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | IFSRootPath | Gets or Sets the directory path where the IFS objects are located in the system. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | JobQueueBaseQueuesPath | Gets or Sets the directory path where the Job Queues are located in the system. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | MessageFilePath | Gets or Sets the directory path where the Message Files are located in the system. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | OutputQueueRootPath | Gets or Sets the directory path where the Output Queues are located in the system. |
