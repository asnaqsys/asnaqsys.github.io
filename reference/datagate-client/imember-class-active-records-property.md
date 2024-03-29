---
title: IMember.ActiveRecords Property

---

The number of active records in the database file member object represented by **IMember** 

```cs
 public long ActiveRecord { get; }
```


## Property Value

**Integer** . Read-only. A non-negative value.
## Exceptions



| Exception Type | Condition |
| ---- | ---- |
| dgException | The property values of this **IMember** are being accessed for the first time and the resulting query to the database provider caused an exception to occur. See table below. |



ASNA.DataGate.Common.dgException is thrown to signal normal procedural conditions, in addition to error conditions. The following table summarizes these conditions, and the corresponding value of the <span>dgException.Error</span> property.
<br />



| Value of dgException.Error | Condition |
| ---- | ---- |
| dgEINVARG | The path name referenced by this **IMember** instance does not locate a valid database object. |
| dgEmMNOTFND | The path name referenced by this **IMember** instance may locate a valid database object but the object is not a member. |
| dgExMISSING | The database provider's "exit point" security support discovered a registration for an exit point validation routine for the method but the validation routine itself was not found. |
| dgExINVLIC | The database provider's "exit point" security support encountered an exit point validation routine for the method but the license for this support is invalid or not found. |
| dgExDENIED | Access to the method was denied by the database provider's "exit point" security support. |



## Remarks

Use **ActiveRecords** to examine the number of active records contained in an existing member object. For a count of deleted records, use the [DeletedRecords](imember-class-deleted-records-property.html) property. 

The value of this read-only property is established only once in the lifetime of the **IMember** instance. Accesses of the property value after the first return a cached value which may not reflect intervening changes to the member object. To obtain a refreshed count, access the property value of a new instance of **IMember** . 
## Requirements

**Namespace:** [ASNA.DataGate.Client](datagate-client-namespace.html) 

**Assembly:** ASNA DataGate Client

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
## See Also


[IMember Class](imember-class.html)
      <br />
[DeletedRecords Property](imember-class-deleted-records-property.html)
      <br />
[ASNA.DataGate.Client Namespace](datagate-client-namespace.html)

