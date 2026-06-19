---
title: "IAdgObject interface.MoveTo Method"
description: "Moves the ADG object to a new path."
---

## Definition

**Namespace:** ASNA.DataGate.Client  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Moves the ADG object to a new path.

<a id="void-moveto-string-newpathname"></a>
## void MoveTo(string NewPathName)

Moves the ADG object to a new path.

#### Remarks
This method is used to move the ADG object to a new path. The NewPathName parameter specifies the new path for the object. This can be useful for organizing objects or for changing the location of an object without changing its contents.

```cs
void MoveTo(string NewPathName)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | NewPathName | The new path for the object.

## See Also
- [IAdgObject interface class](i-adg-object.html)
