---
title: "IDirectory interface.Enumerate Method"
description: "Enumerates the items in the directory using the specified enumerator."
---

## Definition

**Namespace:** ASNA.DataGate.Client  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Enumerates the items in the directory using the specified enumerator.

## Overloads

| Signature | Description |
| --- | --- |
| [Enumerate](#void-enumerate-adgenumerator-enumerator)(void Enumerate(AdgEnumerator enumerator)) | Enumerates the items in the directory using the specified enumerator. |
| [Enumerate](#void-enumerate-adgenumerator-enumerator-filetypes-ftype-bool-sysobjs)(void Enumerate(AdgEnumerator enumerator, FileTypes fType, bool sysObjs)) | Enumerates the items in the directory using the specified enumerator and file types. |

<a id="void-enumerate-adgenumerator-enumerator"></a>
## void Enumerate(AdgEnumerator enumerator)

Enumerates the items in the directory using the specified enumerator.

```cs
void Enumerate(AdgEnumerator enumerator)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [AdgEnumerator](/reference/datagate/datagate-client/adg-enumerator.html) | enumerator | The enumerator to use.

<a id="void-enumerate-adgenumerator-enumerator-filetypes-ftype-bool-sysobjs"></a>
## void Enumerate(AdgEnumerator enumerator, FileTypes fType, bool sysObjs)

Enumerates the items in the directory using the specified enumerator and file types.

```cs
void Enumerate(AdgEnumerator enumerator, FileTypes fType, bool sysObjs)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [AdgEnumerator](/reference/datagate/datagate-client/adg-enumerator.html) | enumerator | The enumerator to use.
| [FileTypes](/reference/datagate/datagate-common/file-types.html) | fType | The file types to enumerate.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | sysObjs | Whether to include system objects in the enumeration.

## See Also
- [IDirectory interface class](i-directory.html)
