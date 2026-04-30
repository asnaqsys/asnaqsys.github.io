---
title: "EscapeProgram.HasRecordChanged Method"
description: "Checks whether a database record has changed since it was last read."
---

## Definition

**Namespace:** ASNA.QSys.EscapeFX  
**Assembly:** ASNA.QSys.EscapeFX.dll

Checks whether a record has changed since it was last read by comparing original and current values.

<a id="bool-hasrecordchangeddatabasefilebasestringstring"></a>

## bool HasRecordChanged(DatabaseFileBase, string, string)

HasRecordChanged operation.

```cs
bool HasRecordChanged(DatabaseFileBase, string, string)
```

#### Parameters

| Type | Parameter name | Description |
| --- | --- | --- |
| DatabaseFileBase | file | Parameter. |
| string | originalRecord | Parameter. |
| string | currentRecord | Parameter. |

#### Returns

| Type | Description |
| --- | --- |
| bool | Returns a bool value. |

### Remarks
Checks whether a record has changed since it was last read by comparing original and current values.

## See Also
- [EscapeProgram class](escape-program.html)
