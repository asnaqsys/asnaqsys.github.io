---
title: "PrintObject Class"
description: "Helper class for managing hierarchical print structures in ASNA.QSys.EscapeFX."
---

## Definition

**Namespace:** ASNA.QSys.EscapeFX  
**Assembly:** ASNA.QSys.EscapeFX.dll

Helper class that manages hierarchical print structures for multi-level reports, including level breaks, headings, and detail printing flags.

## Constructors

| Signature | Description |
| --- | --- |
| `PrintObject(int levels)` | Initializes a new instance with the specified number of break levels. |

## Properties

| Signature | Description |
| --- | --- |
| `int Levels { get; }` | Gets the number of break levels (read-only). |
| `bool PrintHeading { get; set; }` | Gets or sets whether a heading should be printed. |
| `bool EndOfFile { get; set; }` | Gets or sets whether end-of-file has been reached. |
| `bool LoadFirstPage { get; set; }` | Gets or sets whether the first page should be loaded. |
| `PrintFlag PrintFirstPage { get; set; }` | Gets or sets the print flag for the first page. |
| `PrintFlag PrintDetail { get; set; }` | Gets or sets the print flag for detail lines. |
| `bool[] LoadLevelBreak { get; set; }` | Gets or sets the array of level break load flags. |
| `PrintFlag[] PrintLevelBreak { get; set; }` | Gets or sets the array of level break print flags. |

## Methods

| Signature | Description |
| --- | --- |
| [void CascadeLevelBreaks()](print-object-cascade-level-breaks.html) | Cascades level breaks from the highest triggered level downward. |
| [void ResetLevelBreaks()](print-object-reset-level-breaks.html) | Resets all level break flags and sets LoadFirstPage to true. |
| [void SetLevelBreaks()](print-object-set-level-breaks.html) | Sets all level break flags to true. |
| [void RequestAllHeadings()](print-object-request-all-headings.html) | Requests all headings by setting LoadFirstPage and all level break flags. |

## See Also
- [PrintFunction](print-function.html)
- [PrintFlag](print-flag.html)