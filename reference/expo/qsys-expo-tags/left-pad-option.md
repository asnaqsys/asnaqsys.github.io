---
title: "LeftPadOption enum            | QSYS API Reference Guide"
description: "Describes the Left padding option. "
last_modified_at: 2024-08-09T17:26:18Z
---

Describes the Left padding option.

**Namespace:** ASNA.QSys.Expo.Tags
**Assembly:** ASNA.QSys.Expo.Tags.dll
<br>
<br>

## Remarks

Left-Padding guarantees the position of the significant characters of a [Fixed Type](/concepts/program-structure/qsys-fixedtypes.html) field value, when not all the length is used. Application Logic may depend on those filled positions. 


## Enum Values

| Name | Description | Value
| --- | --- | --- 
| Blanks | Pad by adding blank characters to the left. | 1 |
| None | No Left padding. Default | 0 |
| Zeroes | Pad by adding zero character to the left. | 2 |
