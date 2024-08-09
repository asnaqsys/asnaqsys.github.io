---
title: "EditCodes enum                | QSYS API Reference Guide"
description: "Name of Edit-Codes which define output formatting patterns for business numeric data. "
last_modified_at: 2024-08-09T17:25:29Z
---

Name of Edit-Codes which define output formatting patterns for business numeric data.

**Namespace:** ASNA.QSys.Runtime
**Assembly:** ASNA.QSys.Runtime.dll
<br>
<br>

## Enum Values

| Name | Description | Value
| --- | --- | --- 
| A | (A)  12,345.67CR .00 | 5 |
| B | (B)  12,345.67CR     | 6 |
| C | 12345.67CR .00 | 7 |
| D | (D)   12345.67CR     | 8 |
| Four | (4)   12345.67       | 4 |
| J | (J)  12,345.67-  .00 | 9 |
| K | (K)  12,345.67-      | 10 |
| L | (L)   12345.67-  .00 | 11 |
| M | (M)   12345.67-      | 12 |
| N | (N) -12,345.67   .00 | 13 |
| None | None | 0 |
| O | (0) -12,345.67       | 14 |
| One | (1)  12,345.67   .00 | 1 |
| P | (P)  -12345.67   .00 | 15 |
| Q | (Q)  -12345.67       | 16 |
| Three | 12345.67   .00 | 3 |
| Two | (2)  12,345.67       | 2 |
| W | (W)  1234/567        | 17 |
| X | (X)  123456F         | 18 |
| Y | (Y)  1234/56/78 - defaults to YMD format (YYMD) | 19 |
| YDMY | (Y, DMY)  12/34/5678 using DMY format | 531 |
| YMDY | (Y, MDY)  12/34/5678 using MDY format | 275 |
| YYMD | (Y, YMD)  1234/56/78 using YMD format      | 19 |
| Z | (Z)   1234567        | 20 |
