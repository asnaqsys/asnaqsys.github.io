---
title: "DisplayFileFunction Class"
description: "Abstract base class for displaying file records in subfiles in ASNA.QSys.EscapeFX."
---

## Definition

**Namespace:** ASNA.QSys.EscapeFX  
**Assembly:** ASNA.QSys.EscapeFX.dll  
**Inherits:** [SubfileProgram](subfile-program.html)

Abstract base class for programs that display file records in a read-only subfile.

## Constructors

| Signature | Description |
| --- | --- |
| `DisplayFileFunction()` | Initializes a new instance of the DisplayFileFunction class. |

## Methods

| Signature | Description |
| --- | --- |
| [abstract void InitSubfile()](display-file-function-init-subfile.html) | Initializes the subfile. Must be overridden. |
| [abstract void LoadSubfile()](display-file-function-load-subfile.html) | Loads subfile records. Must be overridden. |
| [abstract void ProcessScreen()](display-file-function-process-screen.html) | Processes screen input. Must be overridden. |
| [virtual void ProcessSubfileRecord()](display-file-function-process-subfile-record.html) | Processes a subfile record. |
| [virtual void UpdateSubfileRecordDB()](display-file-function-update-subfile-record-db.html) | Updates a subfile record to the database. |
| [virtual void ConvertControlToExternal()](display-file-function-convert-control-to-external.html) | Converts control fields to external form. |
| [virtual void DisplayFile()](display-file-function-display-file.html) | Main loop for the display file screen. |
| [override void ShowScreen()](display-file-function-show-screen.html) | Displays the screen and resets invite/error indicators. |
| [override void ProcessSubfile()](display-file-function-process-subfile.html) | Processes changed subfile records. |
| [virtual void UpdateSubfileDB()](display-file-function-update-subfile-db.html) | Processes all modified subfile records to the database. |
| [virtual void EstablishSubfileLimits()](display-file-function-establish-subfile-limits.html) | Establishes subfile limits for reading. |
| [override void CancelProgram()](display-file-function-cancel-program.html) | Exits the program directly. |
| [override void ConvertMajorFieldsToExternalForm()](display-file-function-convert-major-fields-to-external-form.html) | Delegates to ConvertControlToExternal. |

## See Also
- [SubfileProgram](subfile-program.html)
- [EditFileFunction](edit-file-function.html)