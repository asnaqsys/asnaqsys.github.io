---
title: "IAdgObject interface.Unlock Method"
description: "Unlocks the ADG object with the specified share type."
---

## Definition

**Namespace:** ASNA.DataGate.Client  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Unlocks the ADG object with the specified share type.

<a id="void-unlock-sharetypes-sharetype"></a>
## void Unlock(ShareTypes ShareType)

Unlocks the ADG object with the specified share type.

#### Remarks
This method is used to remove a lock of the specified type from the ADG object. The ShareType parameter specifies the type of lock to remove, which can be read, write, or other types of locks. This can be useful for managing concurrent access to the object.

```cs
void Unlock(ShareTypes ShareType)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [ShareTypes](/reference/datagate/datagate-common/share-types.html) | ShareType | The type of lock to remove.

## See Also
- [IAdgObject interface class](i-adg-object.html)
