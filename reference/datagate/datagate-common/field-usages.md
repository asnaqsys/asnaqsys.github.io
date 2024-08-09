---
title: "FieldUsages enum              | QSYS API Reference Guide"
description: "Specifies the usage of a field. "
last_modified_at: 2024-08-09T17:25:07Z
---

Specifies the usage of a field.

**Namespace:** ASNA.DataGate.Common
**Assembly:** ASNA.QSys.DataGate.Client.dll
<br>
<br>

## Enum Values

| Name | Description | Value
| --- | --- | --- 
| BOTH | Specifies that the field is both an input and output field. | 6 |
| DirectionMask | Mask to get the direction only. | 6 |
| HIDDEN | Specifies that the field is neither input nor output, but both and hidden. | 7 |
| HiddenMask | Mask to get the hidden and program-to-system fields (H and P). | 33 |
| INPUT | Specifies that the field is an input field. | 2 |
| MESSAGE | Specifies a special message output-only field. | 68 |
| NEITHER | Specifies that the field is neither input nor output. | 1 |
| NoRowColumnMask | Mask to get the fields that do not have row and column information (M, P, and H). | 97 |
| NULLS | Specifies that the field may have null values. | 8 |
| OUTPUT | Specifies that the field is an output field. | 4 |
| PROGRAMTOSYSTEM | Specifies a special hidden output-only field. | 36 |
| VARLEN | Specifies that the field is a variable length vector field. | 16 |
