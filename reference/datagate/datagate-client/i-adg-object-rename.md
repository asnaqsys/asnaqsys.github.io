---
title: "IAdgObject interface.Rename Method"
description: "Renames the ADG object."
---

## Definition

**Namespace:** ASNA.DataGate.Client  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Renames the ADG object.

<a id="void-rename-string-newname"></a>
## void Rename(string NewName)

Renames the ADG object.

#### Remarks
This method is used to rename the ADG object. The NewName parameter specifies the new name for the object. This can be useful for changing the name of an object without changing its contents or location.

```cs
void Rename(string NewName)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | NewName | The new name for the object.

## See Also
- [IAdgObject interface class](i-adg-object.html)
