---
title: RPG Cycle support

---

## Overview

The [IBM i RPG Program Cycle](https://www.ibm.com/docs/en/i/7.2?topic=logic-program-cycle) is a series of ordered steps that the main procedure goes through for each record read. Depending on the coded specifications, your program may or may not use each step in the cycle.

Primary and secondary files indicate input is controlled by the program cycle. A full procedural file indicates that input is controlled by program-specified calculation operations (for example, `READ` and `CHAIN`).

To control the cycle, you can have:

* One primary file and, optionally, one or more secondary files.
* Only full procedural files (including external Printfiles).
* A combination of one primary file, optional secondary files, and one or more full procedural files in which some of the input is controlled by the cycle, and other input is controlled by the program.
* No files (for example, input can come from a parameter list or a DataArea Data structure).

## QSys Cycle

The [RPG implicit logic](https://www.ibm.com/docs/en/i/7.2?topic=cycle-detailed-rpg-iv-program) is made explicit during the conversion to C#.

Each program that uses the `Cycle` is generated with the StartEntry method calling the generated _StartCycle method as indicated by the following pseudo-code:

```cs
void StarEntry(int cparms)
{
    _StartCycle();
    do
    {
        .
        .
        .
    } while (!(bool)_INLR);
}
```

Immediately after the `_StartCycle()` there is an explicit `do loop` that repeats until the **Last Record Indicator** (`_INLR`) is set. The program is said to have processed tha **Last Record** (on the primary file) and it should terminate.

The following [Flow Chart](https://en.wikipedia.org/wiki/Flowchart) shows the steps that are completed, the conditions that are tested and the points in which the following pre-defined methods are called:

* `_DetailCalc`
* `_DetailOutput`
* `_TotalCalc`
* `_TotalOutput`
* `_FetchOverflow`

<br>

<img src="images/qsys-cycle.svg" alt="Cycle Flow-chart" style="width:60em !important; height:115em !important">

## Detailed numbered flow-chart building blocks

1. _StartCycle is the name of the subroutine that initializes the Cycle. It assumes the primary file and all secondary files are already open, which causes the first record from the primary and all secondary files to be read, and all program fields have their correct values including first page indicator (`_IN1P` is initialized to *true* in the class constructor).

2. If _IN1P is *true* (this is the first time _StartCycle is called), go to step 3. Otherwise, go to step 4.

3. Perform header and detail output (`DetailPrintSpec` and `HeaderPrintSpec` in AVR `CycleOutput` section). Set `_IN1P` to *false*.

4. Set all record identifying and `_L1` through `_L9` indicators to *false*.

5. If `_INLR` is *true*, go to step 6, otherwise go to step 7.

6. Set the level indicators `_INL1` through `_INL9` to *true*, and go to step 18.

7. If this is not the first time thru the loop, read a record from the last file processed.

8. If `FORCE` was issued on the previous time thru the loop, go to step 9, otherwise go to step 10.

9. The forced file is selected for processing. If the forced file is at `EOF`, go to step 10. Otherwise, the match record indicator (`_INMR`) is set to *OFF and the match fields in the forced file are saved. Continue at step 13.

10. If match fields are used in the program, go to step 11. Otherwise go to step 12.

11. The match field routine selects the next file. Continue at step 13.

12. The next file is selected. It will be either the primary if is not at `EOF`, or the first secondary that is not at `EOF`, selected in the order by which they are specified in the program.

13. If all files are at `EOF`, then go to 14. Otherwise go to 15.

14. Set `_INLR` to *true* and all level indicators `_INL1` through `_INL9` as well. Continue at 18.

15. The record identifying indicator is set *true* for the record selected for processing.

16. If there is a control break, go to 17. Otherwise go to 18.

17. The appropriate control level indicator (`_INL1` through `_INL9`) is set *ON. All lower level indicators are also set *true*.

18. Determine whether totals need to be executed and if so go to 19. Otherwise go to 20. If no control levels are specified for any record, totals are bypassed on the first cycle and are always processed after the first cycle. If control levels are specified, totals are bypassed until the first record containing control fields has been processed.

19. Total Calculations (`_TotalCalc`) and total output are processed (`TotalPrintSpec` in  `CycleOutput`).

20. If `_INLR` is *true*, go to step 22.

21. The match record indicator (`_INMR`) is set *true* or *false* depending on whether the record read is a matching record. Data from the last record read is made available for processing. Detail Calculations (`_DetailCalc`) are processed. Continue at step 3.

22. Return to the caller.

## Cycle `Input` Specifications

During Migration, if there are legacy RPG [Input Specifications](https://www.ibm.com/docs/en/i/7.3?topic=specifications-input) with *Field Description* entries corresponding to [Control Level](https://www.ibm.com/docs/en/i/7.3?topic=entries-positions-63-64-control-level#ifd6364) or [Matching Fields](https://www.ibm.com/docs/en/i/7.3?topic=entries-positions-65-66-matching-fields), then for each record where these kind of fields are defined, an AVR declaration will be produced.

The syntax is as follows:

&nbsp;&nbsp;&nbsp;**DclFmtCycleAttr** *record-format*  *indicator* **Ln**(*field-name1*, *field-name2*) **Mn**(*field-name*) 

Where,

&nbsp;&nbsp;&nbsp;`Ln` can be `L1`, `L2`, `L3`, `L4`, `L5`, `L6`, `L7`, `L8` or `L9` (up to nine Level Breaks)

and,

&nbsp;&nbsp;&nbsp;`Mn` can be `M1`, `M2`, `M3`, `M4`, `M5`, `M6`, `M7`, `M8` or `M9` (up to nine Matching Fields) 

> The Indicator is optional and comes from the [Record Identification Input Spec](https://www.ibm.com/docs/en/i/7.3?topic=indicator-indicators).

For example:

```
DclFmtCycleAttr Master *In77 M1(MOrder#) L2(MOrder#)
DclFmtCycleAttr Detail *In42 M1(DOrder#)
DclFmtCycleAttr Orders *In43 M1(DOrder#) L1(DOrder#, DItem#)
```

> There can be more than one field declared as an `L` keyword. Only one field can be declared in the `M` keyword.

## Cycle `Output` Specifications

During Migration, if there are legacy RPG [Output Specifications](https://www.ibm.com/docs/en/i/7.3?topic=specifications-output) of type `'H'`, `'D'`, `'T'`, a section of the intermediate [AVR](https://asna.com/us/products/visual-rpg) will be generated with a *syntax* as follows:

**BegCycleOutput**

&nbsp;&nbsp;&nbsp;**HeaderDiskSpec**  *file*   Op(*file-operation*) Flds(*list*) 

&nbsp;&nbsp;&nbsp;**DetailDiskSpec**  *file*   Op(*file-operation*) Flds(*list*)

&nbsp;&nbsp;&nbsp;**TotalDiskSpec**   *file*   Op(*file-operation*) Flds(*list*)

&nbsp;&nbsp;&nbsp;**HeaderPrintSpec** *format* Cond(*ind-expr*) FetchOverflow(*yes/no*)

&nbsp;&nbsp;&nbsp;**DetailPrintSpec** *format* Cond(*ind-expr*) FetchOverflow(*yes/no*)

&nbsp;&nbsp;&nbsp;**TotalPrintSpec**  *format* Cond(*ind-expr*) FetchOverflow(*yes/no*)

**EndCycleOutput**

Notes:
1. Some Output Cycle records are `Disk` (*Database*) related while others are `Print` (*Printfile*) related.
2. Disk Output Specs may use up to 9 Level Breaks (L1 ... L9).
3. Disk Output Specs may use up to 9 Matching Record fields (M1 ... M9).

For example:

```cs
BegCycleOutput
    HeaderPrintSpec QPRINT_DETH1P    Cond(*InOF *Or *In1P )
    HeaderPrintSpec QPRINT_DETH1L1F  Cond(*InL1 ) FetchOverflow(*Yes)
    DetailPrintSpec QPRINT_DET01     Cond(*In01 )
    TotalPrintSpec  QPRINT_TOTAL2LRF Cond(*InLR ) FetchOverflow(*Yes)
EndCycleOutput
```

*Where*  QPRINT_DETH1P, QPRINT_DETH1L1F, QPRINT_DET01 and QPRINT_TOTAL2LRF are record formats. Note that RPG *unnamed* record formats are named by RPG Agent using the name of the file, the record type and the indicator conditions (to make a unique name used by the Printfile Agent). 

The explicit C# conversion will translate each of these records with its proper *Conditions*, Disk *Operations* and used *Fields* into the body of the methods discussed above (`_DetailCalc`, `_DetailOutput`, `_TotalCalc` etc.).

## Database File Designations
Certain Database files participate in the Cycle logic. Files with [Designation](https://www.ibm.com/docs/en/i/7.3?topic=statement-position-18-file-designation) `Primary` and `Secondary`, participate in the program `Cycle`.

In the C# conversion, the file designation is indicated by the `isPrimary` parameter in the [DatabaseCycleFile](/reference/asna-qsys-runtime/classes/database-cycle-file.html) constructor ( *true* means Primary, *false* means Secondary ).

## First Page

Before the first record is read the first time through the loop, the program resolves any parameters passed to it, writes the records conditioned by the `_IN1P` (first page) indicator, and processes any heading or detail output operations having no conditioning indicators.

For example, heading lines printed before the first record is read might consist of constant or page heading information or fields for reserved words, such as `PAGE` and `UDATE`.

The first page indicator is turned on in the class constructor and turned off after the first page headings (if any) are printed. 

## Matching Records

To process matching records in `QSys` programs, the fields defined as the matching record fields are assigned using M1...M9 on the `DclFmtCycleAttr` record for each file format on which the matching is to occur. For instance, if you have an order master file, an order detail file, and a backorder file matched by their respective order numbers you would specify the order number as the matching field in each file.

## Level Breaks

To define level breaks, the control fields are assigned using L1...L9 on the `DclFmtCycleAttr` record for each file format on which the level breaks are to occur. For instance, you have an order master file (one record per order), an order detail file (one record per item in the order), and a backorder file (multiple records per order and item). Specify the order number as the level break field in each file and include the item level on the backorder file.

## Last Record

During the last time a program goes through the loop, when no more records are available, the `_INLR` (last record) indicator and all level indicators (`_L1` through `_L9`) are set to *true*. Any total calculation and total output are completed and then control is returned to the caller.

## Overflow

The fetch overflow routine allows you to alter the overflow logic to prevent printing over the perforation and to let you use as much of the page as possible. Fetch overflow in legacy is specified with an `F` in position 16 of the output specifications on any detail, total, or exception lines for a **PRINTER** file.

Fetching for Overflow means that before printing the record format, the `Overflow` condition needs to be checked and if overflow printing would occur, the overflow indicator is set to *true*. When the indicator is set, all lines conditioned on overflow will be printed first. 

## Look-ahead Fields

Lookahead fields are not supported but code can be added to the migrated `_DetailCalc` section to add the look ahead functions.

