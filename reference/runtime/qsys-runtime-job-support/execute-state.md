---
title: "ExecuteState enum             | QSYS API Reference Guide"
description: "Indicates the execution state of a job. "
last_modified_at: 2024-08-08T21:41:46Z
---

Indicates the execution state of a job.

**Namespace:** ASNA.QSys.Runtime.JobSupport
**Assembly:** ASNA.QSys.Runtime.dll
<br>
<br>

## Enum Values

| Name | Description | Value
| --- | --- | --- 
| AbnormalTermination | The job terminated due to an unhandled exception. | 4 |
| Ended | The job has ended. | 3 |
| Ending | The job is ending. | 2 |
| ForcefullyTerminated | the job was terminated before it could attempt to shutdown on its own. | 6 |
| PrematurelyTerminated | The job was terminated before it could shutdown on its own on time. | 5 |
| Running | Job is running. | 0 |
| ShutdownRequested | The job has been requested to be shut down. | 1 |
