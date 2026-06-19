---
title: "IAdgObject interface.HasLock Method"
description: "Determines whether the ADG object has a lock of the specified type."
---

## Definition

**Namespace:** ASNA.DataGate.Client  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Determines whether the ADG object has a lock of the specified type.

<a id="bool-haslock-sharetypes-sharetype"></a>
## bool HasLock(ShareTypes ShareType)

Determines whether the ADG object has a lock of the specified type.

#### Remarks
This method is used to check if the ADG object has a lock of the specified type. The ShareType parameter specifies the type of lock to check for, which can be read, write, or other types of locks. This can be useful for managing concurrent access to the object.

```cs
bool HasLock(ShareTypes ShareType)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [ShareTypes](/reference/datagate/datagate-common/share-types.html) | ShareType | The type of lock to check for.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | True if the object has a lock of the specified type, false otherwise.

## See Also
- [IAdgObject interface class](i-adg-object.html)
