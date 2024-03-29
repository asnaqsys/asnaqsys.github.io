---
title: AdgConnection.Close Method

---

Sets the [ State](adg-connection-class-state-property.html) property to <span>Closed</span>, and releases connections to the database provider.

```cs
 public void Close();
```


## Exceptions

None.
## Remarks

This method sets the **State** property of the **AdgConnection** object to Closed. Additionally, if the current value of **State** is Open, the connection to the database provider is released, along with any unmanaged resources associated with that connection. 

Note that you must explicitly call either the <span> **Close** </span> or [Dispose](adg-connection-class-dispose-method.html) methods on <span> **AdgConnection** </span> objects in the **Open** state before the objects are finalized, to release unmanaged resources associated with their database connections. If unmanaged resources are not released prior to object finalization, unexpected results can occur, including program termination and loss of data.
## Examples


```cs 
  //Disconnects from the dataBase by closing the connection.
  adg.Close();
```

## Requirements

<span> **Namespace:** [ASNA.DataGate.Client](datagate-client-namespace.html) </span> 

<span> **Assembly:** ASNA DataGate Client</span> 

<span> **Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro</span> 
## See Also


      <span>
[AdgConnection Class](adg-connection-class.html)
        <br />
[AdgConnection Class Members](adg-connection-members.html)
        <br />
[State Property](adg-connection-class-state-property.html)
        <br />
[Dispose Method](adg-connection-class-dispose-method.html)
        <br />
[ASNA.DataGate.Client Namespace](datagate-client-namespace.html)
        <br />
      </span>

