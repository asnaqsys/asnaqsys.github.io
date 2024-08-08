---
title: "SpoolerControlCharacter enum  | QSYS API Reference Guide"
description: "Indicates the manner in which control characters will be represented in the database. "
last_modified_at: 2024-08-08T21:41:46Z
---

Indicates the manner in which control characters will be represented in the database.

**Namespace:** ASNA.QSys.Runtime.JobSupport
**Assembly:** ASNA.QSys.Runtime.dll
<br>
<br>

## Enum Values

| Name | Description | Value
| --- | --- | --- 
| FCFC | The first character is the form ANSI control character. | 1 |
| None | No control characters will be included in the database records. | 0 |
| PrintControl | The first four character of each record contain a code specifying the skip before and space before. | 2 |
