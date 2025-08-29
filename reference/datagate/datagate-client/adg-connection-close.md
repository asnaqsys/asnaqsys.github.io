---
title: "AdgConnection.Close Method"
description: "Closes the connection to the database."
---

## Definition

**Namespace:** ASNA.DataGate.Client<br/>
**Assembly:** ASNA.QSys.DataGate.Client.dll

### void Close()

Closes the connection to the database.

#### Remarks
 
This method sets the **State** property of the** AdgConnection** object to Closed.  Additionally, if the current value of** State** is Open, the connection to the database provider is released, along with any unmanaged resources associated with that connection. 

 
Note that you must explicitly call either the **Close** or [Dispose](adg-connection-dispose.html) methods on **AdgConnection** 	objects in the	**Open** state before the objects are finalized, to release unmanaged resources associated with their database connections.  If unmanaged resources are not released prior to object finalization, unexpected results can occur, including program termination and loss of data.


```cs
void Close()
```


## See Also

[AdgConnection Class](adg-connection.html)