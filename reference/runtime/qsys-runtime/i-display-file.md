---
title: "IDisplayFile interface        | QSYS API Reference Guide"
description: "Defines the interface for display files, providing methods and properties for interacting with display file records and formats. "
last_modified_at: 2024-08-08T21:41:46Z
---

Defines the interface for display files, providing methods and properties for interacting with display file records and formats.

**Namespace:** ASNA.QSys.Runtime
**Assembly:** ASNA.QSys.Runtime.dll

**Extends:** doesn't extend any other interfaces.
<br>
<br>

## Properties

| Type | Name | Description
| --- | --- | --- 
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | DisplayErrorMessages | Determines if the Error Message Subfile should be displayed. |
| [Int16](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | FeedbackActiveWindowCursor | Displayfile Feedback Last Cursor position for Active Window record (row, col). |
| [Byte](https://docs.microsoft.com/en-us/dotnet/api/system.byte) | FeedbackAID | Displayfile Feedback Attention Identifier. |
| [Int16](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | FeedbackCursor | Displayfile Feedback Last Cursor position (row, col). |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | FeedbackField | Displayfile Feedback last field name where cursor was positioned. |
| [Int16](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | FeedbackFlags | Displayfile Feedback flags. |
| [Int16](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | FeedbackLowestSubfile | Displayfile Feedback Lowest subfile Relative Record Number visible. |
| [Int16](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | FeedbackSubfileCursorRRN | Gets or sets the subfile record number where the cursor was position when the AID key was pressed. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | LastFormatName | Displayfile Feedback last format name where cursor was positioned. |

## Methods

| Signature | Description |
| --- | --- |
| [ClearSubfile](#void-clearsubfilestring-subfilename)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Clear Subfile.
| [Close()](#void-close) | Close Display File.
| [DeactivateFormats](#void-deactivateformatsstring-formatnames-string-excludeformatchildren)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | De-activate Display File record formats.
| [DisplaySubfileRecords](#void-displaysubfilerecordsstring-subfilename)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Display subfile records.
| [GetCurrentRow](#int-getcurrentrowstring-formatname)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Get current row.
| [InitMessageSubfile](#void-initmessagesubfilestring-subfilename-string-programq-char--optionindicators)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Char\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.char)) | Initializes Message subfile.
| [IsActive](#bool-isactivestring-formatname)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Determines if Record format is Active.
| [Open()](#void-open) | Open Display File.
| [Read()](#void-read) | Read Display File.
| [SetActive](#void-setactivestring-formatname)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Set the record format as Active.
| [SetCurrentRow](#void-setcurrentrowstring-formatname-int-row)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Set current row.
| [Update()](#void-update) | Update Display File.
| [Write()](#void-write) | Write Display File.

### void ClearSubfile([string subfileName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Clear Subfile.

```cs
void ClearSubfile(string subfileName)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | subfileName | Input subfile name.

### void Close()

Close Display File.

```cs
void Close()
```

### void DeactivateFormats([string formatNames](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string excludeFormatChildren](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

De-activate Display File record formats.

```cs
void DeactivateFormats(string formatNames, string excludeFormatChildren)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatNames | Input record format names.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | excludeFormatChildren | Input child record formats to exclude.

### void DisplaySubfileRecords([string subfileName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Display subfile records.

```cs
void DisplaySubfileRecords(string subfileName)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | subfileName | Input subfile name.

### int GetCurrentRow([string formatName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Get current row.

```cs
int GetCurrentRow(string formatName)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatName | Input record format name.

#### Returns

| Type | Description
| --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | Relative Record Number.

### void InitMessageSubfile([string subfileName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string programQ](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [Char\[\] optionIndicators](https://docs.microsoft.com/en-us/dotnet/api/system.char))

Initializes Message subfile.

```cs
void InitMessageSubfile(string subfileName, string programQ, Char[] optionIndicators)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | subfileName | Input subfile name.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | programQ | Input Program Q.
| [Char\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.char) | optionIndicators | Input option indicator collection.

### bool IsActive([string formatName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Determines if Record format is Active.

```cs
bool IsActive(string formatName)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatName | Input record format name.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | True if active, False otherwise.

### void Open()

Open Display File.

```cs
void Open()
```

### void Read()

Read Display File.

```cs
void Read()
```

### void SetActive([string formatName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Set the record format as Active.

```cs
void SetActive(string formatName)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatName | Input record format name.

### void SetCurrentRow([string formatName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [int row](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Set current row.

```cs
void SetCurrentRow(string formatName, int row)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatName | Input record format name.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | row | Input Relative Record Number.

### void Update()

Update Display File.

```cs
void Update()
```

### void Write()

Write Display File.

```cs
void Write()
```
