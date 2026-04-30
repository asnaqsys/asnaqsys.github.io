---
title: "EscapeProgram.LockForDelete Method"
description: "LockForDelete operation."
---

## Definition

**Namespace:** ASNA.QSys.EscapeFX  
**Assembly:** ASNA.QSys.EscapeFX.dll

LockForDelete operation.

## Overloads

| Signature | Description |
| --- | --- |
| [LockForDelete](#bool-lockfordeletedatabasefilebasestringobjectarray)(DatabaseFileBase, string, object[]) | LockForDelete operation. |
| [LockForDelete](#bool-lockfordeletestringdatabasefilebasestringobjectarray)(string, DatabaseFileBase, string, object[]) | LockForDelete operation. |

<a id="bool-lockfordeletedatabasefilebasestringobjectarray"></a>

## bool LockForDelete(DatabaseFileBase, string, object[])

LockForDelete operation.

```cs
bool LockForDelete(DatabaseFileBase, string, object[])
```

#### Parameters

| Type | Parameter name | Description |
| --- | --- | --- |
| DatabaseFileBase | file | Parameter. |
| string | label | Parameter. |
| object[] | keyParts | Parameter. |

#### Returns

| Type | Description |
| --- | --- |
| bool | Returns a bool value. |

### Remarks
LockForDelete operation.

<a id="bool-lockfordeletestringdatabasefilebasestringobjectarray"></a>

## bool LockForDelete(string, DatabaseFileBase, string, object[])

LockForDelete operation.

```cs
bool LockForDelete(string, DatabaseFileBase, string, object[])
```

#### Parameters

| Type | Parameter name | Description |
| --- | --- | --- |
| string | formatName | Parameter. |
| DatabaseFileBase | file | Parameter. |
| string | label | Parameter. |
| object[] | keyParts | Parameter. |

#### Returns

| Type | Description |
| --- | --- |
| bool | Returns a bool value. |

### Remarks
LockForDelete operation.

## See Also
- [EscapeProgram class](escape-program.html)
