---
title: SourceProfile.GetHashCode Method

---

Invokes the <span>GetHashCode</span> method of the <span>SourceProfile</span> property.

```cs
 public override int GetHashCode();
```


## Return Value

A 32-bit signed integer value, obtained from a hash algorithm using the values of the public properties of the SourceProfile object as input. Such a value can be used as a unique identifier for the set of entities described by a SourceProfile object. 
## Exceptions

**NullReferenceException** . The value of the <span>SourceProfile</span> property is null. 
## Remarks

This method returns a value identifying the contents of the object contained by the current SourceProfile. The value is not guaranteed to be unique to the SourceProfile instance. The value does not identify the current connection or the SourceProfile instance itself.

The DataGate client assembly uses this method internally for connection pooling and other functionality.
## Requirements

**Namespace:** [ ASNA.DataGate.Providers](datagate-providers-namespace.html) 

<span> **Assembly:** ASNA DataGate Client</span> 

<span> **Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10</span> 
## See Also


[SourceProfile Class](source-profile-class.html)
      <br />
[SourceProfile Class Members](source-profile-members.html)
      <br />
[SourceProfile Class Constructors](source-profile-constructors-main.html)
      <br />
[ASNA.DataGate.Providers Namespace](datagate-providers-namespace.html)

