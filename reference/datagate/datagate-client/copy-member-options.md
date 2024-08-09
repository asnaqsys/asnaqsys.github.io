---
title: "CopyMemberOptions enum        | QSYS API Reference Guide"
description: "Specifies the options for copying members. "
last_modified_at: 2024-08-09T16:18:40Z
---

Specifies the options for copying members.

**Namespace:** ASNA.DataGate.Client.CopyData
**Assembly:** ASNA.QSys.DataGate.Client.dll
<br>
<br>

## Remarks
This enumeration is used to control how members are copied.
The options are:
- Add: The member is added to the destination. If the member already exists, an error occurs.
- Replace: The member is replaced in the destination. If the member does not exist, an error occurs.
- UpdateAdd: The member is updated in the destination. If the member does not exist, it is added.

<br>
<br>

## Enum Values

| Name | Description | Value
| --- | --- | --- 
| Add | The member is added to the destination. If the member already exists, an error occurs. | 0 |
| Replace | The member is replaced in the destination. If the member does not exist, an error occurs. | 1 |
| UpdateAdd | The member is updated in the destination. If the member does not exist, it is added. | 2 |
