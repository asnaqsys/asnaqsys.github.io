---
title: "Migration of RPG Programs"
description: "Master RPG migration with our guide. Learn effective strategies, tips, and best practices for a smooth transition to modern platforms."
---

## RPG Programs

### Op-Codes

As of version 11.4, all RPG op codes are supported with the exception of those shown in the table below.

| **Unsupported** | **Unsupported** |
| --- | --- |
| ACQ | NEXT |
| ALLOC | POST |
| DEALLOC | REALLOC |
| DEBUG | REL |
| DSPLY | RESET |
| DUMP | SHTDN |

### Features

#### Overlapping Fields

The overlapping data structure field of RPG is used to remap areas of memory that allow the program to give multiple meanings to the same bytes.  .NET strictly enforces type safety and abhors this kind of arbitrary reinterpretation of memory.  Remapping is sometimes used in a very conflicting manner but there are certain common usages that are convenient and valid.

We have identified several common idioms involving overlapping data fields, for instance giving individual field names to elements of an array, and masquerading a data structure as a large character field - typically stored as an unformatted record or as a data area. 

There is another common usage of remapping, extensively used across the RPG community, which requires special handling.  It involves partitioning a text field into subfields.  The most prevalent and probably perverse use of this style involves dealing with dates.  The Date (and Time) type did not appear in RPG until the mid nineties with the advent of RPG ILE.  Prior to that, RPG programmers were forced to use a Character (or Decimal) type to hold a date field, and then subdivide the field into the year, month, and day subfields.  Another case of subfields deals with encoded data, for example composing an account number based on the division, department, and project of the account.  Monarch makes use of the ECR **Overlay** and **StartAt** keywords of **DclDsFld** to implement overlapping fields.

#### Character vs. Byte

In ECR, character fields are kept in Unicode (as is standard in .NET languages), so a single character occupies two bytes.

In RPG, a single character occupies a single byte, and some programs take advantage of this fact to the point that some of their algorithms blur the difference between a byte and a char; these algorithms many times also depend on the EBCDIC encoding of character fields and assume to know the bit patterns used in their representation.

Programs that have these dependencies need to be revised once converted to ECR so that their EBCDIC and single byte dependencies are eliminated.

#### Hexadecimal Constants

Constants of the form X'xxxx' are invalid, however, the H'xxxx' are valid.

#### Cycle

Monarch supports the RPG Cycle. The features include: Primary and secondary files, control level breaks and matching records. However, halt indicators are not supported.

#### Internally Described Files

Monarch provides support for internally described print files (please see print files below), however there is no support for internally described workstation and disk files.

#### ILE RPG

Monarch supports single and multi-module ILE RPG programs and Service programs. Procedures are also supported.

#### Menus

Monarch supports only UIM menus as entry points for GamePlans.

### Program Status DS and File Information DS

A program-status data structure (PSDS) provides program exception (error) information to the program.  The PSDS is defined in the main source section; therefore, there is only one PSDS per module.

The location of the subfields in the PSDS is defined by special keywords or by predefined 'From' and 'To' positions.  In order to access the subfields, you assign a name to each subfield. The following fields are supported on the Program Status DS:

| **Offset/Keyword** | **Description** |
| --- | --- |
|   1 | Program |
| 191 | Job Start Date |
| 244 | Job |
| 254 | User |
| 264 | Job Number |
| 270 | Job Start Time |
| 276 | Program Start Date |
| 282 | Program Start Time |
| 358 | Current User |
| \*PROC | Program |
| \*PROGRAM | Program |

The following fields are supported on the File Information DS (INFDS):

| **Offset/Keyword** | **Description** |
| --- | --- |
| 1 | File Name |
| 38 | Record Name |
| 83 | For disk file, 'actual' File Name used |
| 93 | For disk file, File's Library |
| 156 | For disk file, Record Count |
| 261 | Record |
| 367 | Flags |
| 369 | For workstation file, AID ByteFor print file, Page Count |
| 370 | For workstation file, Cursor Row |
| 371 | For workstation file, Cursor Column |
| 376 | For workstation file, Subfile Relative Record Number |
| 378 | For workstation file, Subfile Lowest Relative Record Number |
| 397 | For disk file, Relative Record Number |
| \*FILE | File |
| \*RECORD | Record Name |

