---
title: "CopyDataOptions enum          | QSYS API Reference Guide"
description: "Specifies the options for copying data. "
last_modified_at: 2024-08-09T16:18:40Z
---

Specifies the options for copying data.

**Namespace:** ASNA.DataGate.Common
**Assembly:** ASNA.QSys.DataGate.Client.dll
<br>
<br>

## Enum Values

| Name | Description | Value
| --- | --- | --- 
| ByRRN | Specifies that the data should be copied by RRN. | 2 |
| Compress | Specifies that the data should be compressed. | 4 |
| CreateFile | Specifies that a new file should be created. | 1 |
| KeepReferenceInfo | Specifies that reference information should be kept. | 1024 |
| MapFields | Specifies that fields should be mapped by name (disregard order & type, truncate fields). | 256 |
| MapFieldsByIndex | Specifies that fields should be mapped by index (disregard type, truncate fields). | 32 |
| MapFieldsWithDrop | Specifies that fields should be mapped and missing fields should be dropped (always implies MapFields) | 128 |
| MapNoCheck | Specifies that the data should be copied byte-to-byte without checking (record truncation). | 512 |
| Reserved1 | Reserved for future use (AllFormats). | 8 |
