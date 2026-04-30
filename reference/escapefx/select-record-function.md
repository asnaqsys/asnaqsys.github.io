---
title: "SelectRecordFunction Class"
description: "Abstract base class for subfile-based record selection in ASNA.QSys.EscapeFX."
---

## Definition

**Namespace:** ASNA.QSys.EscapeFX  
**Assembly:** ASNA.QSys.EscapeFX.dll  
**Inherits:** [SubfileProgram](subfile-program.html)

Abstract base class for programs that allow users to select records from a subfile list.

## Constructors

| Signature | Description |
| --- | --- |
| `SelectRecordFunction()` | Initializes a new instance of the SelectRecordFunction class. |

## Methods

| Signature | Description |
| --- | --- |
| [abstract void InitSubfile()](select-record-function-init-subfile.html) | Initializes and loads the subfile. Must be overridden. |
| [abstract void LoadSubfile()](select-record-function-load-subfile.html) | Loads subfile records. Must be overridden. |
| [abstract void ProcessScreen()](select-record-function-process-screen.html) | Processes screen input. Must be overridden. |
| [abstract void ProcessSubfileRecord()](select-record-function-process-subfile-record.html) | Processes a selected subfile record. Must be overridden. |
| [virtual void ConvertControlToExternal()](select-record-function-convert-control-to-external.html) | Converts control fields to external display form. |
| [virtual void SelectRecord()](select-record-function-select-record.html) | Main loop for the record selection screen. |
| [override void ShowScreen()](select-record-function-show-screen.html) | Displays the screen and resets invite/error indicators. |
| [override void ProcessSubfile()](select-record-function-process-subfile.html) | Processes changed subfile records. |
| [virtual void EstablishSubfileLimits()](select-record-function-establish-subfile-limits.html) | Establishes the subfile limits for reading. |
| [override void CancelProgram()](select-record-function-cancel-program.html) | Sends "no value selected" message and exits. |
| [override void ConvertMajorFieldsToExternalForm()](select-record-function-convert-major-fields-to-external-form.html) | Delegates to ConvertControlToExternal. |

## See Also
- [SubfileProgram](subfile-program.html)
- [DisplayFileFunction](display-file-function.html)