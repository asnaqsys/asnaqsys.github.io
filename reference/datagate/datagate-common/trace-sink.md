---
title: "TraceSink enum                | QSYS API Reference Guide"
description: "Enumerates the types of trace sinks used in the application. "
last_modified_at: 2024-08-08T21:41:32Z
---

Enumerates the types of trace sinks used in the application.

**Namespace:** ASNA.DataGate.Common
**Assembly:** ASNA.QSys.DataGate.Client.dll
<br>
<br>

## Enum Values

| Name | Description | Value
| --- | --- | --- 
| CSVNetWriter | Same as CSVTextWriter, but writes to a TcpClient stream. | 4 |
| CSVTextWriter | Writes TraceObject as comma separated values to a StreamWriter. | 0 |
| MsgTextWriter | Writes only Message string to a StreamWriter. | 1 |
| SystemDebug | Writes Message string to System.Diagnostics.Debug. | 3 |
| SystemTrace | Writes Message string to System.Diagnostics.Trace. | 2 |
