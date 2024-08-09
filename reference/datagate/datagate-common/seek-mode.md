---
title: "SeekMode enum                 | QSYS API Reference Guide"
description: "Specifies the mode for seeking data in a data structure. "
last_modified_at: 2024-08-09T17:25:07Z
---

Specifies the mode for seeking data in a data structure.

**Namespace:** ASNA.DataGate.Common
**Assembly:** ASNA.QSys.DataGate.Client.dll
<br>
<br>

## Enum Values

| Name | Description | Value
| --- | --- | --- 
| Equal | Specifies that the seeking starts from the record that equals a specific key. | 13 |
| First | Specifies that the seeking starts from the first record. | 5 |
| Greater | Specifies that the seeking starts from the record that is greater than a specific key. | 14 |
| Last | Specifies that the seeking ends at the last record. | 6 |
| SetGE | Specifies that the seeking starts from the record that is greater than or equal to a specific key. | 15 |
| SetGT | Specifies that the seeking starts from the record that is strictly greater than a specific key. | 46 |
| SetLL | Specifies that the seeking starts from a lower limit for a range of records. | 47 |
