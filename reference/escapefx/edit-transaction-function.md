---
title: "EditTransactionFunction Class"
description: "Abstract base class for editable transactional subfile programs in ASNA.QSys.EscapeFX."
---

## Definition

**Namespace:** ASNA.QSys.EscapeFX  
**Assembly:** ASNA.QSys.EscapeFX.dll  
**Inherits:** [SubfileProgram](subfile-program.html)

Abstract base class for programs that support adding and changing records via a transactional subfile.

## Constructors

| Signature | Description |
| --- | --- |
| `EditTransactionFunction()` | Initializes a new instance of the EditTransactionFunction class. |

## Properties

| Signature | Description |
| --- | --- |
| `FixedString<_1> RollBackMode { get; set; }` | Gets or sets the rollback mode flag. |
| `bool inF11Delete { get; set; }` | Gets or sets the F11 delete function key indicator. |

## Methods

| Signature | Description |
| --- | --- |
| [abstract void InitScreen()](edit-transaction-function-init-screen.html) | Initializes the screen for a new transaction. Must be overridden. |
| [virtual void InitSubfile()](edit-transaction-function-init-subfile.html) | Fills the remainder of the subfile page with blank records. |
| [virtual void ConvertControlToExternal()](edit-transaction-function-convert-control-to-external.html) | Converts control fields to external display form. |
| [virtual void ConvertControlToInternal()](edit-transaction-function-convert-control-to-internal.html) | Converts header fields to internal form. |
| [virtual void ProcessHomeKey()](edit-transaction-function-process-home-key.html) | Handles the HOME key by resetting the transaction. |
| [virtual void EditTransaction()](edit-transaction-function-edit-transaction.html) | Main loop for the editable transactional screen. |
| [void ToggleAddChangeMode()](edit-transaction-function-toggle-add-change-mode.html) | Switches between ADD and CHG modes. |
| [override void ClearSubfile()](edit-transaction-function-clear-subfile.html) | Clears subfile records and resets RRN counters. |
| [override void InitMainFileInfo(DatabaseFileBase)](edit-transaction-function-init-main-file-info.html) | Sets program mode to ADD or CHG based on file record count. |
| [override void ConvertMajorFieldsToExternalForm()](edit-transaction-function-convert-major-fields-to-external-form.html) | Delegates to ConvertControlToExternal. |

## See Also
- [SubfileProgram](subfile-program.html)
- [DisplayTransactionFunction](display-transaction-function.html)