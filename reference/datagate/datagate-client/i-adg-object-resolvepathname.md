---
title: "IAdgObject interface.ResolvePathName Method"
description: "Resolves the path name of the ADG object."
---

## Definition

**Namespace:** ASNA.DataGate.Client  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Resolves the path name of the ADG object.

<a id="string-resolvepathname"></a>
## string ResolvePathName()

Resolves the path name of the ADG object.

#### Remarks
This method is used to resolve the path name of the ADG object. The path name is resolved according to the rules of the database where the object is stored. This can be useful for obtaining the absolute path of the object, especially if the object was specified with a relative path.

```cs
string ResolvePathName()
```

## See Also
- [IAdgObject interface class](i-adg-object.html)
