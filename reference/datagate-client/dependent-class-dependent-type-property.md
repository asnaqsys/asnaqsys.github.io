---
title: Dependent.DependentType Property

---

**DependentType** determines the relationship between a dependent database object and its' [ bases](iadg-object-class-bases-property.html). 

```cs
 public DependentTypes DependentType { get; }
```


## Property Value

[DependentTypes](dependent-types-enumeration.html). Read-only. The relationship between a dependent and its [ bases](iadg-object-class-bases-property.html). 
## Remarks

The value of **DependentType** determines what type of dependency is represented by the **Dependent** instance. See **DependentTypes** for details of the possible values of this property.
## Requirements

**Namespace:** [ASNA.DataGate.Common](datagate-common-namespace.html) 

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10

**Assembly:** ASNA DataGate Client (in ASNA.DataGate.Client.dll)
## See Also


[ASNA.DataGate.Common Namespace](datagate-common-namespace.html)
      <br />
[Dependent Class](dependent-class.html)
      <br />
[DependentTypes Enumeration](dependent-types-enumeration.html)
      <br />
[IAdgObject.Bases Property](iadg-object-class-bases-property.html)

