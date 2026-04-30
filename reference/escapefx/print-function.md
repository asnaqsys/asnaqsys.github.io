---
title: "PrintFunction Class"
description: "Abstract base class for programs that generate printed reports in ASNA.QSys.EscapeFX."
---

## Definition

**Namespace:** ASNA.QSys.EscapeFX  
**Assembly:** ASNA.QSys.EscapeFX.dll  
**Inherits:** [EscapeProgram](escape-program.html)

Abstract base class for programs that generate printed reports, managing print files, page formatting, and report generation.

## Constructors

| Signature | Description |
| --- | --- |
| `PrintFunction()` | Initializes a new instance of the PrintFunction class. |


## Indicator Properties

In addition to generic `inXX` properties inherited from the base class EscapeProgram, the PrintFunction class provides indicator 97 with a significant name indicating a page overflow.


| Type | Name | Description |
| --- | --- | --- |
| bool | in97PageOverflow | Gets or sets the value of _IN[97] which reflects the fact that the printer is in the page overflow area. |

## Properties

| Signature | Description |
| --- | --- |
| `abstract PrintFileBase MainPrintFile { get; }` | Gets the main print file for the program. |
| `abstract short MainPrintFileLineHeight { get; }` | Gets the line height (in LOMETRIC units) for the print file. |
| `FixedString<_1> PrintNewPage { get; set; }` | Gets or sets the new-page request flag. |
| `FixedString<_10> PrintFormat { get; set; }` | Gets or sets the current print format name. |
| `FixedString<_40> CompanyName { get; set; }` | Gets or sets the company name for report headers. |
| `FixedDecimal<_4,_0> WorkPageLength { get; set; }` | Gets or sets the working page length. |
| `FixedDecimal<_4,_0> WorkPageOverflow { get; set; }` | Gets or sets the working page overflow threshold. |
| `short CurrentLineNumber { get; }` | Gets the current line number on the page. |
| `short FooterSize { get; }` | Gets the remaining lines in the footer area. |
| `short OverflowSize { get; }` | Gets the overflow size from the print file. |
| `short PageLength { get; }` | Gets the printable page length in lines. |
| `int PageCount { get; }` | Gets the current page count. |
| `string PrintFormatPrefix { get; }` | Gets the format prefix derived from the print file tables. |
| `bool in97PageOverflow { get; set; }` | Gets or sets the page overflow indicator. |

## Methods

| Signature | Description |
| --- | --- |
| [abstract void PrintEndReport()](print-function-print-end-report.html) | Prints the end-of-report format. Must be overridden. |
| [abstract void Prt_A_Main()](print-function-prt-a-main.html) | Main print program body. Must be overridden. |
| [abstract void PrintFormats()](print-function-print-formats.html) | Prints all report formats. Must be overridden. |
| [abstract void EvalPrintLength()](print-function-eval-print-length.html) | Evaluates and adjusts the print page length. Must be overridden. |
| [virtual void SelectPrintFormat()](print-function-select-print-format.html) | Selects the print format for the current record. |
| [virtual void PrintPageHeader()](print-function-print-page-header.html) | Prints the page header and clears the overflow indicator. |
| [virtual void PrintFile()](print-function-print-file.html) | Main report generation loop. |
| [override void InitProgram()](print-function-init-program.html) | Initializes print-specific fields and page dimensions. |
| [bool ShouldPrint(PrintFlag)](print-function-should-print.html) | Determines whether content should be printed based on the flag. |

## See Also
- [EscapeProgram](escape-program.html)
- [PrintObject](print-object.html)
- [PrintFlag](print-flag.html)