---
title: "WorkstationFileBase class     | QSYS API Reference Guide"
description: "Base class for Workstation files. It contains functionality to support common input/output operations on Workstation files. "
last_modified_at: 2024-08-08T21:41:46Z
---

Base class for Workstation files. It contains functionality to support common input/output operations on Workstation files.

**Namespace:** ASNA.QSys.Runtime
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [FileBase](/reference/runtime/qsys-runtime/file-base.html)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [WorkstationFileBase](#workstationfilebasestring-string-boolean)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Initializes a new instance of the WorkstationFileBase class.
| [WorkstationFileBase](#workstationfilebasestring-string-boolean-action)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [Action](https://learn.microsoft.com/en-us/dotnet/api/system.action?view=net-8.0)) | Initializes a new instance of the WorkstationFileBase class.

### WorkstationFileBase([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Initializes a new instance of the WorkstationFileBase class.

```cs
WorkstationFileBase(String, String, Boolean)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | dclWorkstationFileName | Field name for this file in the program.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | filePath | Path to the file in the Database, given as "library/filename".
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | shareOpenDataPath | True to indicate that the file can be shared with other programs; otherwise false.

### WorkstationFileBase([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [Action](https://learn.microsoft.com/en-us/dotnet/api/system.action?view=net-8.0))

Initializes a new instance of the WorkstationFileBase class.

```cs
WorkstationFileBase(String, String, Boolean, Action)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | dclWorkstationFileName | Field name for this file in the program.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | filePath | Path to the file in the Database, given as "library/filename".
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | shareOpenDataPath | True to indicate that the file can be shared with other programs; otherwise false.
| [Action](https://learn.microsoft.com/en-us/dotnet/api/system.action?view=net-8.0) | infSR | Method called when there is an error in a file operation.

## Properties

| Type | Name | Description
| --- | --- | --- 
| [Int16](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | DisplayFileSubfileCursorRRN | Gets the subfile record number where the cursor was position when the AID key was pressed. |
| [Int16](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | FeedbackActiveWindowCursor | Gets the display file feedback active window cursor position. |
| [Int16](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | FeedbackActiveWindowCursorCol | Gets the display file feedback active window cursor column. |
| [Int16](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | FeedbackActiveWindowCursorRow | Gets the display file feedback active window cursor row. |
| [Byte](https://docs.microsoft.com/en-us/dotnet/api/system.byte) | FeedbackAID | Gets the display file feedback attention identifier. |
| [Int16](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | FeedbackCursor | Gets the display file feedback cursor position. |
| [Int16](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | FeedbackCursorCol | Gets the display file feedback cursor column. |
| [Int16](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | FeedbackCursorRow | Gets the display file feedback cursor row. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | FeedbackField | Gets the diaplsy file feedback last field name where cursor was positioned. |
| [Int16](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | FeedbackFlags | Gets the display file feedback flags. |
| [Int16](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | FeedbackLowestSubfile | Gets the display file feedback lowest visible subfile relative record number. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | FeedbackSubfileRecords | Gets the count of subfile records. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | FilePath | Gets or sets the path to the file in the Database, given as "library/filename". |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | FormatName | Gets the last-used record format name. |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | INKA | F1 |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | INKB | F2 |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | INKC | F3 |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | INKD | F4 |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | INKE | F5 |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | INKF | F6 |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | INKG | F7 |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | INKH | F8 |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | INKI | F9 |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | INKJ | F10 |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | INKK | F11 |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | INKL | F12 |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | INKM | F13 |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | INKN | F14 |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | INKP | F15 |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | INKQ | F16 |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | INKR | F17 |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | INKS | F18 |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | INKT | F19 |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | INKU | F20 |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | INKV | F21 |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | INKW | F22 |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | INKX | F23 |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | INKY | F24 |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | SflRRN | Gets the relative record number (1-based) of the last Subfile operation. |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | ShareOpenDataPath | Gets or sets a value to indicate that the file can be shared with other programs. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | StarDirectionIn | String with the value "I" |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | StarDirectionInAttn | String with the value "N" |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | StarDirectionNotActive | String with the value "X" |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | StarDirectionOut | String with the value "O" |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | StarDirectionRead | String with the value "R" |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | StarDirectionReadAttn | String with the value "A" |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | StarDirectionVoid | String with the value "V" |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | StarDirFieldName | String with the value "*Direction" |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | StarOptionIndFieldName | String with the value "*Indicators" |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | StarResponseIndFieldName | String with the value "*ResponseIndicators" |

## Methods

| Signature | Description |
| --- | --- |
| [attachBuffer](#void-attachbufferadgdataset-adgdataset)([AdgDataSet](/reference/datagate/datagate-client/adg-data-set.html)) | When overriden in a derived class, set this file's DataSet to the given AdgDataSet.
| [chainKey](#void-chainkeystring-formatname-adgkeytable-key-bool-nolock)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [AdgKeyTable](/reference/datagate/datagate-client/adg-key-table.html), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Executes CHAIN by search Key override. Throws: CHAIN not supported on WorkstationFiles Exception.
| [chainKey](#void-chainkeystring-formatname-adgkeytable-key-bool-nolock-ids-ds)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [AdgKeyTable](/reference/datagate/datagate-client/adg-key-table.html), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [IDS](/reference/runtime/qsys-runtime/ids.html)) | Executes CHAIN by search Key override. Throws: CHAIN not supported on WorkstationFiles Exception.
| [chainRRN](#void-chainrrnstring-formatname-int-rrn-ids-indds)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [IDS](/reference/runtime/qsys-runtime/ids.html)) | Executes CHAIN by Relative Record Number.
| [chainRRN](#void-chainrrnstring-formatname-int-rrn-char--indicators)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Char\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.char)) | Executes CHAIN by Relative Record Number.
| [chainRRN](#void-chainrrnstring-formatname-int-rrn-bool-nolock)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | For backwards compatibility with programs compiled prior to v12.0
| [chainRRN](#void-chainrrnstring-formatname-int-rrn-bool-nolock-ids-intods)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [IDS](/reference/runtime/qsys-runtime/ids.html)) | Executes CHAIN by Relative Record Number override. (Not implemented).
| [ChainRRN](#void-chainrrnstring-formatname-int-rrn-ids-indds)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [IDS](/reference/runtime/qsys-runtime/ids.html)) | Executes CHAIN by Relative Record Number.
| [ChainRRN](#void-chainrrnstring-formatname-int-rrn-char--indicators)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Char\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.char)) | Executes CHAIN by Relative Record Number.
| [close()](#void-close) | Closes Workstation file.
| [deleteByRRN](#void-deletebyrrnstring-formatname-int-rrn)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Executes DELETE by Relative Record Number.
| [exFmt](#void-exfmtstring-formatname-ids-indds)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [IDS](/reference/runtime/qsys-runtime/ids.html)) | Executes EXFMT operation.
| [exFmt](#void-exfmtstring-formatname-char--optionindicators)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Char\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.char)) | Executes EXFMT operation.
| [ExFmt](#void-exfmtstring-formatname-ids-indds)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [IDS](/reference/runtime/qsys-runtime/ids.html)) | Executes EXFMT operation.
| [ExFmt](#void-exfmtstring-formatname-char--optionindicators)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Char\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.char)) | Executes EXFMT operation.
| [insert](#void-insertstring-formatname-int-rrn)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Insert a row in the current record.
| [open()](#void-open) | Opens Workstation File.
| [Open()](#void-open) | Opens Workstation File.
| [read](#void-readstring-formatname-ids-indds)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [IDS](/reference/runtime/qsys-runtime/ids.html)) | Executes READ operation.
| [read](#void-readstring-formatname-char--indicators)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Char\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.char)) | Executes READ operation.
| [Read](#void-readstring-formatname-ids-indds)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [IDS](/reference/runtime/qsys-runtime/ids.html)) | Executes READ operation.
| [Read](#void-readstring-formatname-char--indicators)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Char\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.char)) | Executes READ operation.
| [readNextChanged](#int-readnextchangedstring-formatname-int-originalrrn-ids-indds)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [IDS](/reference/runtime/qsys-runtime/ids.html)) | Executes Workstationfile READ NEXT record CHANGED operation.
| [readNextChanged](#int-readnextchangedstring-formatname-int-originalrrn-char--indicators)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Char\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.char)) | Executes Workstationfile READ NEXT record CHANGED operation.
| [ReadNextChanged](#int-readnextchangedstring-formatname-int-originalrrn-ids-indds)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [IDS](/reference/runtime/qsys-runtime/ids.html)) | Executes Workstationfile READ NEXT record CHANGED operation.
| [ReadNextChanged](#int-readnextchangedstring-formatname-int-originalrrn-char--indicators)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Char\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.char)) | Executes Workstationfile READ NEXT record CHANGED operation.
| [update](#void-updatestring-formatname-char--optionindicators)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Char\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.char)) | Execute UPDATE subfile record operation. 
| [updateFlds](#void-updatefldsstring-formatname-string--fieldnames)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Execute UPDATE FIELDS operation.
| [write](#void-writestring-formatname-char--optionindicators)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Char\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.char)) | Executes WRITE record operation.
| [write](#void-writestring-formatname-char--optionindicators-ids-fromds)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Char\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.char), [IDS](/reference/runtime/qsys-runtime/ids.html)) | Executes WRITE record operation.
| [writeSubfile](#void-writesubfilestring-formatname-int-rrn-char--optionindicators)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Char\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.char)) | Write a subfile record.

### void attachBuffer([AdgDataSet adgDataSet](/reference/datagate/datagate-client/adg-data-set.html))

When overriden in a derived class, set this file's DataSet to the given AdgDataSet.

```cs
void attachBuffer(AdgDataSet adgDataSet)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [AdgDataSet](/reference/datagate/datagate-client/adg-data-set.html) | adgDataSet | The dataset to attach.

### void chainKey([string formatName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [AdgKeyTable key](/reference/datagate/datagate-client/adg-key-table.html), [bool noLock](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Executes CHAIN by search Key override. Throws: CHAIN not supported on WorkstationFiles Exception.

```cs
void chainKey(string formatName, AdgKeyTable key, bool noLock)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatName | Not used.
| [AdgKeyTable](/reference/datagate/datagate-client/adg-key-table.html) | key | Not used.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | noLock | Not used.

### void chainKey([string formatName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [AdgKeyTable key](/reference/datagate/datagate-client/adg-key-table.html), [bool noLock](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [IDS ds](/reference/runtime/qsys-runtime/ids.html))

Executes CHAIN by search Key override. Throws: CHAIN not supported on WorkstationFiles Exception.

```cs
void chainKey(string formatName, AdgKeyTable key, bool noLock, IDS ds)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatName | Not used.
| [AdgKeyTable](/reference/datagate/datagate-client/adg-key-table.html) | key | Not used.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | noLock | Not used.
| [IDS](/reference/runtime/qsys-runtime/ids.html) | ds | Not used.

### void chainRRN([string formatName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [int rrn](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [IDS indDS](/reference/runtime/qsys-runtime/ids.html))

Executes CHAIN by Relative Record Number.

```cs
void chainRRN(string formatName, int rrn, IDS indDS)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatName | Record format name.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | rrn | Relative Record Number.
| [IDS](/reference/runtime/qsys-runtime/ids.html) | indDS | Indicator Data Structure

### void chainRRN([string formatName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [int rrn](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [Char\[\] indicators](https://docs.microsoft.com/en-us/dotnet/api/system.char))

Executes CHAIN by Relative Record Number.

```cs
void chainRRN(string formatName, int rrn, Char[] indicators)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatName | Record format name.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | rrn | Relative Record Number.
| [Char\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.char) | indicators | Indicator collection.

### void chainRRN([string formatName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [int rrn](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [bool noLock](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

For backwards compatibility with programs compiled prior to v12.0

```cs
void chainRRN(string formatName, int rrn, bool noLock)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatName | Record format name.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | rrn | Relative Record Number.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | noLock | Not used.

### void chainRRN([string formatName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [int rrn](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [bool noLock](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [IDS intoDS](/reference/runtime/qsys-runtime/ids.html))

Executes CHAIN by Relative Record Number override. (Not implemented).

```cs
void chainRRN(string formatName, int rrn, bool noLock, IDS intoDS)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatName | Record format name.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | rrn | Relative Record Number.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | noLock | True if locking should be performed.
| [IDS](/reference/runtime/qsys-runtime/ids.html) | intoDS | IDS object that receives the data read.

### void ChainRRN([string formatName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [int rrn](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [IDS indDS](/reference/runtime/qsys-runtime/ids.html))

Executes CHAIN by Relative Record Number.

```cs
void ChainRRN(string formatName, int rrn, IDS indDS)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatName | Record format name.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | rrn | Relative Record Number.
| [IDS](/reference/runtime/qsys-runtime/ids.html) | indDS | Indicator Data Structure.

### void ChainRRN([string formatName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [int rrn](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [Char\[\] indicators](https://docs.microsoft.com/en-us/dotnet/api/system.char))

Executes CHAIN by Relative Record Number.

```cs
void ChainRRN(string formatName, int rrn, Char[] indicators)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatName | Record format name.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | rrn | Relative Record Number.
| [Char\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.char) | indicators | Indicator collection.

### void close()

Closes Workstation file.

```cs
void close()
```

### void deleteByRRN([string formatName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [int rrn](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Executes DELETE by Relative Record Number.

```cs
void deleteByRRN(string formatName, int rrn)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatName | Format name.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | rrn | Relative Record Number.

### void exFmt([string formatName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [IDS indDS](/reference/runtime/qsys-runtime/ids.html))

Executes EXFMT operation.

```cs
void exFmt(string formatName, IDS indDS)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatName | Record format name.
| [IDS](/reference/runtime/qsys-runtime/ids.html) | indDS | Output Indicator Data Structure.

### void exFmt([string formatName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [Char\[\] optionIndicators](https://docs.microsoft.com/en-us/dotnet/api/system.char))

Executes EXFMT operation.

```cs
void exFmt(string formatName, Char[] optionIndicators)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatName | Record format name.
| [Char\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.char) | optionIndicators | Option indicator collection.

### void ExFmt([string formatName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [IDS indDS](/reference/runtime/qsys-runtime/ids.html))

Executes EXFMT operation.

```cs
void ExFmt(string formatName, IDS indDS)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatName | Record format name.
| [IDS](/reference/runtime/qsys-runtime/ids.html) | indDS | Indicator Data Structure.

### void ExFmt([string formatName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [Char\[\] optionIndicators](https://docs.microsoft.com/en-us/dotnet/api/system.char))

Executes EXFMT operation.

```cs
void ExFmt(string formatName, Char[] optionIndicators)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatName | Record format name.
| [Char\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.char) | optionIndicators | Option indicator collection.

### void insert([string formatName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [int rrn](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Insert a row in the current record.

```cs
void insert(string formatName, int rrn)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatName | Name of the record format.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | rrn | Relative record number.

### void open()

Opens Workstation File.

```cs
void open()
```

### void Open()

Opens Workstation File.

```cs
void Open()
```

### void read([string formatName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [IDS indDS](/reference/runtime/qsys-runtime/ids.html))

Executes READ operation.

```cs
void read(string formatName, IDS indDS)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatName | Record format name.
| [IDS](/reference/runtime/qsys-runtime/ids.html) | indDS | Indicator Data Structure.

### void read([string formatName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [Char\[\] indicators](https://docs.microsoft.com/en-us/dotnet/api/system.char))

Executes READ operation.

```cs
void read(string formatName, Char[] indicators)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatName | Record format name.
| [Char\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.char) | indicators | Option indicator collection.

### void Read([string formatName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [IDS indDS](/reference/runtime/qsys-runtime/ids.html))

Executes READ operation.

```cs
void Read(string formatName, IDS indDS)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatName | Record format name.
| [IDS](/reference/runtime/qsys-runtime/ids.html) | indDS | Indicator Data Structure.

### void Read([string formatName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [Char\[\] indicators](https://docs.microsoft.com/en-us/dotnet/api/system.char))

Executes READ operation.

```cs
void Read(string formatName, Char[] indicators)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatName | Record format name.
| [Char\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.char) | indicators | Option indicator collection.

### int readNextChanged([string formatName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [int originalRRN](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [IDS indDS](/reference/runtime/qsys-runtime/ids.html))

Executes Workstationfile READ NEXT record CHANGED operation.

```cs
int readNextChanged(string formatName, int originalRRN, IDS indDS)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatName | Input record format name.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | originalRRN | Input original Relative Record Number.
| [IDS](/reference/runtime/qsys-runtime/ids.html) | indDS | Input Indicator Data Structure reference.

#### Returns

| Type | Description
| --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | If record exists Relative Record Number for record that changed, otherwise original RRN.

### int readNextChanged([string formatName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [int originalRRN](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [Char\[\] indicators](https://docs.microsoft.com/en-us/dotnet/api/system.char))

Executes Workstationfile READ NEXT record CHANGED operation.

```cs
int readNextChanged(string formatName, int originalRRN, Char[] indicators)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatName | Input record format name.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | originalRRN | Input original Relative Record Number.
| [Char\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.char) | indicators | Input option indicators.

#### Returns

| Type | Description
| --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | If record exists Relative Record Number for record that changed, otherwise original RRN.

### int ReadNextChanged([string formatName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [int originalRRN](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [IDS indDS](/reference/runtime/qsys-runtime/ids.html))

Executes Workstationfile READ NEXT record CHANGED operation.

```cs
int ReadNextChanged(string formatName, int originalRRN, IDS indDS)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatName | Input record format name.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | originalRRN | Input original Relative Record Number.
| [IDS](/reference/runtime/qsys-runtime/ids.html) | indDS | Input Indicator Data Structure reference.

#### Returns

| Type | Description
| --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | If record exists Relative Record Number for record that changed, otherwise exception is thrown.

### int ReadNextChanged([string formatName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [int originalRRN](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [Char\[\] indicators](https://docs.microsoft.com/en-us/dotnet/api/system.char))

Executes Workstationfile READ NEXT record CHANGED operation.

```cs
int ReadNextChanged(string formatName, int originalRRN, Char[] indicators)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatName | Input record format name.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | originalRRN | Input original Relative Record Number.
| [Char\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.char) | indicators | Input option indicators.

#### Returns

| Type | Description
| --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | If record exists Relative Record Number for record that changed, otherwise throws exception.

### void update([string formatName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [Char\[\] optionIndicators](https://docs.microsoft.com/en-us/dotnet/api/system.char))

Execute UPDATE subfile record operation. 

```cs
void update(string formatName, Char[] optionIndicators)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatName | Record format name.
| [Char\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.char) | optionIndicators | Option indicators.

### void updateFlds([string formatName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [String\[\] fieldNames](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Execute UPDATE FIELDS operation.

```cs
void updateFlds(string formatName, String[] fieldNames)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatName | Record format name.
| [String\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.string) | fieldNames | Collection of field names.

### void write([string formatName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [Char\[\] optionIndicators](https://docs.microsoft.com/en-us/dotnet/api/system.char))

Executes WRITE record operation.

```cs
void write(string formatName, Char[] optionIndicators)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatName | Record format name/
| [Char\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.char) | optionIndicators | Option indicator collection.

### void write([string formatName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [Char\[\] optionIndicators](https://docs.microsoft.com/en-us/dotnet/api/system.char), [IDS fromDS](/reference/runtime/qsys-runtime/ids.html))

Executes WRITE record operation.

```cs
void write(string formatName, Char[] optionIndicators, IDS fromDS)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatName | Record format name/
| [Char\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.char) | optionIndicators | Option indicator collection.
| [IDS](/reference/runtime/qsys-runtime/ids.html) | fromDS | Input data from Data Structure.

### void writeSubfile([string formatName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [int rrn](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [Char\[\] optionIndicators](https://docs.microsoft.com/en-us/dotnet/api/system.char))

Write a subfile record.

```cs
void writeSubfile(string formatName, int rrn, Char[] optionIndicators)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatName | Name of the record format to write.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | rrn | Relative record number.
| [Char\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.char) | optionIndicators | Indicator array to use in the write operation.
