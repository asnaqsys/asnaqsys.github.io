---
title: "TraceID enum                  | QSYS API Reference Guide"
description: "Enumerates the types of trace identifiers used in the application. "
last_modified_at: 2024-08-09T16:18:40Z
---

Enumerates the types of trace identifiers used in the application.

**Namespace:** ASNA.DataGate.Common
**Assembly:** ASNA.QSys.DataGate.Client.dll
<br>
<br>

## Enum Values

| Name | Description | Value
| --- | --- | --- 
| DLHeader | Represents a DataLink header (level 3 or less) or full packet (level 4 or greater), with MSGID.This is only enabled in DEBUG builds. | 0 |
| LineTrace | Represents the current location (class.method, file, line).Source info (file & line) only at level 3 or greater.Passed parameters, if any, are ToString()'ed at level 4 or greater. | 1 |
| RecordDump | Represents a byte dump of a single database record. | 3 |
| TimeTrace | Represents a message with optional (level 4) timestamp. | 2 |
