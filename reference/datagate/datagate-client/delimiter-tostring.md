---
title: "Delimiter.ToString Method"
description: "Returns a string that represents the current object."
---

## Definition

**Namespace:** ASNA.DataGate.Client.CopyData  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Returns a string that represents the current object.

<a id="string-tostring"></a>
## string ToString()

Returns a string that represents the current object.

#### Remarks
This method overrides the base  method and performs a check to determine the string representation:- If this instance represents no delimiter (None == this is true), it returns an empty string.- Otherwise, it creates a new string from the  property of this instance.

```cs
string ToString()
```

## See Also
- [Delimiter class](delimiter.html)
