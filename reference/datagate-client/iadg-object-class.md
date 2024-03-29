---
title: IAdgObject Class

---

**IAdgObject** is the base interface implemented by all DataGate class objects modeling database objects. The leaf interfaces of these classes are [IDirectory](idirectory-class.html), [IFileObject](ifile-object-class.html), and [ IMember](imember-class.html). Each of these inherits the methods and properties of **IAdgObject** , so that an instance of **IDirectory** , **IFileObject** , or **IMember** is also an instance of **IAdgObject** .

Note that methods which iterate **IAdgObject** instances (such as [ IDirectory.Enumerate](idirectory-class-enumerate-method.html)), are actually returning references to objects that implement **IDirectory** , **IFileObject** , or **IMember** . The underlying type of an **IAdgObject** instance can be determined with the [ AdgObjectType](iadg-object-class-adg-object-type-property.html) property. 

For a list of all members of this type, see [IAdgObject Members](iadg-object-members.html).

[ASNA.DataGate.Client](datagate-client-namespace.html) 

ASNA.DataGate.Client.IAdgObject
<pre>&lt;Serializable&gt; **Public interface IAdgObject** </pre>

## Thread Safety

Implementations of **IAdgObject** are safe for multithreaded operations.
## Remarks

When a DG method or property returns an instance of **IAdgObject** , the instance returned is also an instance of **IDirectory** , **IFileObject** , or **IMember** . The programmer may operate on the instance through the methods of **IAdgObject** , or may use the methods of the underlying implementation, by assigning the returned instance to the proper object variable. The [AdgObjectType](iadg-object-class-adg-object-type-property.html) property of **IAdgObject** is used to determine if the underlying implementation is **IDirectory** , **IFileObject** , or **IMember** .

The properties and methods provided by **IAdgObject** represent database object management functionality common to all database objects, such as names, locations, security, allocation, and definition. Included are methods for creating, renaming, moving, duplicating, and deleting database objects. Basically, **IAdgObject** and its inheritors are useful for performing the following tasks:

1. *Accessing* 
				the metadata of existing database objects.
2. *Modifying* 
				certain operational attributes of existing database objects.
3. *Defining*  and *creating*  new database objects.

**IAdgObject** instances are created either directly, via the methods of [AdgFactory](adg-factory-class.html) ([NewFile](adg-factory-class-new-file-method.html), [NewDirectory](adg-factory-class-new-directory-method.html), [ NewMember](adg-factory-class-new-member-method.html), [ReadXml](adg-factory-class-read-xml-methods.html)) or from the methods of other **IAdgObject** instances representing database "container" objects ( **IDirectory.Enumerate** , [ IFileObject.Members](ifile-object-class-members-property.html)).

Generally, property values representing the metadata of an existing database object are provided on-demand and are cached. That is, DG will query the database provider for the value of the property only once in the lifetime of the **IAdgObject** instance, and return the same value each time the property value is read. New or changed metadata can be accessed by obtaining a new instance of **IAdgObject** .
## Requirements

**Namespace:** [ASNA.DataGate.Client](datagate-client-namespace.html) 

**Assembly:** ASNA DataGate Client

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
## See Also


[IAdgObject Members](iadg-object-members.html)
      <br />
[AdgObjectType Property](iadg-object-class-adg-object-type-property.html)
      <br />
[IDirectory Class](idirectory-class.html)
      <br />
[Enumerate Method ](idirectory-class-enumerate-method.html)
      <br />
[IFileObject Class](ifile-object-class.html)
      <br />
[Members Property](ifile-object-class-members-property.html)
      <br />
[IMember Class](imember-class.html)
      <br />
[AdgFactory Class](adg-factory-class.html)
      <br />
[NewFile Method](adg-factory-class-new-file-method.html)
      <br />
[NewDirectory Method](adg-factory-class-new-directory-method.html)
      <br />
[NewMember Method](adg-factory-class-new-member-method.html) 
				<br />[ReadXml Method](adg-factory-class-read-xml-methods.html)<br />
[ASNA DataGate Client Namespace](datagate-client-namespace.html)

