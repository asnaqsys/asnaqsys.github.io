---
title: "Mastering DataGate File Adapter Class"
description: "This document explains how to access files using the FileAdapter class, detailing the methods available for file operations such as reading, writing, and managing file metadata."
---

The [ASNA.DataGate.Client.FileAdapter](file-adapter-class.html) class is the entry point for data access in DG. **FileAdapter** consists of a reference to an [AdgConnection](adg-connection-class.html) object and a set of path strings naming the database file being accessed. **FileAdapter** methods allow the standard set of access functions including reading, writing, updating, and deleting file records. It also contains several properties defining constraints on the access to be performed on the file. These properties, such as the [ AccessMode](file-adapter-class-access-mode-property.html) property, should be set prior to opening the file.

**FileAdapter** employs an [AdgDataSet](adg-dataset-class.html) object for data exchange with the database. Thus when a file is opened, you specify an **AdgDataSet** to subsequently be used with the opened file.

The following AVR code opens a database connection and then creates a **FileAdapter** object to be used for reading records from a file.

```cs 
  ASNA.DataGate.Client;
  ASNA.DataGate.Common;
  ...
  AdgConnection Cx;
  FileAdapter DbFile;
  AdgDataSet Ds;
  Cx = createAdgConnection(" ASNA Local DB");
  Cx.Open();
  DbFile = new FileAdapter(Cx,"/cmmaster","*first");
  DbFile.AccessMode = AccessMode.Read;
  DbFile.OpenNewAdgDataSet(ref Ds);
```

> See [AdgConnection Example](/reference/datagate/datagate-client/adg-connection.html#create-an-adgconnection) for an implementation of `createAdgConnection()`

**FileAdapter** models an open database file’s "pointer", or the current position of the virtual record cursor on the database server. For example, **FileAdapter’s** [ OpenNewAdgDataSet](file-adapter-class-open-new-adg-dataset-method.html) method sets the record cursor to just prior to the first record in the file. **FileAdapter** also includes "<span>seek</span>" methods, used to place the record cursor to positions of particular interest. The [CurrentFormatIndex](file-adapter-class-current-format-index-property.html), [FormatRequested](file-adapter-class-format-requested-property.html), [ RRN](file-adapter-class-rrn-property.html), and [ExactSeek](file-adapter-class-exact-seek-property.html) properties of **FileAdapter** provide indicators of the current position of the record cursor.
## See Also


[AdgConnection Class](adg-connection-class.html) <br />
[AdgDataSet Class](adg-dataset-class.html) <br />
[FileAdapter Class](file-adapter-class.html) <br />
[FileAdapter Class Members](file-adapter-members.html) <br />
[Database File Records and AdgDataSet](database-file-recordsand-adg-dataset.html) <br />
[Efficient File Access](efficient-file-access.html) <br />
[Reading and Writing to Database Files](readingand-writingto-database-files.html) <br />
[Verifying Results with Exception Handling](verifying-resultswith-exception-handling.html)

