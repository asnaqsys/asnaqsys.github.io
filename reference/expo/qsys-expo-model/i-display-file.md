---
title: "IDisplayFile interface        | QSYS API Reference Guide"
description: "Exposes DisplayFile properties and methods "
last_modified_at: 2024-08-08T21:42:10Z
---

Exposes DisplayFile properties and methods

**Namespace:** ASNA.QSys.Expo.Model
**Assembly:** ASNA.QSys.Expo.Model.dll

**Extends:** doesn't extend any other interfaces.
<br>
<br>

## Remarks

Encapsulates the portion if the class that implements this interface with properties and methods that are common between the Application logic and the Interactive Website.

The interface is used by ASNA.QSys.Runtime's [Workstation file concept](/concepts/user-interface/qsys-expo-display-pages.html) maintaining the two assemblies (ASNA.QSys.Expo and ASNA.QSys.Runtime) [Loosely coupled](https://en.wikipedia.org/wiki/Loose_coupling).  

## Properties

| Type | Name | Description
| --- | --- | --- 
| [DataSet](https://docs.microsoft.com/en-us/dotnet/api/system.data.dataset) | DataSet | Gets the DisplayFile DataSet |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | DisplayErrorMessages | Gets a boolean value that indicates if the Error Messages should be displayed |
| [Int16](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | FeedbackActiveWindowCursor | If a Window Record is active, this property gets or sets a value that indicates Cursor (row, column) corresponding to the last location last user input (Hi byte is the row, Lo-byte is the column) |
| [Byte](https://docs.microsoft.com/en-us/dotnet/api/system.byte) | FeedbackAID | Gets a value that indicates the AID code sent in last user request |
| [Int16](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | FeedbackCursor | Gets a value that indicates Cursor (row, column) corresponding to the last location last user input (Hi byte is the row, Lo-byte is the column) |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | FeedbackField | Gets a value that indicates the name of the last Field where the Cursor was positioned, corresponding to the last location last user input |
| [Int16](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | FeedbackFlags | Gets a value that indicates Miscellaneous feedback flags. Bit 1: Cancel-read indicator. Bit 2: Data-returned indicator. Bit 3: Command key indicator. Bits 4-16: Reserved. |
| [Int16](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | FeedbackLowestSubfile | Gets a value that indicates the indicates the lowest subfile relative record number currently displayed in the uppermost subfile display area if the last write operation was done to the subfile control record with 'Subfile Display' specified. Updated for roll up and roll down operations. Reset to 0 on a write operation to another record. Not set for message subfiles |
| [Int16](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | FeedbackSubfileCursorRRN | Gets or sets a value that indicates Relative Record Number of a subfile record.  For input operations, updated only if data is returned to the program. If multiple subfiles are on the display, this offset will contain the relative record number for the last subfile updated. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | InstanceId | Gets a value that indicates the Unique Page instance ID |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | LastFormatNameWritten | Gets a value that indicates the name of the last Record Format written |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | PageName | Gets a value that indicates the Name of the Page (URL) |

## Methods

| Signature | Description |
| --- | --- |
| [AddCallHostSpecs](#int-addcallhostspecscallhostspecs-buildoptionsspecs)([CallHostSpecs](/reference/expo/qsys-expo-model/call-host-specs.html)) | Will throw NonImplemented exception
| [GetTopRecordOnInput](#int-gettoprecordoninputstring-format)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Gets the Subfile Top Relative Record Number in the last input operation
| [SetOneTimeDefaultValue](#bool-setonetimedefaultvaluestring-fieldid)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Marks a field as one that has had a Default value (internal use) 
| [SetTopRecordOnInput](#void-settoprecordoninputstring-formatname-int-rrn)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Sets the Subfile Top Relative Record Number for the last input operation

### int AddCallHostSpecs([CallHostSpecs buildOptionsSpecs](/reference/expo/qsys-expo-model/call-host-specs.html))

Will throw NonImplemented exception

```cs
int AddCallHostSpecs(CallHostSpecs buildOptionsSpecs)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [CallHostSpecs](/reference/expo/qsys-expo-model/call-host-specs.html) | buildOptionsSpecs | CallHostSpecs instance

#### Returns

| Type | Description
| --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | throws exception

### int GetTopRecordOnInput([string format](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Gets the Subfile Top Relative Record Number in the last input operation

```cs
int GetTopRecordOnInput(string format)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | format | subfile record name

#### Returns

| Type | Description
| --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | the relative record number at the top

### bool SetOneTimeDefaultValue([string fieldID](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Marks a field as one that has had a Default value (internal use) 

```cs
bool SetOneTimeDefaultValue(string fieldID)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | fieldID | field name

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | true the field was not marked as having a Default value

### void SetTopRecordOnInput([string formatName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [int rrn](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Sets the Subfile Top Relative Record Number for the last input operation

```cs
void SetTopRecordOnInput(string formatName, int rrn)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatName | subfile record name
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | rrn | relative record number
