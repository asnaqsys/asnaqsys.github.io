---
title: "MessageLoggingLevel enum      | QSYS API Reference Guide"
description: "Defines the filter level of which messages should be logged. "
last_modified_at: 2024-08-09T17:25:29Z
---

Defines the filter level of which messages should be logged.

**Namespace:** ASNA.QSys.Runtime.JobSupport
**Assembly:** ASNA.QSys.Runtime.dll
<br>
<br>

## Enum Values

| Name | Description | Value
| --- | --- | --- 
| LevelFour | All messages are logged. | 4 |
| LevelOne | All messages sent to the job's external message queue with a severity greater than or equal to the message logging severity are logged. | 1 |
| LevelThree | "The following information is logged: Logging level 1 and 2 information. All request messages. Commands run by a CL program. | 3 |
| LevelTwo | The following information is logged: Logging level 1 information and Request messages which result in a high-level message with a severity code greater than or equal to the message logging severity.   | 2 |
| None | No messages are logged. | 0 |
