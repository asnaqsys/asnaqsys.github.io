---
title: "IAdgObject interface.Lock Method"
description: "Locks the ADG object with the specified share type and wait option."
---

## Definition

**Namespace:** ASNA.DataGate.Client  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Locks the ADG object with the specified share type and wait option.

<a id="void-lock-sharetypes-sharetype-waitoptions-waitoption-short-waittime"></a>
## void Lock(ShareTypes ShareType, WaitOptions WaitOption, short WaitTime)

Locks the ADG object with the specified share type and wait option.

#### Remarks
This method is used to apply a lock of the specified type to the ADG object. The ShareType parameter specifies the type of lock to apply, which can be read, write, or other types of locks. The WaitOption parameter specifies what to do if the lock cannot be immediately acquired, such as waiting for the lock to become available or throwing an exception.

```cs
void Lock(ShareTypes ShareType, WaitOptions WaitOption, short WaitTime)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [ShareTypes](/reference/datagate/datagate-common/share-types.html) | ShareType | The type of lock to apply.
| [WaitOptions](/reference/datagate/datagate-common/wait-options.html) | WaitOption | The wait option to use if the lock cannot be immediately acquired.
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | WaitTime | The wait time to use if the lock cannot be immediately acquired.

## See Also
- [IAdgObject interface class](i-adg-object.html)
