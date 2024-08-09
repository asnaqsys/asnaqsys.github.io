---
title: "RemoveBlankOption enum        | QSYS API Reference Guide"
description: "Specifies the options for removing blank spaces from a string. "
last_modified_at: 2024-08-09T16:18:40Z
---

Specifies the options for removing blank spaces from a string.

**Namespace:** ASNA.DataGate.Client.CopyData
**Assembly:** ASNA.QSys.DataGate.Client.dll
<br>
<br>

## Remarks
This enumeration is used to control how blank spaces are removed from a string.
The options are:
- None: No blank spaces are removed.
- Leading: Only the blank spaces at the start of the string are removed.
- Trailing: Only the blank spaces at the end of the string are removed.
- Both: Both the blank spaces at the start and the end of the string are removed.

<br>
<br>

## Enum Values

| Name | Description | Value
| --- | --- | --- 
| Both | Both the blank spaces at the start and the end of the string are removed. | 3 |
| Leading | Only the blank spaces at the start of the string are removed. | 1 |
| None | No blank spaces are removed. | 0 |
| Trailing | Only the blank spaces at the end of the string are removed. | 2 |
