---
title: "EscapeProgram.CheckForCallError Method"
description: "Check for program call ending in error, issue message if so."
---

## Definition

**Namespace:** ASNA.QSys.EscapeFX  
**Assembly:** ASNA.QSys.EscapeFX.dll

Checks whether a program call ended in error, sets indicators, and sets the resulting code.

<a id="void-checkforcallerrorstringintarray"></a>

## void CheckForCallError(string, int[])

Check for program call ending in error, issue message if so.

```cs
void CheckForCallError(string, int[])
```

#### Parameters

| Type | Parameter name | Description |
| --- | --- | --- |
| string | calledProgramName | Parameter. |
| int[] | errorIndicators | Parameter. |

### Remarks
Checks whether a program call ended in error, sets indicators, and sets the resulting code.

## See Also
- [EscapeProgram class](escape-program.html)
