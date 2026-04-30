---
title: "SubfileProgram Class"
description: "Abstract base class for subfile-based UI programs in ASNA.QSys.EscapeFX."
---

## Definition

**Namespace:** ASNA.QSys.EscapeFX  
**Assembly:** ASNA.QSys.EscapeFX.dll  
**Inherits:** [InteractiveProgram](interactive-program.html)

Abstract base class extending `InteractiveProgram` for programs that display and manage subfiles (scrollable record lists).

## Constructors

| Signature | Description |
| --- | --- |
| `SubfileProgram()` | Initializes a new instance of the SubfileProgram class. |

## Fields

| Type | Name | Description | Previous Name (PKA in Synon) |
| --- | --- | --- | --- |
| FixedDecimal<_4, _0> | FirstChangedSubfileRRN | First changed subfile RRN value. | YAFSCH |
| FixedDecimal<_4, _0> | HelpPromptEndRow | Last row that can contain promptable subfile fields. | ZHNDRW |
| FixedDecimal<_4, _0> | HelpPromptRowLen | Number of rows represented by one subfile row. | ZHRLEN |
| FixedDecimal<_4, _0> | HelpPromptStartRow | First row that can contain promptable subfile fields. | ZHSTRW |
| FixedDecimal<_5, _0> | MaxSubfileRRN | Highest subfile RRN loaded. | ##RRMX |
| FixedDecimal<_3, _0> | PageSubfileLine | Current line number within a subfile page. | ##SLIN |
| char | previousIN81DisplaySubfile | Previous state of indicator 81 display-subfile flag. |  |
| char | previousIN88ProtectMainFields | Previous state of indicator 88 protect-main-fields flag. |  |
| char | previousIN89AddMode | Previous state of indicator 89 add-mode flag. |  |
| FixedDecimal<_3, _0> | ProcessedSubfilePage | Processed subfile page count. | ##SPG |
| FixedDecimal<_4, _0> | ProcessedSubfileRRN | Last processed subfile RRN. | W0RR0 |
| FixedDecimal<_4, _0> | PromptedSubfileRRN | Subfile RRN where prompt was requested. | YPMRRN |
| FixedDecimal<_4, _0> | PromptedSubfileRow | Relative row where prompt was requested. | YZSFDL |
| FixedDecimal<_3, _0> | RecordsPerPage | Number of subfile records per page. | ##SFPG |
| FixedDecimal<_9, _0> | RecordsReadCount | Number of database records read for subfile load. | ##RRRD |
| FixedDecimal<_9, _0> | ScanLimit | Maximum number of records to scan. | W0SLM |
| FixedString<_3> | ScreenKind | Screen kind code. | W0SCR |
| FixedString<_1> | Subfile2Selector | Secondary subfile selector value. | #2SFL or Z2SFL |
| FixedDecimal<_9, _0> | SubfileLine | Calculated subfile line target. | ##SFLN |
| FixedDecimal<_3, _0> | SubfilePages | Number of subfile pages to process. | W0SPG |
| FixedDecimal<_5, _0> | SubfileRRN | Current subfile relative record number. | ##RR |
| FixedDecimal<_4, _0> | SubfileRRNSaved | Saved top subfile RRN value. | Y#SFRC |
| FixedDecimal<_4, _0> | SubfileRRNToDisplay | Subfile RRN to position at display time. | ##SFRC |
| FixedDecimal<_5, _0> | SubfileRecordsWritten | Number of subfile records written. | ##RROK |
| FixedString<_1> | SubfileSelector | Primary subfile selector value. | #1SFL or Z1SFL |


## Properties

| Signature | Description |
| --- | --- |
| `FixedString<_1> ScreenKind { get; set; }` | Gets or sets the screen kind identifier. |
| `FixedString<_1> SubfileSelector { get; set; }` | Gets or sets the subfile selector value. |
| `FixedDecimal<_5,_0> SubfileRRN { get; set; }` | Gets or sets the current subfile relative record number. |
| `FixedDecimal<_5,_0> MaxSubfileRRN { get; set; }` | Gets or sets the maximum subfile RRN loaded. |
| `FixedDecimal<_5,_0> SubfileRecordsWritten { get; set; }` | Gets or sets the count of subfile records written. |
| `FixedDecimal<_3,_0> RecordsPerPage { get; set; }` | Gets or sets the number of records per subfile page. |
| `FixedDecimal<_3,_0> SubfilePages { get; set; }` | Gets or sets the total number of subfile pages. |


## Indicator Properties

In addition to generic `inXX` properties inherited from the base classes EscapeProgram andInteractiveProgram, this SubfileProgram class provides properties with significant names to manage the program's subfile. 

| Name | Description |
| --- | --- | --- |
| `bool in80ClearSubfile { get; set; }` | Reflects the value of the clear-subfile indicator (_IN[80]) |
| `bool in81DisplaySubfile { get; set; }` | Reflects the value of the display-subfile indicator (_IN[81]) |
| `bool in82EndOfFile { get; set; }` | Reflects the value of the end-of-file indicator (_IN[82]) |
| `bool in83Invite { get; set; }` | Reflects the value of the invite indicator (_IN[83]) |
| `bool in84SubfileNextChanged { get; set; }` | Reflects the value of the subfile-next-changed indicator (_IN[84]) |
| `bool in92SubfileError { get; set; }` | Reflects the value of the subfile error indicator (_IN[82]) |

## Methods

| Signature | Description |
| --- | --- |
| [override void InitProgram()](subfile-program-init-program.html) | Initializes subfile-specific fields and page calculations. |
| [virtual void ProcessSubfile()](subfile-program-process-subfile.html) | Processes modified subfile records. |
| [void CheckDBFRecordsFound()](subfile-program-check-dbf-records-found.html) | Checks whether database records were found. |
| [void SaveHighestSFLRecord()](subfile-program-save-highest-sfl-record.html) | Saves the highest loaded subfile record number. |
| [virtual void establishSubfileLimits(bool)](subfile-program-establish-subfile-limits.html) | Establishes the subfile page and record limits. |
| [void CheckScanLimit()](subfile-program-check-scan-limit.html) | Checks and enforces the scan record limit. |
| [void RequestReloadSubfile()](subfile-program-request-reload-subfile.html) | Requests a full subfile reload. |
| [void SetCursorInSubfile(int, char)](subfile-program-set-cursor-in-subfile.html) | Positions the cursor in a subfile field. |
| [virtual void ClearSubfile()](subfile-program-clear-subfile.html) | Clears the subfile contents. |
| [virtual void SetDisplayAttributes()](subfile-program-set-display-attributes.html) | Sets display conditioning indicators. |
| [virtual void SetDisplayControlAttributes()](subfile-program-set-display-control-attributes.html) | Sets subfile control display indicators. |
| [virtual void ResetScreenFields()](subfile-program-reset-screen-fields.html) | Resets screen fields to defaults. |
| [virtual void ShowScreen()](subfile-program-show-screen.html) | Displays the subfile screen. |
| [override void ProcessPrompt()](subfile-program-process-prompt.html) | Processes prompts within subfile rows. |
| [void SetPromptRows(int, int, int)](subfile-program-set-prompt-rows.html) | Defines the promptable row range within the subfile. |

## See Also
- [InteractiveProgram](interactive-program.html)
- [DisplayTransactionFunction](display-transaction-function.html)
- [EditTransactionFunction](edit-transaction-function.html)
- [SelectRecordFunction](select-record-function.html)
- [DisplayFileFunction](display-file-function.html)
- [EditFileFunction](edit-file-function.html)