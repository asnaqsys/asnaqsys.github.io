---
title: "AdgDataSet.InitializeFormats Method"
description: "Initializes the format strings of the AdgDataSet instance."
---

## Definition

**Namespace:** ASNA.DataGate.Client  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Initializes the format strings of the AdgDataSet instance.

```cs
abstract void InitializeFormats()
```

## Remarks
Intended to be overridden in derived classes to parse and set format strings for each DataTable in the AdgDataSet. Called in constructors and deserialization methods.


## See Also
- [AdgDataSet class](adg-data-set.html)
