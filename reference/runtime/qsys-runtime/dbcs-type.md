---
title: "DbcsType enum                 | QSYS API Reference Guide"
description: "Defines values that describe the kind of DBCS character string of a DBCS field. "
last_modified_at: 2024-08-09T17:25:29Z
---

Defines values that describe the kind of DBCS character string of a DBCS field.

**Namespace:** ASNA.QSys.Runtime
**Assembly:** ASNA.QSys.Runtime.dll
<br>
<br>

## Enum Values

| Name | Description | Value
| --- | --- | --- 
| Either | Double byte (with shift-cntrl) or single byte | 4 |
| Graphic | Double byte only (no shift-cntrl) | 5 |
| None | Not a DBCS type | 0 |
| Only | Double byte only (with shift-cntrl) | 3 |
| Open | Mixed single byte/double byte (with shift-cntrl) | 2 |
| Unicode | Special version of Graphic with CCSID 13488 or 1200 | 1 |
