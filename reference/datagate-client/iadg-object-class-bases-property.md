---
title: IAdgObject.Bases Property

---

**Bases** is a single-dimension array of strings containing path names denoting the set of objects upon which the database object represented by **IAdgObject** is based.

```cs
 public string[] Bases { get; set; }
```

## Property Value

**String** array. The **Length** of the array is equal to the number of base objects and may be no greater than **ASNA.DataGate.Common.MaxBaseFiles** . 
## Exceptions



| ExceptionType | Condition |
| ---- | ---- |
| dgException | See table below. |



ASNA.DataGate.Common.dgException is thrown to signal normal procedural conditions, in addition to error conditions. The following table summarizes these conditions, and the corresponding value of the <span>dgException.Error</span> property.
<br />



| Value of dgException.Error | Condition |
| ---- | ---- |
| dgEINVARG | Reading the value of **Bases** caused a database query for base path names but the path name of the database object represented by **IAdgObject** (specified when **IAdgObject** was created) does not name a valid database object or names an object type that cannot have base objects. |
| dgEmNOOBJAUTH | Reading the value of **Bases** caused a database query for base path names but the current session does not have "operational" authority to the object represented by **IAdgObject.** |
| dgEmBUSYOBJ | Reading the value of **Bases** caused a database query for base path names but the database provider could not obtain a shared-read lock for the object represented by **IAdgObject** in the current session. |
| dgEsAS400ERROR | The database provider encountered a system-level error. Details provided in the **dgException.Message** property. |



## Remarks

Logical files and members have one or more base objects upon which their definitions are based. **Bases** names these base objects by their absolute path names. The value of **Bases** for **IAdgObject** instances representing libraries, physical files, and physical members is an empty array.

When **IAdgObject** represents an existing database object, reading the value of **Bases** results in a query to the database provider to fetch the base paths, if **Bases** has not been set previously or has been set to a null reference.

When **IAdgObject** represents a database object to be created with the [Create](iadg-object-class-create-method.html) method, **Bases** must be set to the paths of the base objects prior to calling **Create** . When creating a logical file, **Bases** must name physical files with format identifiers matching the base format identifiers of the file definition or an exception will occur in **Create** . The **Length** of the string array must be no greater than **ASNA.DataGate.Common.MaxBaseFiles** .
## Requirements

**Namespace:** [ASNA.DataGate.Client](datagate-client-namespace.html) 

**Assembly:** ASNA DataGate Client

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
## See Also


[IAdgObject Class](iadg-object-class.html)
      <br />
[Create Method](iadg-object-class-create-method.html)
      <br />
[ASNA.DataGate.Client Namespace](datagate-client-namespace.html)

