---
title: "Efficient File Access Techniques"
description: "Master efficient file access with our guide. Learn to improve performance and security when accessing files in your applications."
---

Previously, we saw how a file can be read using the [ FileAdapter](/reference/datagate/datagate-client/file-adapter.html) and [AdgDataSet](/reference/datagate/datagate-client/adg-data-set.html) objects. FileAdapter’s [ReadSequential](/reference/datagate/datagate-client/file-adapter-readsequential.html) method is the best way to read each record of a file in succession. For large files, using this method to find a particular record of interest can be inefficient. The [ReadRandomRRN](/reference/datagate/datagate-client/file-adapter-readrandomrrn.html), [ReadRandomKey](/reference/datagate/datagate-client/file-adapter-readrandomkey.html), [ ReadRange](/reference/datagate/datagate-client/file-adapter-readrange.html), and [ReadSequentialEqual](/reference/datagate/datagate-client/file-adapter-readsequentialequal.html) methods are provided for this reason.

**ReadRandomRRN** reads a record specified by relative record number (RRN). **ReadRandomRRN** may not be implemented by all DG database providers, but it allows "random" access to files that may be otherwise non-indexed. On the other hand, **ReadRandomKey** , **ReadRange** , and **ReadSequentialEqual** are methods for reading files that are indexed by key data. To use these, one or more data keys must be initialized and passed to the method.

In DG, key and record data are modeled as **DataRow** objects. **DataColumn** objects in the **DataColumnCollection** of the **DataTable** corresponding to the record format or key contain the basic type information for each field. The [ActiveRow](/reference/datagate/datagate-client/adg-data-set.html#properties) property of **AdgDataSet** is a reference to the **DataRow** object representing the data in the record accessed. 

Likewise, a **DataRow** object can represent a key. Generally, to obtain a **DataRow** object for a particular record format’s key you would use the [NewKeyTable](/reference/datagate/datagate-client/adg-data-set-newkeytable.html) method of **AdgDataSet.** Use this method on the **AdgDataSet** object returned by the [OpenNewAdgDataSet](/reference/datagate/datagate-client/file-adapter-opennewadgdataset.html) method of **FileAdapter** . **NewKeyTable** returns an [AdgKeyTable](/reference/datagate/datagate-client/adg-key-table.html) object reference containing the **DataRow** object for the key.

The [Row](/reference/datagate/datagate-client/adg-key-table.html#properties) property of **AdgKeyTable** references this **DataRow** . As with the [ PrepareRow](/reference/datagate/datagate-client/adg-data-set-preparerow.html) methods of **AdgDataSet** , the **DataRow** referenced by **AdgKeyTable** will be initialized with "null values". Before using the new key in a **ReadRandomKey** method call, the **Value** properties should be set to reflect the key being sought, as in the following example.

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

In the above example, we access a file using the **ReadRandomKey** method. This particular file has one key field named "CMCustNo". The **NewKeyTable** method is called on the **AdgDataSet** returned from **OpenNewAdgDataSet.** **NewKeyTable** is passed the format name of the only format of the file. Note that we use the [GetFormatName](/reference/datagate/datagate-client/adg-data-set-getformatname.html) method of **AdgDataSet** to avoid hard-coding the format name. The returned **AdgKeyTable** object contains one **DataRow** object consisting of only one database field value for the CMCustNo field. This key field is initialized with the integer value 500 in this example. Next, **ReadRandomKey** is called passing the key value in the **AdgKeyTable** object. Also note that the [ ReadRandomMode.GTEQ](/reference/datagate/datagate-common/read-random-mode.html) is passed to **ReadRandomKey** . This specifies that we would like to read the next record containing the given key, or otherwise the next record containing a key greater than the given key.
## See Also


[AdgDataSet Class](/reference/datagate/datagate-client/adg-data-set.html) <br />
[ActiveRow Property](/reference/datagate/datagate-client/adg-data-set.html#properties) <br />
[GetFormatName Method](/reference/datagate/datagate-client/adg-data-set-getformatname.html) <br />
[PrepareRow Methods](/reference/datagate/datagate-client/adg-data-set-preparerow.html) <br />
[FileAdapter Class](/reference/datagate/datagate-client/file-adapter.html) <br />
[ReadSequential Method](/reference/datagate/datagate-client/file-adapter-readsequential.html) <br />
[ReadRandomRRN Method](/reference/datagate/datagate-client/file-adapter-readrandomrrn.html) <br />
[ReadRandomKey Method](/reference/datagate/datagate-client/file-adapter-readrandomkey.html) <br />
[ReadRange Method](/reference/datagate/datagate-client/file-adapter-readrange.html) <br />
[ReadSequentialEqual Method](/reference/datagate/datagate-client/file-adapter-readsequentialequal.html) <br />
[OpenNewAdgDataSet Method](/reference/datagate/datagate-client/file-adapter-opennewadgdataset.html) <br />
[AdgKeyTable Class](/reference/datagate/datagate-client/adg-key-table.html) <br />
[Row Property](/reference/datagate/datagate-client/adg-key-table.html#properties) <br />
[ReadRandomMode Enumeration](/reference/datagate/datagate-common/read-random-mode.html) <br />
[Reading and Writing to Database Files](readingand-writingto-database-files.html)<br />
[Verifying Results with Exception Handling](verifying-resultswith-exception-handling.html)<br />
[Using the FileAdapter Class](usingthe-file-adapter-class.html)<br />
[Database File Records and AdgDataSet](database-file-recordsand-adg-dataset.html)

