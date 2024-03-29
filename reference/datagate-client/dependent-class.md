---
title: Dependent Class

---

<span> **Dependent** </span> names a database object, its type, and characterizes its dependent relationship to another database object. 
```cs
public class DependentClass
```

## Thread Safety

Any public static (Shared) members of this type are safe for multithreaded operations. Any instance members are not guaranteed to be thread safe.
## Remarks

Instances of **Dependent** are returned by the **Dependents** property of [IAdgObject](iadg-object-class.html). These instances enumerate logical database objects that are defined in terms of a relationship to the base physical database object, represented by **IAdgObject** . Database providers may place constraints on database objects that have dependents, such as not allowing the object's deletion.

The [AdgObjectType](dependent-class-adg-object-type-property.html) property reveals the dependent object's type, defined by the [ AdgObjectTypes](adg-object-types-enumeration.html) enumeration. Current database providers only list database files and members as dependents. The [ PathName](dependent-class-path-name-property.html) property is the full path of the dependent object.

The [DependentType](dependent-class-dependent-type-property.html) property determines the relationship between this dependent and its base (see [ DependentTypes](dependent-types-enumeration.html) enumeration). 
## Requirements

**Namespace:** [ASNA.DataGate.Client](datagate-client-namespace.html) 

**Assembly:** ASNA DataGate Client

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
## See Also


[Dependent Class Members](dependent-members.html)
      <br />
[IAdgObject Class](iadg-object-class.html)
      <br />
[AdgObjectTypes Enumeration](adg-object-types-enumeration.html)
      <br />
[ASNA.DataGate.Client Namespace](datagate-client-namespace.html)

