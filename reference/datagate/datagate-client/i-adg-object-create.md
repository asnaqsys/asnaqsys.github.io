---
title: "IAdgObject interface.Create Method"
description: "Creates the ADG object."
---

## Definition

**Namespace:** ASNA.DataGate.Client  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Creates the ADG object.

<a id="void-create"></a>
## void Create()

Creates the ADG object.

#### Remarks
This method is used to create the ADG object. It should be called after the properties of the object have been set, but before the object is used. This method may perform various initialization tasks, such as establishing a connection to the server or allocating resources.

```cs
void Create()
```

## See Also
- [IAdgObject interface class](i-adg-object.html)
