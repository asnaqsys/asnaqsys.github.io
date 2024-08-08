---
title: "XmlInfoEventType enum         | QSYS API Reference Guide"
description: "Enumerate the possible event types for XML information. This includes different levels of errors, warnings, and information. "
last_modified_at: 2024-08-08T21:41:32Z
---

Enumerate the possible event types for XML information. This includes different levels of errors, warnings, and information.

**Namespace:** ASNA.DataGate.Client
**Assembly:** ASNA.QSys.DataGate.Client.dll
<br>
<br>

## Enum Values

| Name | Description | Value
| --- | --- | --- 
| ErrorAll | Option to include all errors. | 48 |
| ErrorL1 | Critical error. | 16 |
| ErrorL2 | Second level error. | 32 |
| ErrorsAndWarnings | Option to include errors and warnings. | 255 |
| InfoAll | Option to include all information. | 65280 |
| InfoDebug | Detailed info. | 1024 |
| InfoL1 | General info (line one) | 256 |
| InfoL2 | General info (line two) | 512 |
| NonDebugInfo | Option to include non-debug information. | 768 |
| Warning | Warning. | 64 |
