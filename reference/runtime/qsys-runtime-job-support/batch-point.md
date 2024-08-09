---
title: "BatchPoint class              | QSYS API Reference Guide"
description: "Defines the location and time or a batch job. "
last_modified_at: 2024-08-09T16:18:25Z
---

Defines the location and time or a batch job.

**Namespace:** ASNA.QSys.Runtime.JobSupport
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>

## Properties

| Type | Name | Description
| --- | --- | --- 
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | JobQueueName | Gets or sets the name of the job queue for a batch job. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | JobQueuePriority | Gets or sets the priority of the batch job in the job queue. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | ScheduleDateString | Gets or sets the date when the new job becomes eligible to run. Special values include: *CURRENT, *MON->*SUN, *MONTHSTR and *MONTHEND. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | ScheduleTimeString | Gets or sets the time of day when the new job becomes eligible to run. Special value: *CURRENT. |
