---
title: "OpenAccessFile class          | QSYS API Reference Guide"
description: "Provides the facilities to use a display file without prior infrastructure. "
last_modified_at: 2024-08-09T17:25:29Z
---

Provides the facilities to use a display file without prior infrastructure.

**Namespace:** ASNA.QSys.Runtime.JobSupport
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [OpenAccessFile](#openaccessfilestring)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Initializes a new instance of the OpenAccessFile class for the razor display page.

### OpenAccessFile([String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Initializes a new instance of the OpenAccessFile class for the razor display page.

```cs
OpenAccessFile(String)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | displayFilePath | Route to the razor display page.

## Properties

| Type | Name | Description
| --- | --- | --- 
| [DataSet](https://docs.microsoft.com/en-us/dotnet/api/system.data.dataset) | DataSet | Gets the dataset containing the data for the records of the display file. |
| [Byte](https://docs.microsoft.com/en-us/dotnet/api/system.byte) | FeedbackAID | Gets or sets the device's attention identifier (AID) key pressed. |
| [Int16](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | FeedbackCursor | Gets or sets the device's cursor position. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | FeedbackField | Gets or set the name of the field where the cursor was position when the AID key was pressed. |
| [Int16](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | FeedbackLowestSubfile | Gets or sets the subfile record number on first record displayed on the screen when the AID key was pressed. |
| [Int16](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | FeedbackSubfileCursorRRN | Gets or sets the subfile record number where the cursor was position when the AID key was pressed. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | LibraryNameFound | Gets the library where file was found. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | OpenAccessFileID | Unique file identifier. |

## Methods

| Signature | Description |
| --- | --- |
| [ClearRecords](#void-clearrecordsstring-formatname)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Clears all the data from a record format's buffer.
| [Close()](#void-close) | Closes the display file disposing of its resources.
| [Dispose](#void-disposebool-disposing)([Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Closes the file and releases the resources used by the current instance of the OpenAccessFile class.
| [Dispose()](#void-dispose) | Closes the file and releases the resources used by the current instance of the OpenAccessFile class.
| [Extend](#void-extendstring-formatname-char--optionindicators-action-string-datarow-object-populatebuffer-object-popcookie)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Char\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.char), [Action\<String, DataRow, Object\>](https://learn.microsoft.com/en-us/dotnet/api/system.action?view=net-8.0), [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | Adds a record to the record format's buffer.
| [Open()](#int-open) | Opens the display file for IO operations, allocating the dataset buffer for the file's records.
| [Read()](#void-read) | Presents the current data on the device and waits for the user to enter new data. 
| [Write](#void-writestring-formatname-char--optionindicators-action-string-datarow-object-populatebuffer-object-popcookie)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Char\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.char), [Action\<String, DataRow, Object\>](https://learn.microsoft.com/en-us/dotnet/api/system.action?view=net-8.0), [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | Adds a record to the record format's buffer.

### void ClearRecords([string formatName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Clears all the data from a record format's buffer.

```cs
void ClearRecords(string formatName)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatName | The name of the record format to clear.

### void Close()

Closes the display file disposing of its resources.

```cs
void Close()
```

### void Dispose([bool disposing](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Closes the file and releases the resources used by the current instance of the OpenAccessFile class.

```cs
void Dispose(bool disposing)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | disposing | true to perfom the closing and releasing.

### void Dispose()

Closes the file and releases the resources used by the current instance of the OpenAccessFile class.

```cs
void Dispose()
```

### void Extend([string formatName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [Char\[\] optionIndicators](https://docs.microsoft.com/en-us/dotnet/api/system.char), [Action\<string, DataRow, object\> populateBuffer](https://learn.microsoft.com/en-us/dotnet/api/system.action?view=net-8.0), [object popCookie](https://docs.microsoft.com/en-us/dotnet/api/system.object))

Adds a record to the record format's buffer.

```cs
void Extend(string formatName, Char[] optionIndicators, Action<string, DataRow, object> populateBuffer, object popCookie)
```

### int Open()

Opens the display file for IO operations, allocating the dataset buffer for the file's records.

```cs
int Open()
```

### void Read()

Presents the current data on the device and waits for the user to enter new data. 

```cs
void Read()
```

### void Write([string formatName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [Char\[\] optionIndicators](https://docs.microsoft.com/en-us/dotnet/api/system.char), [Action\<string, DataRow, object\> populateBuffer](https://learn.microsoft.com/en-us/dotnet/api/system.action?view=net-8.0), [object popCookie](https://docs.microsoft.com/en-us/dotnet/api/system.object))

Adds a record to the record format's buffer.

```cs
void Write(string formatName, Char[] optionIndicators, Action<string, DataRow, object> populateBuffer, object popCookie)
```
