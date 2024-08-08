---
title: "TraceConfig enum              | QSYS API Reference Guide"
description: "Enumerates the types of trace configurations used in the application. "
last_modified_at: 2024-08-08T21:41:32Z
---

Enumerates the types of trace configurations used in the application.

**Namespace:** ASNA.DataGate.Common
**Assembly:** ASNA.QSys.DataGate.Client.dll
<br>
<br>

## Enum Values

| Name | Description | Value
| --- | --- | --- 
| ThreadInfo | If level is 1 or greater, the CSV data contains thread information. | 0 |
| ThreadPriority | Sets the logger thread priority. 1 or 0 means lowest priority.2 means below normal priority.3 means normal priority.4 or greater means no logger thread - Trace output is written in the caller's thread and flushed after every call. | 1 |
