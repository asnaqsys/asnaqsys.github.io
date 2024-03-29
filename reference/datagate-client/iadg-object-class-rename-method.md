---
title: IAdgObject.Rename Method

---

The **Rename** method renames an object without changing its location in the database.

```cs
 public void IAdgObject Rename( string NewName );
```

## Parameters



 *NewName* 

: 
String. The new name for the [IAdgObject](iadg-object-class.html).



## Exceptions



| Exception Type | Condition |
| ---- | ---- |
| NullReferenceException | *NewName* is a null reference. |
| dgException | See table below. |



ASNA.DataGate.Common.dgException is thrown to signal normal procedural conditions, in addition to error conditions. The following table summarizes these conditions, and the corresponding value of the dgException.Error property.
<br />



| Value of dgException.Error | Condition |
| ---- | ---- |
| dgEINVARG | The path name specified when the **IAdgObject** instance was created does not reference an existing database object or the method is not available for this object type. |
| dgEsAS400ERROR | The database provider encountered a system-level error. Details provided in the **dgException.Message** property. |
| dgEmNOOBJAUTH | The user of the session does not have "operational" authority to the existing database object represented by **IAdgObject** . |
| dgEmNOPARENTUPD | The database object represented by **IAdgObject** is contained by a parent file or library object and "update" access is not permitted by the parent. |
| dgEmNOTONQTEMP | The database object represented by **IAdgObject** is the special library "/QTEMP" and the method is not permitted for QTEMP. |
| dgEmROOTDIR | The database object represented by **IAdgObject** is the special root library "/" and the method is not permitted for root. |
| dgEmBUSYOBJ | Some database providers attempt to obtain an exclusive lock on the database object represented by **IAdgObject** , and an exclusive-read lock on the object's parent. This exception indicates that one of these locks could not be obtained. |
| dgEmINVOBJNAME | *NewName* fails the database provider's syntax check for valid object names due to invalid or reserved characters. |



## Remarks

This method permits the renaming of an existing database object represented by **IAdgObject** . *NewName* must conform to the database provider's conventions for object names and the user of the session must have requisite authority to the object.

**Rename** only changes the base name of the object. To change the path name of the object, consider using [MoveTo](iadg-object-class-move-to_method.html), [Duplicate](iadg-object-class-duplicate-method.html), or another method capable of creating an equivalent object in a different location.
## Requirements

<span> **Namespace:** [ASNA.DataGate.Client](datagate-client-namespace.html) </span> 

<span> **Assembly:** ASNA DataGate Client</span> 

<span> **Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro</span> 
## See Also


[IAdgObject Class](iadg-object-class.html)
      <br />
[MoveTo Method](iadg-object-class-move-to_method.html)
      <br />
[Duplicate Method](iadg-object-class-duplicate-method.html)
      <br />
[ASNA.DataGate.Client Namespace](datagate-client-namespace.html)

