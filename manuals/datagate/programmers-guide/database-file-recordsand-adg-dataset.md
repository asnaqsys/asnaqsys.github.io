---
title: "Managing Database File Records and ADG Dataset"
description: "Learn how to manage and manipulate database file records and ADG datasets effectively. This guide covers techniques, tips, and best practices."
---

.NET provides the ( **DataSet** ) class as a general-purpose container for relational database data. **DataSet** objects offer many useful functions and are used throughout the framework and in data-centric components for access, update, and display. For example, **DataSet** objects can be bound to certain Windows forms controls at design-time. DG builds on this foundation by sub-classing **DataSet** in its own [ AdgDataSet](/reference/datagate/datagate-client/adg-data-set.html) class. **AdgDataSet** effectively provides a bridge between the record-oriented access world of DataGate and AVR and set-oriented access methods. For a complete introduction to **DataSet** , please consult the .NET documentation.

**AdgDataSet** objects consist of one or more ( **DataTable** ) objects. These **DataTables** represent each format of the file. The **DataTables** contain a collection of ( **DataRow** ) objects. In DG, database file records are contained by **DataRow** objects. Field data of records are accessed by field name or through ( **DataColumn** ) objects, which reference the data and metadata of "columns" in **DataRow** objects. **AdgDataSet** adds methods and properties, such as [ ActiveRow](/reference/datagate/datagate-client/adg-data-set.html#properties) and [PrepareRow](/reference/datagate/datagate-client/adg-data-set-preparerow.html), to facilitate quick, familiar access patterns to the data in **AdgDataSets** .

**AdgDataSet** introduces the notion of an "active row" in a **DataSet** . This is the row which represents the database record to be accessed. For example, when a database record is read by one of **FileAdapter’s** read methods, the **AdgDataSet’s** **ActiveRow** property is set to reference the **DataRow** object added to **AdgDataSet** to contain the database record read.

Although DG uses the facilities of a **DataSet** to represent record formats as a set of **DataTables** , **AdgDatSet** provides several methods which automate access to those tables with familiar record format specifications. [ DeleteRow](/reference/datagate/datagate-client/adg-data-set-deleterow.html), [AddRow](/reference/datagate/datagate-client/adg-data-set-addrow.html), [ InsertRow](/reference/datagate/datagate-client/adg-data-set-insertrow.html), and **PrepareRow** all provide direct access to **DataRow** objects in **DataTables** corresponding to a specific record format. 

As records are read from a file or added via **InsertRow** they accumulate in the **DataTable** for the format. The **ActiveRow** property only references the last record read - previously read/inserted records remain in the **DataTable** until they are explicitly removed, via **DataSet.Clear** or **DataTable.Clear.** To access or specify accumulated **DataRow** objects, the **DeleteRow** , **InsertRow** , and [SetActive](/reference/datagate/datagate-client/adg-data-set-setactive.html) methods provide a *RRN* parameter. 

Note that accessing **DataRow** objects in **AdgDataSet** is not the same as accessing records in a database file. Database records can only be read, added, updated, and removed via [ FileAdapter](/reference/datagate/datagate-client/file-adapter.html) methods. **AdgDataSet** methods only access the in-memory representation of a database file's formats, not the underlying database file. **FileAdapter** methods use the **AdgDataSet** as a repository for database records read, added, and updated.
## See Also


[AdgDataSet Class](/reference/datagate/datagate-client/adg-data-set.html)
      <br />
[ActiveRow Property](/reference/datagate/datagate-client/adg-data-set.html#properties)
      <br />
[AddRow Methods](/reference/datagate/datagate-client/adg-data-set-addrow.html)
      <br />
[DeleteRow Method](/reference/datagate/datagate-client/adg-data-set-deleterow.html)
      <br />
[InsertRow Methods](/reference/datagate/datagate-client/adg-data-set-insertrow.html)
      <br />
[PrepareRow Methods](/reference/datagate/datagate-client/adg-data-set-preparerow.html)
      <br />
[SetActive Methods](/reference/datagate/datagate-client/adg-data-set-setactive.html)
      <br />
[FileAdapter Class](/reference/datagate/datagate-client/file-adapter.html)
      <br />
      <br />
      [Reading and Writing to Database 
					Files](readingand-writingto-database-files.html)
      <br />
      [Verifying Results with 
					Exception Handling](verifying-resultswith-exception-handling.html)
      <br />
[Using the FileAdapter Class](usingthe-file-adapter-class.html)
      <br />
[Efficient File Access](efficient-file-access.html)

