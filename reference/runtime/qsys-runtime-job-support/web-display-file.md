---
title: "WebDisplayFile class          | QSYS API Reference Guide"
description: "Provides a program with an interface to the user interactions, supporting read and write operation to the user&#39;s screen. "
last_modified_at: 2024-08-09T17:25:29Z
---

Provides a program with an interface to the user interactions, supporting read and write operation to the user's screen.

**Namespace:** ASNA.QSys.Runtime.JobSupport
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [WebDisplayFile](#webdisplayfilestring-string-adgdataset-boolean)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [AdgDataSet](/reference/datagate/datagate-client/adg-data-set.html), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Initializes a new instance of a web display file.
| [WebDisplayFile](#webdisplayfilestring-string-dataset)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [DataSet](https://docs.microsoft.com/en-us/dotnet/api/system.data.dataset)) | Initializes a new instance of a web display file.

### WebDisplayFile([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [AdgDataSet](/reference/datagate/datagate-client/adg-data-set.html), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Initializes a new instance of a web display file.

```cs
WebDisplayFile(String, String, AdgDataSet, Boolean)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | fileName | Name of the display file.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | pageName | Web page name used to identify the display file.
| [AdgDataSet](/reference/datagate/datagate-client/adg-data-set.html) | dataSet | Dataset used as the data buffer for the records of the display file.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | shared | true to indicate that the display file can be shared with other programs using the same device; otherwise false.

### WebDisplayFile([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [DataSet](https://docs.microsoft.com/en-us/dotnet/api/system.data.dataset))

Initializes a new instance of a web display file.

```cs
WebDisplayFile(String, String, DataSet)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | fileName | Name of the display file.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | pageName | Web page name used to identify the display file.
| [DataSet](https://docs.microsoft.com/en-us/dotnet/api/system.data.dataset) | dataSet | Dataset used as the data buffer for the records of the display file.

## Properties

| Type | Name | Description
| --- | --- | --- 
| [DataSet](https://docs.microsoft.com/en-us/dotnet/api/system.data.dataset) | DataSet | Gets the dataset containing the data for the records of the display file. |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | DisplayErrorMessages | Gets a value that indicates whether to display error messages. |
| [Int16](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | FeedbackActiveWindowCursor | Gets or sets the cursor position on the active window. |
| [Byte](https://docs.microsoft.com/en-us/dotnet/api/system.byte) | FeedbackAID | Gets or sets the device's attention identifier (AID) key pressed. |
| [Int16](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | FeedbackCursor | Gets or sets the device's cursor position. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | FeedbackField | Gets or set the name of the field where the cursor was position when the AID key was pressed. |
| [Int16](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | FeedbackFlags | Gets an indication of the last key pressed: a value of 0 if it was a function key, otherwise a 4. |
| [Int16](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | FeedbackLowestSubfile | Gets or sets the subfile record number on first record displayed on the screen when the AID key was pressed. |
| [Int16](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | FeedbackSubfileCursorRRN | Gets or sets the subfile record number where the cursor was position when the AID key was pressed. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | HostResult | Result from HostService. |
| [HostService](/reference/runtime/qsys-runtime-job-support/host-service.html) | HostService | Requested service from the (IBM i) Host. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | LastFormatName | Gets or sets the name of the last format name of the display file used to output data. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | PageName | Gets the page name that identifies this display file. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | SvcString | Parameter of HostService. |

## Methods

| Signature | Description |
| --- | --- |
| [Attach()](#adgdataset-attach) | Attaches a new use of the display file.
| [ClearSubfile](#void-clearsubfilestring-subfilename)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Clears the dataset's table used as the bufer for a subfile.
| [Close()](#void-close) | Closes the display file disposing of its resources.
| [DeactivateFormats](#void-deactivateformatsstring-formatnames-string-excludeformatchildren)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Marks a set of record formats as not being available for being displayed on the device.
| [DisplaySubfileRecords](#void-displaysubfilerecordsstring-subfilename)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Marks a subfile as being active and available to be displayed at the device.
| [GetCurrentRow](#int-getcurrentrowstring-formatname)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Gets the current, or active, row number for a record format.
| [GetSharedFile](#webdisplayfile-getsharedfilestring-dclfilename)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Gets a sharable display file.
| [InitMessageSubfile](#void-initmessagesubfilestring-subfilename-string-programq-char--optionindicators)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Char\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.char)) | Initialized the records of a subfile with the messages on a program's message queue.
| [IsActive](#bool-isactivestring-formatname)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Gets a value indicating whether a record format is active or not.
| [Open()](#void-open) | Opens the display file for IO operations, allocating the dataset buffer for the file's records.
| [Read()](#void-read) | Presents the current data on the device and waits for the user to enter new data. 
| [SetActive](#void-setactivestring-formatname)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Marks a record format as being active.
| [SetCurrentRow](#void-setcurrentrowstring-formatname-int-row)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Sets the current, or acive, row number for a record format.
| [Update()](#void-update) | Checks to see if the job should shutdown.
| [Write()](#void-write) | Checks to see if the job should shutdown.

### AdgDataSet Attach()

Attaches a new use of the display file.

```cs
AdgDataSet Attach()
```

### void ClearSubfile([string subfileName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Clears the dataset's table used as the bufer for a subfile.

```cs
void ClearSubfile(string subfileName)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | subfileName | The name of the sufile to clear.

### void Close()

Closes the display file disposing of its resources.

```cs
void Close()
```

### void DeactivateFormats([string formatNames](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string excludeFormatChildren](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Marks a set of record formats as not being available for being displayed on the device.

```cs
void DeactivateFormats(string formatNames, string excludeFormatChildren)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatNames | A comma separated list of the record formats to clear.  Use *ALL to deactivate all the records of the display file.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | excludeFormatChildren | The name of the format whose children should not be affected when deactiating *ALL records.

### void DisplaySubfileRecords([string subfileName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Marks a subfile as being active and available to be displayed at the device.

```cs
void DisplaySubfileRecords(string subfileName)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | subfileName | The name of the sufile to clear.

### int GetCurrentRow([string formatName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Gets the current, or active, row number for a record format.

```cs
int GetCurrentRow(string formatName)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatName | The name of the record format.

#### Returns

| Type | Description
| --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | The current row number.

### WebDisplayFile GetSharedFile([string DclFileName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Gets a sharable display file.

```cs
WebDisplayFile GetSharedFile(string DclFileName)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | DclFileName | The name of the display file to get.

#### Returns

| Type | Description
| --- | ---
| [WebDisplayFile](/reference/runtime/qsys-runtime-job-support/web-display-file.html) | The sharable display file. Null if one is not found.

### void InitMessageSubfile([string subfileName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string programQ](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [Char\[\] optionIndicators](https://docs.microsoft.com/en-us/dotnet/api/system.char))

Initialized the records of a subfile with the messages on a program's message queue.

```cs
void InitMessageSubfile(string subfileName, string programQ, Char[] optionIndicators)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | subfileName | The name of the subfile file to initialize.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | programQ | The program queue identifier.
| [Char\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.char) | optionIndicators | A set of 100 option indicators to associate with each subfile record.

### bool IsActive([string formatName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Gets a value indicating whether a record format is active or not.

```cs
bool IsActive(string formatName)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatName | The name of the record format.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | True if the record format is active.

### void Open()

Opens the display file for IO operations, allocating the dataset buffer for the file's records.

```cs
void Open()
```

### void Read()

Presents the current data on the device and waits for the user to enter new data. 

```cs
void Read()
```

### void SetActive([string formatName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Marks a record format as being active.

```cs
void SetActive(string formatName)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatName | The name of the record format.

### void SetCurrentRow([string formatName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [int row](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Sets the current, or acive, row number for a record format.

```cs
void SetCurrentRow(string formatName, int row)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatName | The name of the record format.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | row | The new current row number.

### void Update()

Checks to see if the job should shutdown.

```cs
void Update()
```

### void Write()

Checks to see if the job should shutdown.

```cs
void Write()
```
