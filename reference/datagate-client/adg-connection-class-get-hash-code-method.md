---
title: AdgConnection.GetHashCode Metod

---

Invokes the <span> **GetHashCode** </span> method of the <span> **SourceProfile** </span> property.

```cs
 public override int GetHashCode();
```


## Exceptions

**NullReferenceException** . The value of the <span> **SourceProfile** </span> property is null. 
## Return Value

A 32-bit signed integer hash code, one, which represents Boolean **true** if the value of this instance is nonzero; otherwise, the integer zero, which represents Boolean **false** . 
## Remarks

This method returns a value identifying the contents of the object contained by the current <span> **SourceProfile** </span>. The value is not guaranteed to be unique to the <span> **SourceProfile** </span> instance. The value does not identify the current connection or the **AdgConnection** instance itself.

The DataGate client assembly uses this method internally for connection pooling and other functionality.
## Requirements

**Namespace:** [ASNA.DataGate.Client](datagate-client-namespace.html) 

**Assembly:** ASNA DataGate Client

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
## See Also


[AdgConnection Class](adg-connection-class.html)
      <br />
[AdgConnection Class Members](adg-connection-members.html)
      <br />
[ASNA.DataGate.Client Namespace](datagate-client-namespace.html)
      <br />

