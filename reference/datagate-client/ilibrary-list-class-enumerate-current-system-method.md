---
title: ILibraryList.EnumerateCurrentSystem Method

---

**EnumerateCurrentSystem** enumerates the object contents of the system and user portion of the library list represented by **ILibraryList** , with the supplied [AdgEnumerator](adg-enumerator-delegate.html) delegate.

```cs
 public void EnumerateCurrentSystem( AdgEnumerator enumerator  );
```


## Parameters



 *enumerator* 

: 

[AdgEnumerator](adg-enumerator-delegate.html). The delegate **EnumerateCurrentSystem** calls once for database object in the system and user portion of the library list represented by **ILibraryList** .



## Exceptions


          <col span="1" style="FONT-WEIGHT: bold; WIDTH: 30%" />
          <col span="1" style="WIDTH: 70%" />

| Exception Type | Condition |
| ---- | ---- |
| dgException | See table below. |



ASNA.DataGate.Common.dgException is thrown to signal normal procedural conditions, in addition to error conditions. The following table summarizes these conditions, and the corresponding value of the dgException.Error property.

 <col span="1" style="FONT-WEIGHT: bold; WIDTH: 30%" /> <col span="1" style="WIDTH: 70%" />

| Value of dgException.Error | Condition |
| ---- | ---- |
| <p>dgEmNODIRREAD | The database provider's security model does not permit the current session to access lists of library contents. |
| dgEINVARG | The path name given for this ILibraryList object does not correspond to a database library. |
| dgExMISSING | The database provider's "exit point" security support discovered a registration for an exit point validation routine for the method, but the validation routine itself was not found. |
| dgExINVLIC | The database provider's "exit point" security support encountered an exit point validation routine for the method, but the license for this support is invalid or not found. |
| dgExDENIED | Access to the method was denied by the database provider's "exit point" security support. |
| dgEINTERNAL | A database provider internal error occurred. Review the provider's event logs for more information. |
| dgENOMEM | The database provider encountered an "out of memory" exception. |
| dgECHANBUSY | The delegate *enumerator* has attempted to call a restricted method or access a restricted property. See AdgEnumerator for details on what DG methods the delegate may invoke.. |



## Remarks

**EnumerateCurrentSystem** provides a call-back interface for enumerating the database object contents of the system and user portion of an existing library list. This is useful in visual applications, for example, when a library contains a large amount of objects and a separate thread is used to display a view of objects as they are supplied by the database provider. The delegate *enumerator* is called by **EnumerateCurrentSystem** as each object is returned by the provider. Each object in the library list is rendered to the delegate as an instance of [IAdgObject](iadg-object-class.html) through which the program can immediately obtain static details, such as path name and object type. Not all methods of **IAdgObject** are available from the delegate's code however (see **AdgEnumerator** for details).

DG and current database providers only support the enumeration of files and libraries as the contents of libraries. Exceptions raised by the delegate cause **Enumeration** to halt the database provider's stream of objects (safely interrupting the operation) just prior to rethrowing the exception.

Note that the [IDirectory.ItemList](idirectory-class-item-list-property.html) property provides similar information, but "all at once" in a cached list format for a specific directory.
## Requirements

<span> **Namespace:** [ASNA.DataGate.Client](datagate-client-namespace.html) </span> 

<span> **Assembly:** ASNA DataGate Client</span> 

<span> **Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro</span> 
## See Also

[ILibraryList Class](ilibrary-list-class.html) <br /> [ ILibraryList Members](ilibrary-list-members.html) <br /> [ EnumerateCurrentUser Method](ilibrary-list-class-enumerate-current-user-method.html) <br /> [AdgEnumerator Delegate](adg-enumerator-delegate.html) <br /> [IAdgObject Class](iadg-object-class.html) <br /> [ IDirectory.ItemList Property](idirectory-class-item-list-property.html) <br /> [ASNA.DataGate.Client Namespace](datagate-client-namespace.html) 
