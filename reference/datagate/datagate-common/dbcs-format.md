---
title: "DbcsFormat enum               | QSYS API Reference Guide"
description: "Specifies the format for a double-byte character set (DBCS). "
last_modified_at: 2024-08-09T16:18:40Z
---

Specifies the format for a double-byte character set (DBCS).

**Namespace:** ASNA.DataGate.Common
**Assembly:** ASNA.QSys.DataGate.Client.dll
<br>
<br>

## Enum Values

| Name | Description | Value
| --- | --- | --- 
| Either | Specifies a format that can be either double byte (with shift-control) or single byte. | 4 |
| Graphic | Specifies a double byte only format (no shift-control). | 5 |
| None | Specifies no format. | 0 |
| Only | Specifies a double byte only format (with shift-control). | 3 |
| Open | Specifies a mixed single byte/double byte format (with shift-control). | 2 |
