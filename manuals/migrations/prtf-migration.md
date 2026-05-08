---
title: "Migration of Printer Files"
description: "Master Printer-Files migration with our concise guide. Learn key strategies for a smooth transition, ensuring data integrity and system compatibility."
---

## Printer Files

Two techniques are employed by RPG report applications to describe the layout of the report; **externally-described printer files** and the use of **O-Specs** to internally describe the layout. Monarch provides two migration agents to deal with these two techniques.  Both agents target the DataGate Printer File facilities. These facilities consist of:

- Print Files
- Print File Designer
- Data-aware controls
- Render engine

The **printer O-Spec agent** takes the RPG O-Specs as input and generates a DataGate Print File.  Print File Overflow Areas are also supported. All the fields associated with an exception record are grouped together into an externally described record format. If multiple exception records exist with the same name, each one generates its own record format and the name of each is distinguished by the indicators that control it.

The **print file agent** takes DDS specifications as input and creates a DataGate Print File.  

When each record format is printed, the print position within the page always advances the height of the format; there is no mechanism available to print two record formats on the same area of the page.

While DataGate print fields can be printed (or not) based on conditional indicators, fields and labels do not have the ability to be underlined or bolded via conditional indicators, instead the underline or bold properties must be set programmatically in ECR.

## DDS Print File Keywords

The following tables specify the level of support provided by Monarch for Print file DDS keywords.

### Printer Field-Level Keywords

| **Supported** | **May be supported in future release** | **Not applicable **|**Unsupported** |
| --- | --- | --- | --- |
| ALIAS | FLTFIXDEC | BLKFOLD | CDEFNT |
| BARCODE | FLTPCN |   | CHRID |
| COLOR | INDTXT |   | CHRSIZ |
| DATE | TEXT |   | CPI |
| DATFMT |   |   | CVTDTA |
| DATSEP |   |   | DLTEDT |
| DFT |   |   | DTASTMCMD |
| EDTCDE |   |   | FNTCHRSET |
| EDTWRD |   |   | PRTQLTY |
| FONT [^1] |   |   | TRNSPY |
| FONTNAME |   |   | TXTRTT |
| HIGHLIGHT |   |   |   |
| MSGCON |   |   |   |
| PAGNBR |   |   |   |
| POSITION [^2] |   |   |   |
| REFFLD |   |   |   |
| SKIPA |   |   |   |
| SKIPB |   |   |   |
| SPACEA |   |   |   |
| SPACEB |   |   |   |
| TIME |   |   |   |
| TIMFMT |   |   |   |
| TIMSEP |   |   |   |
| UNDERLINE |   |   |   |

### Printer Record-Level Keywords

| **Supported** | **May be supported in future release** | **Not applicable** | **Unsupported** |
| --- | --- | --- | --- |
| CPI | BOX | OVERLAY | CDEFNT |
| ENDPAGE | DRAWER |   | CHRSIZ |
| FONT | DUPLEX | | DFNCHR |
| FONTNAME | INDTXT |   | DOCIDXTAG |
| HIGHLIGHT | LINE |   | DTASTMCMD |
| LPI | OUTBIN |   | ENDPAGGRP |
| PAGNBR | TEXT |   | FNTCHRSET |
| SKIPA | |   | FORCE |
| SKIPB |   |   | GDR |
| SPACEA |   |   | INVDTAMAP |
| SPACEB |   |   | INVMMAP |
| |   |   | PAGRTT |
| |   |   | PRTQLTY |
| |   |   | STRPAGGRP |
| |   |   | ZFOLD |

### Printer File-Level Keywords

| **Supported** | **May be supported in future release** | **Not applicable** |**Unsupported** |
| --- | --- | --- | --- |
| REF | INDTXT | INDARA | DFNCHR |
|   |   |   | FNTCHRSET |
|   |   |   | SKIPA |
|   |   |   | SKIPB |

----

[^1]: Font "PointSize" height value supported only.

[^2]: Position supported when position-down and position-across are expressed as constants.
