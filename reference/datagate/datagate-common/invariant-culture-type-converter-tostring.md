---
title: "InvariantCultureTypeConverter.ToString Method"
description: "Returns a string that represents the current object, using the wrapped converter's ToString method."
---

## Definition

**Namespace:** ASNA.DataGate.Common  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Returns a string that represents the current object, using the wrapped converter's ToString method.

<a id="string-tostring"></a>
## string ToString()

Returns a string that represents the current object, using the wrapped converter's ToString method.

#### Remarks
This method overrides the base implementation to ensure that the string representation is generated using the wrapped converter's ToString method.This is useful when you need to ensure that the string representation of the object is not affected by the current culture settings of the system.

```cs
string ToString()
```

## See Also
- [InvariantCultureTypeConverter class](invariant-culture-type-converter.html)
