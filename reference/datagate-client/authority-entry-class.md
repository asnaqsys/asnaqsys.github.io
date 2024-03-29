---
title: AuthorityEntry Class

---

The **AuthorityEntry** class describes a user or group authorization to a database object. For a list of all members, see [AuthorityEntry Members](authority-entry-members.html). 

[ASNA.DataGate.Client](datagate-client-namespace.html) <br /> **ASNA.DataGate.Client.AuthorityEntry** 

```cs
public class AuthorityEntry :
```

## Thread Safety

Any public static (Shared) members of this type are safe for multithreaded operations. Any instance members are not guaranteed to be thread safe.
## Remarks

<span style="FONT-WEIGHT: bold">AuthorityEntry</span> describes a user or group authorization to a database directory, member, or file. An instance of **AuthorityEntry** is usually one of a collection of authority descriptors for the database object, such as provided by the [AuthorityEntries](iadg-object-class-authority-entries-property.html) property of [IAdgObject](iadg-object-class.html).

[AuthorityEntry](authority-entry-class-authority-entry-constructors.html) constructors create a single authority descriptor. [ AuthorityType](authority-entry-class-authority-type-field.html) establishes the access capabilitities and limitations (add, change, exclude, management, etc.). [ UserName](authority-entry-class-username-field.html) establishes the user or group profile name associated with the access authority. [IsGroupAccount](authority-entry-class-username-field.html) indicates if the **Username** is a user or group profile.
## Requirements

**Namespace:** [ASNA.DataGate.Client](datagate-client-namespace.html) 

**Assembly:** ASNA DataGate Client

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
## See Also


[AuthorityEntry Class Members](authority-entry-members.html)
      <br />
[IAdgObject Class](iadg-object-class.html)
      <br />
      [IAdgObject.AuthorityEntries 
					Property](iadg-object-class-authority-entries-property.html)
      <br />
[ASNA.DataGate.Client Namespace](datagate-client-namespace.html)

