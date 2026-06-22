---
title: "InvariantCultureTypeConverter.GetHashCode Method"
description: "Serves as the default hash function, using the wrapped converter's GetHashCode method."
---

## Definition

**Namespace:** ASNA.DataGate.Common  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Serves as the default hash function, using the wrapped converter's GetHashCode method.

<a id="int-gethashcode"></a>
## int GetHashCode()

Serves as the default hash function, using the wrapped converter's GetHashCode method.

#### Remarks
This method overrides the base implementation to ensure that the hash code is generated using the wrapped converter's GetHashCode method.This is useful when you need to ensure that hash code generation is not affected by the current culture settings of the system.

```cs
int GetHashCode()
```

## See Also
- [InvariantCultureTypeConverter class](invariant-culture-type-converter.html)
