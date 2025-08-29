---
title: "AdgConnection.Clone Method"
description: "Creates a new AdgConnection that is a copy of the current instance."
---

## Definition

**Namespace:** ASNA.DataGate.Client<br/>
**Assembly:** ASNA.QSys.DataGate.Client.dll

### object Clone()

Creates a new AdgConnection that is a copy of the current instance.


#### Remarks

This method returns a copy of the **AdgConnection** object. If successful, the copy’s `SourceProfile` property will reference the same **SourceProfile** object contained in the **SourceProfile** property of the copied object.  If the copied object is in the Open <b>state</b>, the `Open` method is invoked on the copy, providing a new database connection.
 
Note that a database connection cannot be shared between two instances of **AdgConnection**.


```cs
object Clone()
```


## See Also

[AdgConnection Class](adg-connection.html)