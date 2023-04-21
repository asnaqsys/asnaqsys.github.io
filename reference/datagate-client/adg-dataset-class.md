---
title: AdgDataSet Class

---

A DataGate-compatible DataSet class for record-oriented database access.

For a list of all members of this type, see [AdgDataSet Members](adg-dataset-members.html).

[ASNA.DataGate.Client](datagate-client-namespace.html) <br /> **ASNA.DataGate.Client.<span>AdgDataSet</span>** 

```
public abstract class AdgDataSet : System.Data.DataSet 
```
## Thread Safety

Any public static (Shared) members of this type are safe for multithreaded operations. Any instance members are not guaranteed to be thread safe.
## Remarks

<span> **AdgDataSet** </span> is a subclass of the class. <span>System.Data.DataSet</span> is used widely throughout the .NET Framework. When used in tandem with [FileAdapter](file-adapter-class.html) **AdgDataSet** features methods to facilitate record-oriented access, while maintaining all of the integration and set-oriented features of System.Data.DataSet. 

**AdgDataSet** objects are specialized instances of System.Data. DataSet, distinguished by the composition of the data tables they contain. The **Tables** property of System.Data.DataSet is a collection of objects. In **AdgDataSet** objects, the tables referred to by the Tables property represent the formats of a DataGate file. Each table in a System.Data.DataSet contains a **Rows** collection of objects. System.Data.DataRow objects are used to model records in DG. Records are composed of fields, and in System.Data.DataRow, field data is accessed with its **Item** and **ItemArray** properties. Some field meta-data, or type information, is available from the **Columns** property of System.Data.DataTable.

Generally, applications need not access the System.Data.DataTable objects in **AdgDataSet** via the Tables property, etc. Rather, **AdgDataSet** provides several methods and properties for accessing particular rows of a table, such as [ActiveRow](adg-dataset-class-active-row-property.html) property and [PrepareRow](adg-dataset-class-prepare-row-method-main.html), [AddPreparedRowAndSetActive](adg-dataset-class-add-prepared-row-and-set-active-method.html), [AddRow](adg-dataset-class-add-row-methods.html), [InsertRow](adg-dataset-class-insert-row-methods.html), [SetActive](adg-dataset-class-set-active-methods.html), and [DeleteRow](adg-dataset-class-delete-row-method.html) methods. 

Other methods and properties, such as [Formats](adg-dataset-class-formats-property.html), [FormatIDs](adg-dataset-class-formatids-property.html), [GetFormatIndex](adg-dataset-class-get-format-index-method.html), [GetFormatName](adg-dataset-class-get-format-name-method.html), [CurrentFormatIndex](adg-dataset-class-get-format-index-method.html), and [CurrentFormatName](adg-dataset-class-current-format-name-property.html), provide information about the formats of the file modeled by **AdgDataSet** . When a format modeled by **AdgDataSet** contains a key, [NewKeyTable](adg-dataset-class-new-key-table-methods.html) provides a method to construct a key buffer for keyed access methods.

**AdgDataSet** is an "abstract" base class, not intended for direct instantiation (<span>MustInherit in VB). **AdgDataSet** instances are returned by [FileAdapter.OpenNewAdgDataSet](file-adapter-class-open-new-adg-dataset-method.html) or by instantiating another class that inherits **AdgDataSet.** For most applications, it is sufficient to use **<code>OpenNewAdgDataSet</code>** to create the **AdgDataSet** instance, since this method creates table structures in the **AdgDataSet** to match the formats of the file to be accessed.</span>

It is generally not recommended to compose your own class to inherit **AdgDataSet** . Such a class could be directly instantiated, however. Alternately, an **AdgDataSet** sub-class created with a DG-aware development tool, such as Visual RPG, can be directly instantiated for use with access functions like [FileAdapter.Open](file-adapter-class-open-method.html).
## Requirements

**Namespace:** [ASNA.DataGate.Client](datagate-client-namespace.html) 

**Assembly:** ASNA DataGate Client

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
## See Also


[AdgDataSet Members](adg-dataset-members.html)
							  <br />
[FileAdapter.OpenNewAdgDataSet](file-adapter-class-open-new-adg-dataset-method.html)
							  <br />
[AdgKeyTable Class](adg-key-table-class.html)
							  <br />
[ASNA DataGate Client Namespace](datagate-client-namespace.html)
							  <br /><br />
							  <br />

