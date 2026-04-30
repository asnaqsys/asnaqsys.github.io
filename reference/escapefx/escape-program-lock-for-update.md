---
title: "EscapeProgram.LockForUpdate Method"
description: "Locks a database record for update."
---

## Definition

**Namespace:** ASNA.QSys.EscapeFX  
**Assembly:** ASNA.QSys.EscapeFX.dll

Locks a record for update by chaining to it using key parts.

## Overloads

| Signature | Description |
| --- | --- |
| [LockForUpdate](#bool-lockforupdatedatabasefilebasestringobjectarray)(DatabaseFileBase, string, object[]) | Locks using the file's default format. |
| [LockForUpdate](#bool-lockforupdatestringdatabasefilebasestringobjectarray)(string, DatabaseFileBase, string, object[]) | Locks using the specified format name. |


<a id="bool-lockforupdatedatabasefilebasestringobjectarray"></a>

## bool LockForUpdate(DatabaseFileBase, string, object[])

Locks using the file's default format.

```cs
bool LockForUpdate(DatabaseFileBase, string, object[])
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
LockForUpdate operation.

<a id="bool-lockforupdatestringdatabasefilebasestringobjectarray"></a>

## bool LockForUpdate(string, DatabaseFileBase, string, object[])

Locks using the specified format name.

```cs
bool LockForUpdate(string, DatabaseFileBase, string, object[])
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
LockForUpdate operation.

## See Also
- [EscapeProgram class](escape-program.html)
