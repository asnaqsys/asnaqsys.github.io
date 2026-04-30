---
title: "EditFileFunction Class"
description: "Abstract base class for editing file records in subfiles in ASNA.QSys.EscapeFX."
---

## Definition

**Namespace:** ASNA.QSys.EscapeFX  
**Assembly:** ASNA.QSys.EscapeFX.dll  
**Inherits:** [SubfileProgram](subfile-program.html)

Abstract base class for programs that edit file records in a subfile, supporting ADD and CHG modes.

## Constructors

| Signature | Description |
| --- | --- |
| `EditFileFunction()` | Initializes a new instance of the EditFileFunction class. |

## Methods

| Signature | Description |
| --- | --- |
| [virtual void InitSubfile()](edit-file-function-init-subfile.html) | Initializes the subfile. |
| [virtual void LoadSubfile()](edit-file-function-load-subfile.html) | Loads subfile records. |
| [virtual void ProcessScreen()](edit-file-function-process-screen.html) | Processes screen input. |
| [abstract void ProcessSubfileRecord()](edit-file-function-process-subfile-record.html) | Processes a subfile record. Must be overridden. |
| [abstract void UpdateSubfileRecordDB()](edit-file-function-update-subfile-record-db.html) | Updates a subfile record to the database. Must be overridden. |
| [virtual void ConvertControlToExternal()](edit-file-function-convert-control-to-external.html) | Converts control fields to external form. |
| [virtual void EditFile()](edit-file-function-edit-file.html) | Main loop for the edit file screen. |
| [override void ProcessSubfile()](edit-file-function-process-subfile.html) | Processes modified subfile records. |
| [virtual void UpdateSubfileDB()](edit-file-function-update-subfile-db.html) | Updates all modified subfile records to the database. |
| [virtual void EstablishSubfileLimits()](edit-file-function-establish-subfile-limits.html) | Establishes subfile limits for writing. |
| [override void SetDisplayAttributes()](edit-file-function-set-display-attributes.html) | Sets display indicators based on ADD/CHG mode. |
| [override void SetDisplayControlAttributes()](edit-file-function-set-display-control-attributes.html) | Sets subfile control display indicators. |
| [void ToggleAddChangeMode()](edit-file-function-toggle-add-change-mode.html) | Switches between ADD and CHG modes and requests reload. |
| [override void ConvertMajorFieldsToExternalForm()](edit-file-function-convert-major-fields-to-external-form.html) | Delegates to ConvertControlToExternal. |
| [override decimal ResolvePromptRow()](edit-file-function-resolve-prompt-row.html) | Resolves the prompt row within the subfile. |

## See Also
- [SubfileProgram](subfile-program.html)
- [DisplayFileFunction](display-file-function.html)