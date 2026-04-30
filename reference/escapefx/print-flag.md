---
title: "PrintFlag Enumeration"
description: "Defines print condition flags used in PrintFunction."
---

## Definition

**Namespace:** ASNA.QSys.EscapeFX  
**Assembly:** ASNA.QSys.EscapeFX.dll

Defines the print condition flags used to control when content is printed in a report.

## Members

| Name | Value | Description |
| --- | --- | --- |
| `None` | 0 | No printing. Corresponds to blank value. |
| `Ready` | 1 | Content is ready to print immediately. Corresponds to `'Y'`. |
| `OnFirstPage` | 2 | Print only on the first page when a new page is requested. Corresponds to `'P'`. |

## Remarks

`PrintFlag` is used by `PrintFunction.ShouldPrint` to determine whether a section of the report should be output at the current point in the report generation cycle.

## See Also
- [PrintFunction](print-function.html)
- [PrintFunction.ShouldPrint](print-function-should-print.html)
- [PrintObject](print-object.html)