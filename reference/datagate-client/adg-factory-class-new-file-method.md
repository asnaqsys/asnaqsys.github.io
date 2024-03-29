---
title: AdgFactory.NewFile Method

---

The **NewFile** method creates a new instance of [IFileObject](ifile-object-class.html) representing a database file for object management functions.

```cs
 public IFileObject NewFile(
AdgConnection cn
   string PathName
);
```


## Parameters


        <dt />


*cn* 
<dl>
: 

An instance of the [AdgConnection](adg-connection-class.html) representing a database connection to the server.

        <dt />
</dl>

*PathName* 
<dl>
: 

String. The path name of a new or exiting database file object.

</dl>

## Returns

An instance of an [IFileObject](ifile-object-class.html) object.
## Exceptions



| Exception Type | Condition |
| ---- | ---- |
| NullReferenceException | The *cn* and/or *PathName* parameters are null references. |
| dgException | See table below. |



ASNA.DataGate.Common.dgException is thrown to signal normal procedural conditions, in addition to error conditions. The following table summarizes these conditions, and the corresponding value of the <span>dgException.Error</span> property.


| Value of dgException.Error | Condition |
| ---- | ---- |
| dgEmINVSQLOP | The **AdgConnection** specified is a connection to an SQL Server database provider, and DG currently does not support the **IDirectory** interface for those providers. |



## Remarks

This method creates a new [IFileObject](ifile-object-class.html) based upon a new or existing database file (whose path is specified by *PathName* ). The database containing the file is specified as *cn* , an [ AdgConnection](adg-connection-class-state-property.html) object. Note that this method does not throw an exception if *PathName* and *cn* do not reference a valid, pre-existing database file. Subseqent usage of the returned **IFileObject** object's methods may raise such exceptions, however. 

To create a new database file, first call **NewFile** with the desired name for the new file in *PathName* . Next, use properties and methods of the **IFileObject** reference returned to set the new file's attributes (minimally, the [ IFileObject.ReadDefinition](ifile-object-class-read-definition-method.html) and [ IFileObject.ReadCreationAttributes](ifile-object-class-read-creation-attributes-method.html) methods must be called). Finally, call the [Create](iadg-object-class-create-method.html) method. A database file may also be created via [ AdgFactory.ReadXml](adg-factory-class-read-xml-methods.html).

<p class="normal">If the [State](adg-connection-class-state-property.html) property of the *cn* parameter is not **ConnectionState.Open** , **NewFile** may temporarily open the database provider connection, via [AdgConnection.Open](adg-connection-class-open-method.html). In this case only, upon successful return from **NewFile** , the **State** property of *cn* will be **ConnectionState.Closed** .
## Requirements

<span> **Namespace:** [ASNA.DataGate.Client](datagate-client-namespace.html) </span> 

<span> **Assembly:** ASNA DataGate Client</span> 

<span> **Platforms:** , Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8</span> Pro
## See 
Also


[AdgFactory Class](adg-factory-class.html)
      <br />
[ReadXml Methods](adg-factory-class-read-xml-methods.html)
      <br />
[IFileObject Class](ifile-object-class.html)
      <br />
[ReadDefinition Method](ifile-object-class-read-definition-method.html)
      <br />
      [ReadCreationAttributes 
					Method](ifile-object-class-read-creation-attributes-method.html)
      <br />
[IAdgObject Class](iadg-object-class.html)
      <br />
[Create Method](iadg-object-class-create-method.html)
      <br />
[AdgConnection Class](adg-connection-class.html)
      <br />
[State Property](adg-connection-class-state-property.html)
      <br />
[Open Method](adg-connection-class-open-method.html)
      <br />
[ASNA.DataGate.Client Namespace](datagate-client-namespace.html)

