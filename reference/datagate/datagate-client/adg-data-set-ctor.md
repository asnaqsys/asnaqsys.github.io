---
title: "AdgDataSet Constructor"
description: "Initializes a new instance of the AdgDataSet class."
---

## Definition

**Namespace:** ASNA.DataGate.Client  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Initializes a new instance of the class with the specified name.

```cs
AdgDataSet(string name)
```

#### Parameters

| Type | Parameter name | Description |
| --- | --- | --- |
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | name | The name to give the new AdgDataSet. |

## Remarks

The constructor of **AdgDataSet** should not be called directly, since the class is abstract. Rather it must be called by a class that inherits and implements the abstract methods of the class.

Most applications should create **AdgDataSet** instances via the [FileAdapter.OpenNewAdgDataSet](file-adapter-opennewadgdataset.html) method. The **AdgDataSet** object returned by this method is properly initialized for accessing a particular file. 


## See Also
- [AdgDataSet class](adg-data-set.html)
