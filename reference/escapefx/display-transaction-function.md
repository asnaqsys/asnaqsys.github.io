---
title: "DisplayTransactionFunction Class"
description: "Abstract base class for read-only transactional subfile display in ASNA.QSys.EscapeFX."
---

## Definition

**Namespace:** ASNA.QSys.EscapeFX  
**Assembly:** ASNA.QSys.EscapeFX.dll  
**Inherits:** [SubfileProgram](subfile-program.html)

Abstract base class for programs that display transactional data in a read-only subfile view.

## Constructors

| Signature | Description |
| --- | --- |
| `DisplayTransactionFunction()` | Initializes a new instance of the DisplayTransactionFunction class. |

## Properties

| Signature | Description |
| --- | --- |
| `FixedString<_1> FirstCycle { get; set; }` | Gets or sets the first-cycle flag (`"Y"` on initial display). |

## Methods

| Signature | Description |
| --- | --- |
| [abstract void InitScreen()](display-transaction-function-init-screen.html) | Initializes the screen and subfile data. Must be overridden. |
| [virtual void ConvertControlToExternal()](display-transaction-function-convert-control-to-external.html) | Converts control fields to external display form. |
| [virtual void ProcessHomeKey()](display-transaction-function-process-home-key.html) | Handles the HOME key by resetting the transaction state. |
| [virtual void DisplayTransaction()](display-transaction-function-display-transaction.html) | Main loop for displaying the transactional screen. |
| [override void ClearSubfile()](display-transaction-function-clear-subfile.html) | Clears subfile records and resets RRN counters. |
| [override void ConvertMajorFieldsToExternalForm()](display-transaction-function-convert-major-fields-to-external-form.html) | Delegates to ConvertControlToExternal. |

## See Also
- [SubfileProgram](subfile-program.html)
- [EditTransactionFunction](edit-transaction-function.html)