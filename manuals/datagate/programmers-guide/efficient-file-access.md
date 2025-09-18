---
title: "Efficient File Access Techniques"
description: "Master efficient file access with our guide. Learn to improve performance and security when accessing files in your applications."
---

Previously, we saw how a file can be read using the [ FileAdapter](file-adapter-class.html) and [AdgDataSet](adg-dataset-class.html) objects. FileAdapter’s [ReadSequential](file-adapter-class-read-sequential-method.html) method is the best way to read each record of a file in succession. For large files, using this method to find a particular record of interest can be inefficient. The [ReadRandomRRN](file-adapter-class-read-random-rrn-method.html), [ReadRandomKey](file-adapter-class-read-random-key-method.html), [ ReadRange](file-adapter-class-read-range-method.html), and [ReadSequentialEqual](file-adapter-class-read-sequential-equal-method.html) methods are provided for this reason.

**ReadRandomRRN** reads a record specified by relative record number (RRN). **ReadRandomRRN** may not be implemented by all DG database providers, but it allows "random" access to files that may be otherwise non-indexed. On the other hand, **ReadRandomKey** , **ReadRange** , and **ReadSequentialEqual** are methods for reading files that are indexed by key data. To use these, one or more data keys must be initialized and passed to the method.

In DG, key and record data are modeled as **DataRow** objects. **DataColumn** objects in the **DataColumnCollection** of the **DataTable** corresponding to the record format or key contain the basic type information for each field. The [ActiveRow](adg-dataset-class-active-row-property.html) property of **AdgDataSet** is a reference to the **DataRow** object representing the data in the record accessed. 

Likewise, a **DataRow** object can represent a key. Generally, to obtain a **DataRow** object for a particular record format’s key you would use the [NewKeyTable](adg-dataset-class-new-key-table-methods.html) method of **AdgDataSet.** Use this method on the **AdgDataSet** object returned by the [OpenNewAdgDataSet](file-adapter-class-open-new-adg-dataset-method.html) method of **FileAdapter** . **NewKeyTable** returns an [AdgKeyTable](adg-key-table-class.html) object reference containing the **DataRow** object for the key.

The [Row](adg-key-table-class-row-property.html) property of **AdgKeyTable** references this **DataRow** . As with the [ PrepareRow](adg-dataset-class-prepare-row-method-main.html) methods of **AdgDataSet** , the **DataRow** referenced by **AdgKeyTable** will be initialized with "null values". Before using the new key in a **ReadRandomKey** method call, the **Value** properties should be set to reflect the key being sought, as in the following example.

```cs 
  AdgConnection Cx;
  FileAdapter DbFile;
  AdgDataSet Ds;
  AdgKeyTable KeyTbl;
  Cx = createAdgConnection("MyDatabaseName");
  Cx.Open();
  DbFile = new FileAdapter(Cx,"Asna_example_files/custmast","*first");
  DbFile.AccessMode = AccessMode.RWCD;
  DbFile.OpenNewAdgDataSet( ref Ds );
  KeyTbl = Ds.NewKeyTable(ds.GetFormatName(0));
  KeyTbl.Row["CMCustNo"] = 500;
  DbFile.ReadRandomKey( Ds, ReadRandomMode.GTEQ, LockRequest.Default, KeyTbl );
  Console.WriteLine( "CMCustNo = " + Ds.ActiveRow["CMCustNo"] ) ;
```

> See [AdgConnection Example](/reference/datagate/datagate-client/adg-connection.html#create-an-adgconnection) for an implementation of `createAdgConnection()`

In the above example, we access a file using the **ReadRandomKey** method. This particular file has one key field named "CMCustNo". The **NewKeyTable** method is called on the **AdgDataSet** returned from **OpenNewAdgDataSet.** **NewKeyTable** is passed the format name of the only format of the file. Note that we use the [GetFormatName](adg-dataset-class-get-format-name-method.html) method of **AdgDataSet** to avoid hard-coding the format name. The returned **AdgKeyTable** object contains one **DataRow** object consisting of only one database field value for the CMCustNo field. This key field is initialized with the integer value 500 in this example. Next, **ReadRandomKey** is called passing the key value in the **AdgKeyTable** object. Also note that the [ ReadRandomMode.GTEQ](read-random-mode-enumeration.html) is passed to **ReadRandomKey** . This specifies that we would like to read the next record containing the given key, or otherwise the next record containing a key greater than the given key.
## See Also


[AdgDataSet Class](adg-dataset-class.html) <br />
[ActiveRow Property](adg-dataset-class-active-row-property.html) <br />
[GetFormatName Method](adg-dataset-class-get-format-name-method.html) <br />
[PrepareRow Methods](adg-dataset-class-prepare-row-method-main.html) <br />
[FileAdapter Class](file-adapter-class.html) <br />
[ReadSequential Method](file-adapter-class-read-sequential-method.html) <br />
[ReadRandomRRN Method](file-adapter-class-read-random-rrn-method.html) <br />
[ReadRandomKey Method](file-adapter-class-read-random-key-method.html) <br />
[ReadRange Method](file-adapter-class-read-range-method.html) <br />
[ReadSequentialEqual Method](file-adapter-class-read-sequential-equal-method.html) <br />
[OpenNewAdgDataSet Method](file-adapter-class-open-new-adg-dataset-method.html) <br />
[AdgKeyTable Class](adg-key-table-class.html) <br />
[Row Property](adg-key-table-class-row-property.html) <br />
[ReadRandomMode Enumeration](read-random-mode-enumeration.html) <br />
[Reading and Writing to Database Files](readingand-writingto-database-files.html)<br />
[Verifying Results with Exception Handling](verifying-resultswith-exception-handling.html)<br />
[Using the FileAdapter Class](usingthe-file-adapter-class.html)<br />
[Database File Records and AdgDataSet](database-file-recordsand-adg-dataset.html)

