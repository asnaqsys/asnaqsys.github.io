---
title: "Dependent.GetHashCode Method"
description: "Serves as the default hash function."
---

## Definition

**Namespace:** ASNA.DataGate.Client  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Serves as the default hash function.

<a id="int-gethashcode"></a>
## int GetHashCode()

Serves as the default hash function.

#### Remarks
This method overrides the  method.It calculates the hash code for the current instance based on the , , and  properties.The hash code for  is calculated using a case-insensitive method.This hash code will be used when the  instance is used in a hash-based collection, like a hash set or a dictionary.

```cs
int GetHashCode()
```

## See Also
- [Dependent class](dependent.html)
