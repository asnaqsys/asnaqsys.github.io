---
title: Reading and Writing to Database Files

---

The following example <span>opens a database file</span> for "read" access and then reads the first record in the file.

```cs
 
  using ASNA.DataGate.Client;
  using ASNA.DataGate.Common;
  ...
  AdgConnection Cx;
  FileAdapter DBFile;
  AdgDataSet Ds;
  Cx = new AdgConnection("ASNA Local DB");
  Cx.Open();
  DbFile = new FileAdapter(Cx,"/cmmaster","*first");
  DbFile.OpenNewAdgDataSet( ref Ds );
  DbFile.ReadSequential (Ds, ReadSequentialMode.Next, LockRequest.Default);
  Console.WriteLine("CMCustNo = " + Ds.ActiveRow["CMCustNo"]);

```

Upon the successful completion of the `DbFile.ReadSequential` method in this example, the database file cursor represented by DbFile will rest on the first record of the file. Also, the data contained in the first record is available via the **AdgDataSet** object referred to by the Ds variable. The most recent record read into **AdgDataSet** is accessible via its `ActiveRow` property. In the last line of the example, the value of a field in the record (CMCustNo) is referenced from the ActiveRow property and displayed in a message box.

Other FileAdapter methods provide the record-oriented "read" access functions familiar to RPG and AS/400 programmers, including reading by key and reading by RRN. Keyed-access is explained in more detail in the Advanced Topics section (coming soon).

To update a database file record, the `ChangeCurrent` method of FileAdapter is used. First, the record to be updated is read as in the previous example. Then the fields whose values are to be changed are accessed by name as above.

The following example illustrates one procedure for **updating a file**.


```cs
  AdgConnection cx; 
  FileAdapter dbFile;
  AdgDataSet ds;
  cx = new AdgConnection("ASNA Local DB");
  cx.Open();
  dbFile = new FileAdapter(cx, "/cmmaster", "*first");
  dbFile.AccessMode = AccessMode.Change + AccessMode.Read;
  dbFile.OpenNewAdgDataSet(ds);
  dbFile.ReadSequential(ds, ReadSequentialMode.Next, LockRequest.Default);
  ds.ActiveRow.Item("CMCustNo") = 101;
  dbFile.ChangeCurrent(ds);
  dbFile.Close();
  cx.Close();
```

This example simply opens and reads the first record as in the previous example, then sets the value of the CMCustNo field before calling the [ ChangeCurrent](file-adapter-class-change-current-method.html) method to send the change to the server. Note that we have set the [AccessMode](file-adapter-class-access-mode-property.html) property of the **FileAdapter** object prior to calling the [ OpenNewAdgDataSet](file-adapter-class-open-new-adg-dataset-method.html) method. This informs the server that records in the opened file are to be read and updated. If not set explicitly, the <span> **AccessMode** </span> property value is Read, for read-only access.

The procedure for adding new records to database files follows a similar pattern, but the <span> **DataRow** </span> object representing the record to be inserted must be initialized according to the file format it represents. New **DataRow** objects to be added to a file are initialized with the [ PrepareRow ](adg-dataset-class-prepare-row-method-main.html)method of **AdgDataSet** . This method is passed an index identifying the format of the record to be added, so that the new **DataRow** can be initialized with field objects of the appropriate name and type. Note that fields are initialized with the value <span>System.DBNull.Value</span>. Unless the corresponding database field supports "null values", the **DataRow** field value must be set explicitly by your program before the record is added to the database or an exception will occur. After setting field values in the new record you must append it to the dataset using a method such as [ AddPreparedRowAndSetActive](adg-dataset-class-add-prepared-row-and-set-active-method.html). Once the prepared row is the active row in the **AdgDataSet** , the [ FileAdapter.AddRecord](file-adapter-class-add-record-method.html) method can be called to add the new record to the database file.

The following example illustrates an appropriate sequence for **adding a database record** .

```cs 
  using ASNA.DataGate.Client;
  using ASNA.DataGate.Common;
  ...
  AdgConnection cx;
  FileAdapter dbFile;
  AdgDataSet ds;
  cx.Open();
  dbFile.AccessMode = AccessMode.RWCD;
  dbFile.OpenNewAdgDataSet(ds);
  newRow DataRow;
  newRow = ds.PrepareRow(0);
  newRow["CMCustNo"] = 1;
  newRow["CMName"] = "Important Co.";
  newRow["CMAddr1"] = "1 Business Way";
  newRow["CMAddr2"] = "";
  newRow["CMCity"] = "Portland";
  newRow["CMState"] = "FL";
  newRow["CMPostCode"] = "21012";
  newRow["CMActive"] = "1";
  newRow["CMFax"] = 1232344567;
  newRow["CMPhone"] = "(234)456-6789";
  ds.AddPreparedRowAndSetActive(0);
  dbFile.AddRecord(ds);
  dbFile.Close();
  cx.Close();
```

## See Also

[AdgDataSet Class](/reference/datagate/datagate-client/adg-data-set.html)
<br />
[FileAdapter Enumeration](/reference/datagate/datagate-providers/i-file-adapter.html)
<br />
[Verifying Results with Exception Handling](/manuals/datagate/programmers-guide/verifying-resultswith-exception-handling.html)
<br />
[Using the FileAdapter Class](/manuals/datagate/programmers-guide/usingthe-file-adapter-class.html)

