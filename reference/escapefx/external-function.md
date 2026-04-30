---
title: "ExternalFunction Class"
description: "Base class for generic programs with no predefined I/O style in ASNA.QSys.EscapeFX."
---

## Definition

**Namespace:** ASNA.QSys.EscapeFX  
**Assembly:** ASNA.QSys.EscapeFX.dll  
**Inherits:** [EscapeProgram](escape-program.html)

Concrete base class for generic application programs that do not require a predefined I/O style such as interactive screens or printed reports. Provides a minimal extension of `EscapeProgram` for custom logic.

## Constructors

| Signature | Description |
| --- | --- |
| `ExternalFunction()` | Initializes a new instance of the ExternalFunction class. |

## Methods

| Signature | Description |
| --- | --- |
| [override void CancelProgram()](external-function-cancel-program.html) | Exits the program directly without clearing the resulting code. |

## See Also
- [EscapeProgram](escape-program.html)