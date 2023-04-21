---
title: ILibraryList.RemoveEntry Method

---

**RemoveEntry** removes a library list entry from a database in the library represented by [ILibraryList](ilibrary-list-class.html).

```cs
 public void RemoveEntry(
   string path );
```


## Parameters



 *path* 

: 

String. Specifies the path name of the database library to remove from the library list.



## Remarks

A library list entry can not be removed if it is on an active user's library list. 
## Requirements

<span> **Namespace:** [ASNA.DataGate.Client](datagate-client-namespace.html) </span> 

<span> **Assembly:** ASNA DataGate Client</span> 

<span> **Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro</span> 
## See 
Also


[ILibraryList Class](ilibrary-list-class.html)
      <br />
[ILibraryList Members](ilibrary-list-members.html)
      <br />
[ASNA.DataGate.Client Namespace](datagate-client-namespace.html)

