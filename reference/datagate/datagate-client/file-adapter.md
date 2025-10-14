---
title: "FileAdapter class   | QSYS API Reference Guide"
description: "The  class manages file operations like opening, closing, reading, writing, and querying, handling various access modes and settings. "
---

**Namespace:** ASNA.DataGate.Client
**Assembly:** ASNA.QSys.DataGate.Client.dll

The class manages file operations like opening, closing, reading, writing, and querying, handling various access modes and settings.


**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>
## Thread Safety

Any public static (Shared) members of this type are safe for multithreaded operations. Any instance members are not guaranteed to be thread safe.

## Remarks

 **FileAdapter** models an open database file, and when used in conjunction with the `AdgConnection` class, can be used to read, write, update, and delete database records.  The **FileAdapter** class maintains a "file pointer" or a server-side indicator of the current position for record operations on the file.

Several "open" methods perform the function of opening a file for access operations.  These methods define an `AdgDataSet`parameter, which is bound to the open file to contain database records.  Generally, the access methods and properties of **FileAdapter** are unavailable before the file is open.  The `Status` property can be used to determine if a file is currently closed or is already open.  An `Open`method call reopens a database file closed by a preceding `Close` method call.

The **Open** method is used to open a file with a preexisting **AdgDataSet** object.  In general, this method should be reserved for use by development environments such as Visual RPG, which generate strongly-typed data sets at compile-time.

`OpenNewAdgDataSet` opens a database file member specified by the `Connection`, `FileName`, and `MemberName` properties.  A new **AdgDataSet** object is created and returned as an output parameter reference.

Before calling an open method, properties may be set to modify the access or availability of the open file.  The `AccessMode` property may be set with the values of `AccessMode enumeration`  to indicate how the open file will be accessed.  `OpenAttributes` references the `FileOpenAttr`object, which is used to specify many properties of open files.  For example, the `FileOpenAttr.FormatIDs`property may be assigned an array of format identifiers used in a "level-check" operation to verify that the format of the file is the format expected.

The record access methods of the **FileAdapter** class are used to read and write records to an open file.  However, **FileAdapter’s** `SeekRange`, `SeekRRN`, and `SeekKey` methods may be used to change the file pointer without reading or changing the file.  The `DeleteCurrent`,`ChangeCurrent`, and `ReleaseCurrent` methods operate upon the "current record", or the record last read from or written to the file.

Several indicator properties may be used to determine the side effects of a preceding access operation on the **FileAdapter** object.  `ExactSeek` is set to <b>true</b> if a seek operation results in placing the file pointer on a record containing a specified key or RRN.  `RRN` contains the "relative-record number" of the last record accessed, if the database provider supports this information.  `CurrentFormatIndex` identifies the format of the record most recently accessed.

The `SetFormat` method is available for multiformat read access.  Calling this method causes the read methods to fetch only those records with the given format.  To read all record formats, specify a null or empty string.  `FormatRequested` is the record format for reading multiformat file records.

To improve the efficiency of sequential access to files residing on network database servers, specify the `FileOpenAttr.BlockingFactor` property of the **OpenAttributes** property.  Even more efficiency can be achieved with the proper use of the "range" methods, `SeekRange`,`ReadRange`, and `DeleteRange`.


## Constructors

| Name | Description |
| ---- | ----------- |
| [FileAdapter()](file-adapter-ctor.html#fileadapter) | Initializes a new instance of the FileAdapter class without a connection.
| [FileAdapter](file-adapter-ctor.html#fileadapteradgconnection)([AdgConnection](/reference/datagate/datagate-client/adg-connection.html)) | Initializes a new instance of the FileAdapter class with a connection.
| [FileAdapter](file-adapter-ctor.html#fileadapteradgconnection-string)([AdgConnection](/reference/datagate/datagate-client/adg-connection.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Initializes a new instance of the FileAdapter class with a connection and a file name.
| [FileAdapter](file-adapter-ctor.html#fileadapteradgconnection-string-string)([AdgConnection](/reference/datagate/datagate-client/adg-connection.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Initializes a new instance of the FileAdapter class with a connection, a file name, and a member name.
| [FileAdapter](file-adapter-ctor.html#fileadapterifileobject-string)([IFileObject](/reference/datagate/datagate-client/i-file-object.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Initializes a new instance of the FileAdapter class with a FileObject and a member name.
| [FileAdapter](file-adapter-ctor.html#fileadapterifileobject)([IFileObject](/reference/datagate/datagate-client/i-file-object.html)) | Initializes a new instance of the FileAdapter class with a FileObject.

For detailed constructor documentation, see [FileAdapter Constructors](file-adapter-ctor.html).

## Properties

| Type | Name | Description
| --- | --- | --- 
| [AccessMode](/reference/datagate/datagate-common/access-mode.html) | AccessMode | Gets or sets the access mode of the FileAdapter. |
| [AdgConnection](/reference/datagate/datagate-client/adg-connection.html) | Connection | Gets or sets the connection of the FileAdapter. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | CurrentFormatIndex | Gets the index of the current format in the file that the FileAdapter is working with. |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | ExactSeek | Gets a value indicating whether the file that the FileAdapter is working with is in exact seek mode. |
| [Hashtable](https://learn.microsoft.com/en-us/dotnet/api/system.collections.hashtable?view=net-8.0) | ExtendedResults | Gets a Hashtable containing the extended results for the file that the FileAdapter is working with. |
| [Int64](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | FileLength | Gets the length of the file that the FileAdapter is working with. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | FileName | Gets or sets the name of the file that the FileAdapter is working with. |
| [IFileObject](/reference/datagate/datagate-client/i-file-object.html) | FileObject | Gets the FileObject that the FileAdapter is working with. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | FormatRequested | Gets the index of the format that was requested for the file that the FileAdapter is working with. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | FormatToUse | Gets the index of the format that is currently being used in the file that the FileAdapter is working with. |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | IsBulkWriter | Gets a value indicating whether the file that the FileAdapter is working with supports bulk writing. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | LibraryName | Gets the name of the library that the file that the FileAdapter is working with is located in. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | MemberName | Gets or sets the name of the member that the FileAdapter is working with. |
| [FileOpenAttr](/reference/datagate/datagate-providers/file-open-attr.html) | OpenAttributes | Gets or sets the open attributes of the FileAdapter. |
| [Int64](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | RecordCount | Gets the record count of the file that the FileAdapter is working with. |
| [Int64](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | RRN | Gets the relative record number (RRN) of the current record in the file that the FileAdapter is working with. |
| [AdapterStatus](/reference/datagate/datagate-client/adapter-status.html) | Status | Gets the current status of the FileAdapter. |

## Methods

| Signature | Description |
| --- | --- |
| [AddRecord](file-adapter-addrecord.html#void-addrecordadgdataset)([AdgDataSet](/reference/datagate/datagate-client/adg-data-set.html)) | Adds a record to the file using the provided AdgDataSet.
| [AddRecord](file-adapter-addrecord.html#void-addrecordxmlreader-adgdataset)([XmlReader](https://learn.microsoft.com/en-us/dotnet/api/system.xml.xmlreader?view=net-8.0), [AdgDataSet](/reference/datagate/datagate-client/adg-data-set.html)) | Adds a record to the file using the provided XmlReader and AdgDataSet.
| [AddRecord](file-adapter-addrecord.html#void-addrecordadgdataset-char)([AdgDataSet](/reference/datagate/datagate-client/adg-data-set.html), [Char\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.char)) | Adds a record to the file using the provided AdgDataSet and application indicators.
| [ChangeCurrent](file-adapter-changecurrent.html)([AdgDataSet](/reference/datagate/datagate-client/adg-data-set.html)) | Changes the current record in the file using the provided AdgDataSet.
| [ChangeRRN](file-adapter-changerrn.html)([AdgDataSet](/reference/datagate/datagate-client/adg-data-set.html), [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64)) | Changes the current record in the file to the record at the specified relative record number (RRN).
| [CheckKey](file-adapter-checkkey.html)([AdgKeyTable](/reference/datagate/datagate-client/adg-key-table.html)) | Checks the validity of the provided key table.
| [Close()](file-adapter-close.html) | Closes the FileAdapter and releases all resources used by it.
| [CreateDataSet()](file-adapter-createdataset.html) | Creates a new AdgDataSet for the FileAdapter.
| [DeleteAllRecords()](file-adapter-deleteallrecords.html) | Deletes all records from the file that the FileAdapter is working with.
| [DeleteCurrent()](file-adapter-deletecurrent.html) | Deletes the current record from the file that the FileAdapter is working with.
| [DeleteKey](file-adapter-deletekey.html)([AdgKeyTable](/reference/datagate/datagate-client/adg-key-table.html)) | Deletes the record with the specified key from the file that the FileAdapter is working with.
| [DeleteRange](file-adapter-deleterange.html)([AdgKeyTable](/reference/datagate/datagate-client/adg-key-table.html), [RangeFirst](/reference/datagate/datagate-common/range-first.html), [AdgKeyTable](/reference/datagate/datagate-client/adg-key-table.html), [RangeLast](/reference/datagate/datagate-common/range-last.html)) | Deletes a range of records from the file that the FileAdapter is working with.
| [DeleteRRN](file-adapter-deleterrn.html)([Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64)) | Deletes the record at the specified relative record number (RRN) from the file that the FileAdapter is working with.
| [Dispose()](file-adapter-dispose.html#void-dispose) | Releases all resources used by the FileAdapter.
| [Dispose](file-adapter-dispose.html#void-disposebool)([Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Releases the unmanaged resources used by the FileAdapter and optionally releases the managed resources.
| [Finalize()](file-adapter-finalize.html) | Finalizes an instance of the FileAdapter class.
| [ForceEOD()](file-adapter-forceeod.html) | Forces the end of data (EOD) for the file that the FileAdapter is working with.
| [GetFormatName](file-adapter-getformatname.html)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Gets the name of the format at the specified index in the file that the FileAdapter is working with.
| [GetPrintProperties](file-adapter-getprintproperties.html)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Gets the print properties for the specified format in the file that the FileAdapter is working with.
| [Open](file-adapter-open.html)([AdgDataSet](/reference/datagate/datagate-client/adg-data-set.html)) | Opens the FileAdapter with the specified AdgDataSet.
| [OpenNewAdgDataSet](file-adapter-opennewadgdataset.html)([AdgDataSet&](/reference/datagate/datagate-client/adg-data-set.html)) | Opens a new AdgDataSet for the FileAdapter.
| [OpenSimpleQuery](file-adapter-opensimplequery.html)([AdgDataSet&](/reference/datagate/datagate-client/adg-data-set.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.string), [KeyUsages\[\]](/reference/datagate/datagate-common/key-usages.html)) | Opens the FileAdapter with a simple query.
| [ReadRandomKey](file-adapter-readrandomkey.html)([AdgDataSet](/reference/datagate/datagate-client/adg-data-set.html), [ReadRandomMode](/reference/datagate/datagate-common/read-random-mode.html), [LockRequest](/reference/datagate/datagate-common/lock-request.html), [AdgKeyTable](/reference/datagate/datagate-client/adg-key-table.html)) | Reads a record from the file that the FileAdapter is working with using the specified key.
| [ReadRandomRRN](file-adapter-readrandomrrn.html)([AdgDataSet](/reference/datagate/datagate-client/adg-data-set.html), [ReadRandomMode](/reference/datagate/datagate-common/read-random-mode.html), [LockRequest](/reference/datagate/datagate-common/lock-request.html), [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64)) | Reads a record from the file that the FileAdapter is working with using the specified relative record number (RRN).
| [ReadRange](file-adapter-readrange.html)([AdgDataSet](/reference/datagate/datagate-client/adg-data-set.html), [RangeMode](/reference/datagate/datagate-common/range-mode.html), [LockRequest](/reference/datagate/datagate-common/lock-request.html), [AdgKeyTable](/reference/datagate/datagate-client/adg-key-table.html), [RangeFirst](/reference/datagate/datagate-common/range-first.html), [AdgKeyTable](/reference/datagate/datagate-client/adg-key-table.html), [RangeLast](/reference/datagate/datagate-common/range-last.html)) | Reads a range of records from the file that the FileAdapter is working with using the specified keys.
| [ReadSequential](file-adapter-readsequential.html)([AdgDataSet](/reference/datagate/datagate-client/adg-data-set.html), [ReadSequentialMode](/reference/datagate/datagate-common/read-sequential-mode.html), [LockRequest](/reference/datagate/datagate-common/lock-request.html)) | Reads a record from the file that the FileAdapter is working with sequentially.
| [ReadSequentialEqual](file-adapter-readsequentialequal.html)([AdgDataSet](/reference/datagate/datagate-client/adg-data-set.html), [ReadEqualMode](/reference/datagate/datagate-common/read-equal-mode.html), [LockRequest](/reference/datagate/datagate-common/lock-request.html), [AdgKeyTable](/reference/datagate/datagate-client/adg-key-table.html)) | Reads a record from the file that the FileAdapter is working with sequentially and equal to the specified key.
| [ReleaseCurrent()](file-adapter-releasecurrent.html) | Releases the lock on the current record in the file that the FileAdapter is working with.
| [ReleaseRRN](file-adapter-releaserrn.html)([LockRequest](/reference/datagate/datagate-common/lock-request.html), [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64)) | Releases the lock on the record at the specified relative record number (RRN) in the file that the FileAdapter is working with.
| [ResetFormat()](file-adapter-resetformat.html) | Resets the format of the file that the FileAdapter is working with to the default format.
| [ResetPrintAttr()](file-adapter-resetprintattr.html) | Resets the print attributes for the file that the FileAdapter is working with.
| [ReuseRRN](file-adapter-reuserrn.html)([AdgDataSet](/reference/datagate/datagate-client/adg-data-set.html), [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64)) | Reuses the record at the specified relative record number (RRN) in the file that the FileAdapter is working with.
| [SeekKey](file-adapter-seekkey.html)([SeekMode](/reference/datagate/datagate-common/seek-mode.html), [AdgKeyTable](/reference/datagate/datagate-client/adg-key-table.html)) | Positions the file pointer at the record with the specified key in the file that the FileAdapter is working with.
| [SeekRange](file-adapter-seekrange.html)([RangeMode](/reference/datagate/datagate-common/range-mode.html), [AdgKeyTable](/reference/datagate/datagate-client/adg-key-table.html), [RangeFirst](/reference/datagate/datagate-common/range-first.html), [AdgKeyTable](/reference/datagate/datagate-client/adg-key-table.html), [RangeLast](/reference/datagate/datagate-common/range-last.html)) | Positions the file pointer at the first record in the specified range in the file that the FileAdapter is working with.
| [SeekRRN](file-adapter-seekrrn.html)([SeekMode](/reference/datagate/datagate-common/seek-mode.html), [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64)) | Positions the file pointer at the record with the specified relative record number (RRN) in the file that the FileAdapter is working with.
| [SetFormat](file-adapter-setformat.html)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Sets the format of the file that the FileAdapter is working with to the specified format.
| [ThrowIfNotOpen\<T\>](file-adapter-throwifnotopen.html)([T](https://learn.microsoft.com/en-us/dotnet/api/system.type?view=net-8.0)) | Checks if the provided state is open. If it is, the state is returned. If it is not, an exception is thrown.

## Examples
Most of the following examples create an AdgConnection by calling the `createAdgConnection()` method which is part of the [AdgConnection Example](/reference/datagate/datagate-client/adg-connection.html#create-an-adgconnection) showing how to `new` an `AdgConnection` using a Database Source Profile Name.


### Example 1. Use of WaitForRecord Open attribute property. 


```cs 
  /* Opens a record which will spend no time waiting for a record
   * if that record is locked. */
  AdgConnection db = createAdgConnection("MyDatabaseName");
  FileAdapter dbFile = new FileAdapter(db, "*Libl/CMASTNEW", "CMMASTER");
  dbFile.AccessMode = AccessMode.Delete;
  dbFile.OpenAttributes.WaitForRecord = 0;
  AdgDataSet myDS = null;
  dbFile.OpenNewAdgDataSet(out myDS);

```


### Example 2. Use of ShareTypes Open attribute property.

```cs 
  /* We open the file in order to delete all of its records. */
  AdgConnection db = createAdgConnection("MyDatabaseName");
  FileAdapter dbFile = new FileAdapter(db, "*Libl/CMASTNEW", "CMMASTER");
  dbFile.AccessMode = AccessMode.Delete;
  /* Its generally good practice to make sure you have an exclusive lock
   * on a file that you are deleting all of the records from, but some
   * databases do not require it. */
  dbFile.OpenAttributes.ShareTypes = ShareTypes.Exclusive;
  AdgDataSet myDS = null;

  try
  {
      dbFile.Open(myDS);
      dbFile.DeleteAllRecords();
  }
  catch(dgException dgEx)
  {
      db.Close();
      if (dgEx.Error == dgErrorNumber.dgEmBUSYOBJ)
      {
          MessageBox.Show("Couldn't open the file for exclusive access.", "Error opening file.");
          //Exit routine or procedure here to avoid preceding file operations.
      }
      else 
          throw dgEx;
  }
  dbFile.DeleteAllRecords();

  dbFile.Close();
  db.Close();
```

### Example 3. Use of BlockingFactor Open attribute property.

```cs 
  AdgConnection db = createAdgConnection("MyDatabaseName");
  FileAdapter dbFile = new FileAdapter(db, "*Libl/CMASTNEWL1", "CMMASTERL1");
  dbFile.AccessMode = AccessMode.Read;

  /* Automatically calculates the best blocking factor. */
  dbFile.OpenAttributes.BlockingFactor = FileOpenAttr.OptimalBlockingFactor;
  AdgDataSet ds = null;
  dbFile.OpenNewAdgDataSet(out ds);
```

### Example 4. Use of OmitBlocking BlockingFactor Open attribute property.

```cs
  AdgConnection db = createAdgConnection("MyDatabaseName"); 
  FileAdapter dbFile = new FileAdapter(db, "*Libl/CMASTNEWL1", "CMMASTERL1"); 
  dbFile.AccessMode = AccessMode.Read; /* Omits record blocking feature. */
  dbFile.OpenAttributes.BlockingFactor = FileOpenAttr.OmitBlocking;
  AdgDataSet ds = null;
  dbFile.OpenNewAdgDataSet(out ds);
```

### Example 5. Using the FileLocks property of a FileAdapter's OpenAttributes

```cs 
  /* Using the FileLocks property of a FileAdapter's OpenAttributes,
   * you can set file locking to manual, which allows you to lock more
   * than one record at a time. Note that manual file locking
   * is database dependent- for instance, it will work with a Acceler8
   * database but not with an IBM i. */
  AdgConnection db = createAdgConnection("MyDatabaseName");
  FileAdapter dbFile = new FileAdapter(db, "*Libl/CMASTNEWL1", "CMMASTERL1");
  dbFile.OpenAttributes.FileLocks = FileLocks.Manual;
  dbFile.AccessMode = AccessMode.RWCD;

  AdgDataSet myDS = null;
  dbFile.OpenNewAdgDataSet(out myDS);
  AdgKeyTable keyTbl = myDS.NewKeyTable("RCMMASTL1");

  /* In the code below, we read records for customer numbers
   * 400 - 800. When it ends, we will still have locks on customer numbers
   * 500 and 700. */
  try
  {
      /* Read customer number 400 but don't lock it. */
      keyTbl.Row["CMCUSTNO"] = 400;
      dbFile.ReadRandomKey(myDS, ReadRandomMode.Equal, LockRequest.NoLock, keyTbl);

      /* Read customer number 500 and lock it. */
      keyTbl.Row["CMCUSTNO"] = 500;
      dbFile.ReadRandomKey(myDS, ReadRandomMode.Equal, LockRequest.Read, keyTbl);

      /* Read customer number 600 and lock it. */
      dbFile.ReadSequential(myDS, ReadSequentialMode.Next, LockRequest.Read);

      /* Read customer number 700 and lock it. */
      dbFile.ReadSequential(myDS, ReadSequentialMode.Next, LockRequest.Read);

      /* Read customer number 800 without locking it. */
      dbFile.ReadSequential(myDS, ReadSequentialMode.Next, LockRequest.NoLock);

      /* Unlock customer number 600. */
      keyTbl.Row["CMCUSTNO"] = 600;
      dbFile.ReadRandomKey(myDS, ReadRandomMode.Equal, LockRequest.NoLock, keyTbl);
      dbFile.ReleaseCurrent();

  }
  catch(dgException dgEx)
  { 
      MessageBox.Show("Couldn't find one or more records. " + dgEx.Message,
          dgEx.Error.ToString());
  }

  dbFile.Close(); /* Release all locks. */
  db.Close();
```

### Example 6. Using an specific BlockingFactor value to periodically update a progress bar.

```cs 
  AdgConnection db = createAdgConnection("MyDatabaseName");
  FileAdapter dbFile = new FileAdapter(db, "*Libl/CMASTNEWL1", "CMMASTERL1");
  dbFile.AccessMode = AccessMode.Read;
  AdgDataSet myDS = null;

  int refreshInterval = 10; //Used so we don't slow down refreshing too much...
  dbFile.OpenAttributes.BlockingFactor = refreshInterval;
  dbFile.OpenNewAdgDataSet(out myDS);

    /* Here, we read every record until end of file is reached.
    * Because this is an fairly long process, we set up a progress bar
    * to keep the user from being discouraged. We set its Maximum
    * value to the number of records in the file, which is found
    * using FileAdapter's RecordCount property, divided by
    * our refreshInterval. */
  int recordsReadSinceLastRefresh = 0;
  prgBar.Minimum = 0;
  prgBar.Maximum = Convert.ToInt32(dbFile.RecordCount) / refreshInterval;

  bool EOF = false;
  while(!EOF)
  {
      try
      {
         /* Though it seems like we have to read each record one at a time,
          * in reality DG stores the first 10 records the first time we read
          * and then afterwards we simply read from the cache. When those run out, 
          * DG will automatically grab another ten records from the database.
          * Note that 10 is our refresh interval, meaning that this I/O operation
          * occurs at the same time that we update our progress bar. If the blocking
          * factor was higher than our refresh interval, not only would we have to 
          * wait longer to read the first record but the progress bar would go longer
          * without being updated. */
         dbFile.ReadSequential(myDS, ReadSequentialMode.Next, LockRequest.NoWait);
         /* Perform some action on each record here... */
         recordsReadSinceLastRefresh ++;
         if (recordsReadSinceLastRefresh == refreshInterval)
         {
             recordsReadSinceLastRefresh = 0;
             prgBar.PerformStep();
             this.Refresh(); //Refreshes the form.
         }
      }
      catch(dgException dgEx)
      {
          if (dgEx.Error == dgErrorNumber.dgEaEOF)
              EOF = true;
          else
          {
              //Exit procedure or end application here.
          }
      }
  }
  dbFile.Close();
  db.Close()
```


### Example 7. Use of FileLocks enumeration to allow locking more than one record at a time.

```cs 
  /* Using the FileLocks property of a FileAdapter's OpenAttributes,
   * you can set file locking to manual, which allows you to lock more
   * than one record at a time. Note that manual file locking
   * is database dependent- for instance, it will work with a Acceler8
   * database but not with an IBM i. */
  AdgConnection db = createAdgConnection("MyDatabaseName");
  FileAdapter dbFile = new FileAdapter(db, "*Libl/CMASTNEWL1", "CMMASTERL1");
  dbFile.OpenAttributes.FileLocks = FileLocks.Manual;
  dbFile.AccessMode = AccessMode.RWCD;

  AdgDataSet myDS = null;
  dbFile.OpenNewAdgDataSet(out myDS);
  AdgKeyTable keyTbl = myDS.NewKeyTable("RCMMASTL1");

  /* In the code below, we read records for customer numbers
   * 400 - 800. When it ends, we will still have locks on customer numbers
   * 500 and 700. */
  try
  {
      /* Read customer number 400 but don't lock it. */
      keyTbl.Row["CMCUSTNO"] = 400;
      dbFile.ReadRandomKey(myDS, ReadRandomMode.Equal, LockRequest.NoLock, keyTbl);

      /* Read customer number 500 and lock it. */
      keyTbl.Row["CMCUSTNO"] = 500;
      dbFile.ReadRandomKey(myDS, ReadRandomMode.Equal, LockRequest.Read, keyTbl);

      /* Read customer number 600 and lock it. */
      dbFile.ReadSequential(myDS, ReadSequentialMode.Next, LockRequest.Read);

      /* Read customer number 700 and lock it. */
      dbFile.ReadSequential(myDS, ReadSequentialMode.Next, LockRequest.Read);

      /* Read customer number 800 without locking it. */
      dbFile.ReadSequential(myDS, ReadSequentialMode.Next, LockRequest.NoLock);

      /* Unlock customer number 600. */
      keyTbl.Row["CMCUSTNO"] = 600;
      dbFile.ReadRandomKey(myDS, ReadRandomMode.Equal, LockRequest.NoLock, keyTbl);
      dbFile.ReleaseCurrent();

  }
  catch(dgException dgEx)
  {
      MessageBox.Show("Couldn't find one or more records. " + dgEx.Message,
      dgEx.Error.ToString());
  }

  dbFile.Close(); /* Release all locks. */
  db.Close();
```


### Example 8. Checking the status of a FileAdapter object before using it.

Using a fileAdapter object named "dbFile" but are unsure as to whether or not it is been initialized, so we check for null and use the Status property to make sure it is opened and open it if it isn't.

```cs 
  if (dbFile == null)
      dbFile = new FileAdapter();
  if (dbFile.Status == FileAdapter.AdapterStatus.Closed)
  {
      dbFile.SetConnection( myAdgConnection );
      dbFile.FileName = fileName;
      dbFile.MemberName = memberName;
      dbFile.OpenNewAdgDataSet(out myDataSet);
  }
  
```

### Example 9. Use of FileAdapter.SetFormat Method.

```cs 
  /* Read only records from format one. */
  AdgConnection db = createAdgConnection("MyDatabaseName");
  FileAdapter dbFile = new FileAdapter(db, "*Libl/SalesMem", "SalesMem");
  dbFile.AccessMode = AccessMode.Read | AccessMode.Write;
  AdgDataSet myDS = null;
  dbFile.OpenNewAdgDataSet(out myDS);

  /* Add a record to format 0, "RCustMast". */
  /* Get new customer number to avoid adding a duplicate key. */
  dbFile.ReadSequential(myDS, ReadSequentialMode.Last, LockRequest.Read);
  decimal newCustNo = Convert.ToDecimal(myDS.ActiveRow["CMCustNo"]) + 100m;

  DataRow newRecord = myDS.PrepareRow("RCustMast");
  /* Create a customer record. */

  newRecord["CMCustNo"] = newCustNo;
  newRecord["CMName"] = "Amalgamated Software of North America";
  newRecord["CMAddr1"] = "9901 IH-10 West, Suite 1000";
  newRecord["CMCity"] = "San Antonio";
  newRecord["CMState"] = "TX";
  newRecord["CMCntry"] = "US";
  newRecord["CMPostCode"] = "78230";
  newRecord["CMActive"] = "1";
  newRecord["CMPhone"] = "2104080212";

  myDS.AddPreparedRowAndSetActive(0);
  dbFile.SetFormat("RCustMast");
  try
  {
      dbFile.AddRecord(myDS);
  }
  catch(dgException dgEx)
  {
      if (dgEx.Error != dgErrorNumber.dgEaDUPKEY)
          throw dgEx; /* If the 
            exception wasn't thrown due to a duplicate key, throw it again. */
      MessageBox.Show("Key value \"" + 
            newRecord["CMName"].ToString() +
          "\" already in this 
            file.", "Error");
      dbFile.Close();
      db.Close();
      //Exit procedure or take other action here to 
            avoid adding next record.
  }
  /* Now add a record to format 1, "RSalesMast". */
  DataRow newRecord2 = myDS.PrepareRow("RSalesMast");

  /* Create a record of sales for 2004. */
  newRecord2["CSCustNo"] = newRecord["CMCustNo"];
  newRecord2["CSYear"] = 2004m;
  newRecord2["CSType"] = 1m;
  newRecord2["CSSales01"] = 100m;
  newRecord2["CSSales02"] = 200m;
  newRecord2["CSSales03"] = 300m;
  newRecord2["CSSales04"] = 400m;
  newRecord2["CSSales05"] = 500m;
  newRecord2["CSSales06"] = 600m;
  newRecord2["CSSales07"] = 500m;
  newRecord2["CSSales08"] = 400m;
  newRecord2["CSSales09"] = 200m;
  newRecord2["CSSales10"] = 100m;
  newRecord2["CSSales11"] = 1m;
  newRecord2["CSSales12"] = 0m;

  myDS.AddPreparedRowAndSetActive(1);
  dbFile.SetFormat("RSalesMast");
  try
  {
      dbFile.AddRecord(myDS);
  }
  catch(dgException dgEx)
  {
      if (dgEx.Error != dgErrorNumber.dgEaDUPKEY)
          throw dgEx; /* If the 
            exception wasn't thrown due to a duplicate key, throw it again. */
      MessageBox.Show("Key " + 
            newRecord["CSName"].ToString() + " already in this file.", "Error");
  }

  dbFile.Close();
  db.Close();
```


### Example 10. SeekRange method example.

```cs 
  AdgConnection db = createAdgConnection("MyDatabaseName");
  FileAdapter dbFile = new FileAdapter(db, "*Libl/CSMASTERL1", "CSMASTERL1");
  dbFile.AccessMode = AccessMode.Read;
  AdgDataSet myDS = null;
  dbFile.OpenNewAdgDataSet(out myDS);

  /* The code below will find all of the sales for all 
   * customers with a number from 300 to 1400, 
   * and read all the customer numbers from lowest to highest. */
  AdgKeyTable key1 = myDS.NewKeyTable("RCSMASTL1");
  key1.Row["CSCUSTNO"] = Convert.ToDecimal(300);
  key1.KeyPartCount = 1;
  AdgKeyTable key2 = myDS.NewKeyTable("RCSMASTL1");
  key2.Row["CSCUSTNO"] = Convert.ToDecimal(1400);
  key2.KeyPartCount = 1;
  dbFile.SeekRange(RangeMode.First, key1, RangeFirst.Include, key2, RangeLast.Include);

  /* Read until we go past record 1421. */
  bool EOF = false;
  decimal Total = 0;
  while(!EOF)
  {
      try
      {
          dbFile.ReadSequential(myDS, ReadSequentialMode.Next, LockRequest.NoWait);
          for (int j=1; j &lt;= 12; j++)
          {
              string number = j.ToString();
              if (number.Length &lt; 2)
                  number = "0" + number;
              Total += Convert.ToDecimal(myDS.ActiveRow["CSSALES" + number]); 
          }
      }
      catch(dgException dgEx)
      {
          if (dgEx.Error == dgErrorNumber.dgEaEOF)
              EOF = true;
          else
          {
              throw dgEx; //Throw exception if we didn't expect it.
          }
      }
  }
  MessageBox.Show("Total sales for customers 300 to 1400 totalled " 
      + Total.ToString() + ".", "Result");

  dbFile.Close();
  db.Clone();
```


### Example 11. SeekKey method example.

```cs 
  AdgConnection db = createAdgConnection("MyDatabaseName");
  FileAdapter dbFile = new FileAdapter(db, "*Libl/CMASTNEWL1", "CMMASTERL1");
  dbFile.AccessMode = AccessMode.Read;
  AdgDataSet myDS = null;
  dbFile.OpenNewAdgDataSet(out myDS);

  /* Seek the file pointer to just before Customer number 1500. */
  AdgKeyTable key = myDS.NewKeyTable("RCMMASTL1");
  key.Row["CMCustNo"] = Convert.ToDecimal(1500);
  dbFile.SeekKey(SeekMode.SetLL, key);
  /* We read the next record to get customer number 1500.*/
  dbFile.ReadSequential(myDS, ReadSequentialMode.Next, LockRequest.Default);
  string CustomerName1 = myDS.ActiveRow["CMName"].ToString();

  /* We set the file pointer to just after customer number 2000. */
  key.Row["CMCustNo"] = Convert.ToDecimal(2000);
  dbFile.SeekKey(SeekMode.SetGT, key);
  /* We read backwards one record to get customer number 2000. */
  dbFile.ReadSequential(myDS, ReadSequentialMode.Previous, LockRequest.Default);
  string CustomerName2 = myDS.ActiveRow["CMName"].ToString();

  /* We set the file pointer to greater than or equal to 2979. */
  key.Row["CMCustNo"] = Convert.ToDecimal(2979);
  dbFile.SeekKey(SeekMode.SetGE, key);
  /* Record 2979 usually does not exist, so we should be on record
  * 3000, which we read by reading the current record (using
  * SeekMode.SetLL would have gotten us record 2900). */
  dbFile.ReadSequential(myDS, ReadSequentialMode.Next, LockRequest.Default);
  string CustomerName3 = myDS.ActiveRow["CMName"].ToString();

  /* We set the file pointer to greater than or equal to 4000. */
  key.Row["CMCustNo"] = Convert.ToDecimal(4000);
  dbFile.SeekKey(SeekMode.SetGE, key);
  /* Record 4000 does exist, and by reading the next record we should access it. */
  dbFile.ReadSequential(myDS, ReadSequentialMode.Next, LockRequest.Default);
  string CustomerName4 = myDS.ActiveRow["CMName"].ToString();

  dbFile.Close();
  db.Close();
```


### Example 12. FileAdaptor ResetFormat method example.


```cs 
AdgConnection db = createAdgConnection("MyDatabaseName");
FileAdapter dbFile = new FileAdapter(db, "Examples/SalesMem", "SalesMem");
dbFile.AccessMode = AccessMode.Read;
AdgDataSet myDS = null;
dbFile.OpenNewAdgDataSet(out myDS);

/* Here we find the name of the customer whose sales (not counting returns) were
 * the best on average in January from 1998 to 2004. This example assumes
 * there are no customer numbers in the second format which are not found in the
 * first format, and that there are no years on record past 1998 to 2004.
 * We use the ResetFormat method to read from both formats, and
 * this gives us the ability to easy see the next customer's name before we
 * read their records. */

decimal total = 0;
decimal currentAverage = 0;
string currentName = "";
decimal maxAverage = -1;
string maxName = "";

dbFile.ResetFormat(); /* Read from both formats automatically. */
/* Make sure we start off on format 0. */
do{
    dbFile.ReadSequential(myDS,ReadSequentialMode.Next, LockRequest.Read);
  }while(dbFile.CurrentFormatIndex != 0);
try /* Read until end of file. Throw exception again if it was not due to EOF. */
    {
    while(true) /* Hitting end of file will throw an exception and let us leave. */
    {
/* Remember, the ActiveRow changes depending on the current format. */
        currentName = myDS.ActiveRow["CMName"].ToString();
        total = 0;
        dbFile.ReadSequential(myDS, ReadSequentialMode.Next, LockRequest.Read);
        while (dbFile.CurrentFormatIndex == 1)
        {
            total += Convert.ToDecimal(myDS.ActiveRow["CSSales01"]);
            dbFile.ReadSequential(myDS, ReadSequentialMode.Next, LockRequest.Read);
        }
/* there could be as many as seven records from 1998 - 2004. */
        currentAverage = total / 7;
        if (currentAverage &gt; maxAverage)
        {
            maxName = currentName;
            maxAverage = currentAverage;
        }
    }
}
catch(dgException dgEx)
{
    if (dgEx.Error != dgErrorNumber.dgEaEOF)
        throw dgEx;
}
string decimalResult = maxAverage.ToString();
decimalResult = decimalResult.Substring(0, decimalResult.IndexOf('.') + 3);
MessageBox.Show("The cusomter with the highest average sales in " +
    "January from 1998 - 2004 is \"" + maxName +
     "\", with an average of " + decimalResult + ".",
     "Result");
dbFile.Close();
db.Close();
```


### Example 13. FileAdaptor ReleaseCurrent method example.

```cs 
 /* Here, we are using a pre-initialized FileAdapter (named "dbFile")
  * which was opened using AccessMode.RWCD, which automatically locks
  * each read record read, so it will remain unchanged until we
  * update it or read a new record. Here we don't want to
  * update the record if the customer is not from Texas, and if
  * this code is being called by unknown client code it could be awhile
  * before the next read. In order to remove the lock without
  * performing some additional action, we use the ReleaseCurrent method . */
 dbFile.ReadSequential(myDS, ReadSequentialMode.Next, LockRequest.Default);
 if (myDS.ActiveRow["CMState"].ToString() == "TX" &amp;&amp;
     myDS.ActiveRow["CMActive"].ToString() == "0")
 {
     myDS.ActiveRow["CMActive"] = '1';
     dbFile.ChangeCurrent(myDS);
 }
 else
 {
     dbFile.ReleaseCurrent();
 }

```

### Example 14. FileAdaptor RecordCount property usage example.

```cs 
  AdgConnection db = createAdgConnection("MyDatabaseName");
  FileAdapter dbFile = new FileAdapter(db, "*Libl/CMASTNEWL1", "CMMASTERL1");
  dbFile.AccessMode = AccessMode.Read;
  AdgDataSet myDS = null;

  int refreshInterval = 10; //Used so we don't slow down refreshing too much...
  dbFile.OpenAttributes.BlockingFactor = refreshInterval;
  dbFile.OpenNewAdgDataSet(out myDS);

  /* Here, we read every record until end of file is reached.
   * Because this is an fairly long process, we set up a progress bar
   * to keep the user from being discouraged. We set its Maximum
   * value to the number of records in the file, which is found
   * using FileAdapter's RecordCount propert, divided by
   * our refreshInterval. */
  int recordsReadSinceLastRefresh = 0;
  prgBar.Minimum = 0;
  prgBar.Maximum = Convert.ToInt32(dbFile.RecordCount) / refreshInterval;

  bool EOF = false;
  while(!EOF)
  {
      try
      {
          /* Though it seems like we have to read each record one at a time,
           * in reality DG stores the first 10 records the first time we read
           * and then afterwards we simply read from the cache. When those run out, 
           * DG will automatically grab another ten records from the database.
           * Note that 10 is our refresh interval, meaning that this I/O operation
           * occurs at the same time that we update our progress bar. If the blocking
           * factor was higher than our refresh interval, not only would we have to 
           * wait longer to read the first record but the progress bar would go longer
           * without being updated. */
          dbFile.ReadSequential(myDS, ReadSequentialMode.Next, LockRequest.NoWait);
          /* Perform some action on each record here... */
          recordsReadSinceLastRefresh ++;
          if (recordsReadSinceLastRefresh == refreshInterval)
          {
              recordsReadSinceLastRefresh = 0;
              prgBar.PerformStep();
              this.Refresh(); //Refreshes the form.
          }
      }
      catch(dgException dgEx)
      {
          if (dgEx.Error == dgErrorNumber.dgEaEOF)
              EOF = true;
          else
          {
              //Exit procedure or end application here.
          }
      }
  }
  dbFile.Close();
  db.Close();
```


### Example 15. ReadSequential FileAdaptor method example.

```cs 
   AdgConnection db = createAdgConnection("MyDatabaseName");
   FileAdapter dbFile = new FileAdapter(db, "*Libl/CMASTNEWL1",
           "CMMASTERL1");
   dbFile.AccessMode = AccessMode.Read;
   AdgDataSet myDS = null;
   dbFile.OpenNewAdgDataSet(out myDS);

   /* Read the first record (in terms of Customer number, which CMASTNEWL1 is
    * keyed by.) */
   dbFile.ReadSequential(myDS, ReadSequentialMode.First, LockRequest.Default);
   string FirstCustomerName = myDS.ActiveRow["CMCustNo"].ToString();

   /* Seek the file pointer to just before Customer number 1500. */
   AdgKeyTable key = myDS.NewKeyTable("RCMMastL1");
   key.Row["CMCustNo"] = Convert.ToDecimal(1500);
   dbFile.SeekKey(SeekMode.SetLL, key);
   /* We read the next record to get customer number 1500.*/
   dbFile.ReadSequential(myDS, ReadSequentialMode.Next, LockRequest.Default);
   string OneThousandFiveHundrethCustomerName =
           myDS.ActiveRow["CMName"].ToString();
```


### Example 16. ReadSequentialEqual FileAdaptor method example.

```cs 
  AdgConnection db = createAdgConnection("MyDatabaseName");
  FileAdapter dbFile = new FileAdapter(db, "*Libl/CSMASTERL1", "CSMASTERL1");
  dbFile.AccessMode = AccessMode.Read;
  AdgDataSet myDS = null;
  dbFile.OpenNewAdgDataSet(out myDS);

  /* We read all of the records for customer 300 in order to get 
   * their net sales as well as their average yearly gross sales
   * and returns. */
  AdgKeyTable custNoKey = myDS.NewKeyTable("RCSMastL1");
  custNoKey.Row["CSCustNo"] = Convert.ToDecimal(300);
  custNoKey.KeyPartCount = 1; //Only use the first field of the key.
  decimal totalSales = 0;
  decimal totalReturns = 0;
  int saleRecordsRead = 0;
  int returnRecordsRead = 0;
  bool EOF = false;
  /* Because ReadSequentialEqual will return EOF if the record
   * it immediately gets is not equal to its search key, we need
   * to first seek to an equal record. */ 
  dbFile.SeekKey(SeekMode.SetLL, custNoKey);
  while(!EOF){
      try{
          dbFile.ReadSequentialEqual(myDS, ReadEqualMode.NextEqual, LockRequest.Read, custNoKey);
          if (Convert.ToDecimal(myDS.ActiveRow["CSType"]) == 1)
          {
              totalSales += Convert.ToDecimal(myDS.ActiveRow["CSSales01"]) + 
                  Convert.ToDecimal(myDS.ActiveRow["CSSales02"]) +
                  Convert.ToDecimal(myDS.ActiveRow["CSSales03"]) + 
                  Convert.ToDecimal(myDS.ActiveRow["CSSales04"]) +
                  Convert.ToDecimal(myDS.ActiveRow["CSSales05"]) + 
                  Convert.ToDecimal(myDS.ActiveRow["CSSales06"]) +
                  Convert.ToDecimal(myDS.ActiveRow["CSSales07"]) + 
                  Convert.ToDecimal(myDS.ActiveRow["CSSales08"]) +
                  Convert.ToDecimal(myDS.ActiveRow["CSSales09"]) + 
                  Convert.ToDecimal(myDS.ActiveRow["CSSales10"]) +
                  Convert.ToDecimal(myDS.ActiveRow["CSSales11"]) + 
                  Convert.ToDecimal(myDS.ActiveRow["CSSales12"]);
              saleRecordsRead ++;
          }
          else
          {
              totalReturns -= Convert.ToDecimal(myDS.ActiveRow["CSSales01"]) + 
                  Convert.ToDecimal(myDS.ActiveRow["CSSales02"]) +
                  Convert.ToDecimal(myDS.ActiveRow["CSSales03"]) + 
                  Convert.ToDecimal(myDS.ActiveRow["CSSales04"]) +
                  Convert.ToDecimal(myDS.ActiveRow["CSSales05"]) + 
                  Convert.ToDecimal(myDS.ActiveRow["CSSales06"]) +
                  Convert.ToDecimal(myDS.ActiveRow["CSSales07"]) + 
                  Convert.ToDecimal(myDS.ActiveRow["CSSales08"]) +
                  Convert.ToDecimal(myDS.ActiveRow["CSSales09"]) + 
                  Convert.ToDecimal(myDS.ActiveRow["CSSales10"]) +
                  Convert.ToDecimal(myDS.ActiveRow["CSSales11"]) + 
                  Convert.ToDecimal(myDS.ActiveRow["CSSales12"]);
              returnRecordsRead ++;
          }
      }
      catch(dgException dgEx){
          if (dgEx.Error == dgErrorNumber.dgEaEOF)
          {
              EOF = true;
          }
          else
          {
              MessageBox.Show("Error getting next record for customer 300:" + 
                  dgEx.Message, "Error");
              //Exit procedure or end application here.
          }
      }
  }
  /* Compute additional results. */
  decimal netSales = totalSales - totalReturns;
  decimal averageSalesPerYear;
  if (saleRecordsRead &gt; 0)
      averageSalesPerYear = totalSales / saleRecordsRead;
  else
      averageSalesPerYear = 0;
  decimal averageReturnsPerYear;
  if (returnRecordsRead &gt; 0)
      averageReturnsPerYear = totalReturns / returnRecordsRead;
  else
      averageReturnsPerYear = 0;
  dbFile.Close();
  db.Close();

```

### Example 17. ReadRange FileAdaptor method example.

```cs 
  AdgConnection db = createAdgConnection("MyDatabaseName");
  FileAdapter dbFile = new FileAdapter(db, "*Libl/CMASTNEWL1", 
            "CMMASTERL1");
  dbFile.AccessMode = AccessMode.Read;

  AdgDataSet myDS = null;
  try
  {
      dbFile.OpenNewAdgDataSet(out myDS);
  }
  catch(dgException dgEx)
  {
      MessageBox.Show("Error opening file! " + 
            dgEx.Message, "Error");
      //Exit procedure or end application here.
  }

  /* We read all records with a customer number greater
   * than, but not equal to 10000 and less than or equal
   * to, 40000. */
  AdgKeyTable OneKey = myDS.NewKeyTable("RCMMastL1");
  OneKey.Row["CMCustNo"] = 10000;
  AdgKeyTable TwoKey = myDS.NewKeyTable("RCMMastL1");
  TwoKey.Row["CMCustNo"] = 40000;

  try
  {
      dbFile.ReadRange(myDS, RangeMode.First,
      LockRequest.Read, OneKey,
      RangeFirst.Exclude, TwoKey,
      RangeLast.Include);
  }
  catch(dgException dgEx)
  {
      MessageBox.Show("Error getting records 
            10000-40000 :" +
          dgEx.Message, "Error");
      //Exit procedure or end application here.
  }

  int totalSum = 0;
  int activeSum = 0;
  bool EOF = false;
  while(!EOF)
  {
      try
      {

            dbFile.ReadSequential(myDS, ReadSequentialMode.Next, 
            LockRequest.NoWait);
          if (Convert.ToChar(myDS.ActiveRow["CMActive"]).ToString() 
            == "1")
          activeSum ++;
          totalSum ++;
      }
      catch(dgException dgEx)
      {
          if (dgEx.Error == 
            dgErrorNumber.dgEaEOF)

            EOF = true;
          else
          {
 
            //Exit procedure or end application here.
          }
      }
  }

  string percent = Convert.ToDecimal((Convert.ToDecimal(activeSum)
      /Convert.ToDecimal(totalSum)) * 100).ToString();
  MessageBox.Show(percent.Substring(0, percent.IndexOf('.')) +
      "% of the customers sampled are active.");
  dbFile.Close();
  db.Close(); 
```


### Example 18. ReadRandomKey FileAdaptor method example.

```cs 
  AdgConnection db = createAdgConnection("MyDatabaseName");
  FileAdapter dbFile = new FileAdapter(db, "*Libl/CMASTNEWL1", "CMMASTERL1");
  dbFile.AccessMode = AccessMode.Read;
  AdgDataSet myDS = null;
  dbFile.OpenNewAdgDataSet(out myDS);
  /* We retrieve the record for customer number 92300. */
  AdgKeyTable keyTbl = myDS.NewKeyTable("RCMMASTL2");
  keyTbl.Row["CMCUSTNO"] = 92300;
  try
  {
      dbFile.ReadRandomKey(myDS, ReadRandomMode.Equal, LockRequest.Default, keyTbl);
  }
  catch(dgException dgEx)
  {
      MessageBox.Show("Error finding the record: " + dgEx.Message,
          dgEx.Error.ToString());
  }

  dbFile.Close();
  db.Close();
```


### Example 19. OpenSimpleQuery FileAdaptor method example.

```cs 
  AdgConnection db = createAdgConnection("MyDatabaseName");
  FileAdapter dbFile = new FileAdapter(db, "*Libl/CMASTNEWL1", "CMMASTERL1");
  dbFile.AccessMode = AccessMode.Read; 
  AdgDataSet myDS = null;

  string[] keys = new string[]{"CMCUSTNO"};
  KeyUsages[] usages = new KeyUsages[]{KeyUsages.ASCEND};

  /* Read the first customer name listed for Texas. */
  dbFile.OpenSimpleQuery(ref myDS, "*UNIQUE", "CMSTATE=\"TX\"", keys, usages);
  dbFile.ReadSequential(myDS, ReadSequentialMode.First, LockRequest.Read);
  string FirstInTexas = myDS.ActiveRow["CMName"].ToString();
  /* First close the file to avoid throwing an exception... */
  dbFile.Close();
  /* Read the first customer name listed in Tennessee. */ 
  dbFile.OpenSimpleQuery(ref myDS, "*UNIQUE", "CMSTATE=\"TN\"", keys, usages);
  dbFile.ReadSequential(myDS, ReadSequentialMode.First, LockRequest.Read);
  string FirstInTennessee = myDS.ActiveRow["CMName"].ToString();

  dbFile.Close();
  db.Close();

```

### Example 20. OpenNewAdgDataSet FileAdaptor method example.

```cs 
  AdgConnection db = createAdgConnection("MyDatabaseName");
  FileAdapter dbFile = new FileAdapter(db, "*Libl/CMASTNEWL1", "CMMASTERL1");
  dbFile.AccessMode = AccessMode.Read;

  /* The AdgDataSet consists of data read from the database file
   * using the FileAdapter class. It also must be used in most
   * of the FileAdapter's operations. */
  AdgDataSet myDS = null;
  try
  {
      dbFile.OpenNewAdgDataSet(out myDS);
  }
  catch(dgException dgEx)
  {
      /* There are many reasons why opening a file can fail. Here, we
       * catch some of the more general ones. */
      if (dgEx.Error == dgErrorNumber.dgEmMNOTFND)
          MessageBox.Show("Member " + dbFile.MemberName + " not found!", "Error opening file");
      else if (dgEx.Error == dgErrorNumber.dgEmFNOTFND)
          MessageBox.Show("File " + dbFile.FileName + " not found!", "Error opening file");
      else
          MessageBox.Show(dgEx.Message, "Error opening file");
      //Exit procedure here.
  }

  /* The code below finds the names of every data field in the 
   * file "*Libl/CMASTNEWL1" and puts them into an array list. */
  ArrayList fieldNames = new ArrayList();

  for (int i = 0; i &lt; myDS.Formats; i ++)
  {
      foreach(DataColumn column in myDS.Tables[i].Columns)
      {
          fieldNames.Add(column.ToString());
      }
  } 

  dbFile.Close();
  db.Close();
```

### Example 20. Open FileAdaptor method example.

```cs 
  /* Unlike OpenNewAdgDataSet, the Open method does not create
   * a new AdgDataSet to meet the requirements of the file being
   * opened. However, it is slightly faster because of this, so
   * Open is a preferable way to open a file if a suitable.
   * AdgDataSet already exists or you don't need one. 
   * Note, however, that opening a file is a relatively slow
   * operation and the need to reopen a file rarely occurs. */

  FileAdapter dbFile = new FileAdapter();
  dbFile.SetConnection( createAdgConnection("MyDatabaseName") );
  dbFile.FileName = "*Libl/CMASTNEW";
  dbFile.MemberName = "CMMASTER";
  AdgDataSet myDS = null;

  /* Only need to open the file to show the number of records,
   * then we're through with it. */
  dbFile.Open(myDS); /* Will not initialize the data set. */

  MessageBox.Show("Number of deleted and non-deleted records still " +
      "taking up space in file \"" + dbFile.FileName +
      "\" is " + dbFile.FileLength.ToString());
  dbFile.Close();
  dbFile.Connection.Close();

```

### Example 21. OpenAttributes property example.

```cs 
  AdgConnection db = createAdgConnection("MyDatabaseName");
  FileAdapter dbFile = new FileAdapter(db, "*Libl/CMASTNEWL1", "CMMASTERL1");
  dbFile.AccessMode = AccessMode.Read;
  AdgDataSet myDS = null;

  int refreshInterval = 10; //Used so we don't slow down refreshing too much...
  dbFile.OpenAttributes.BlockingFactor = refreshInterval;
  dbFile.OpenNewAdgDataSet(out myDS);

  /* Here, we read every record until end of file is reached.
   * Because this is an fairly long process, we set up a progress bar
   * to keep the user from being discouraged. We set its Maximum
   * value to the number of records in the file, which is found
   * using FileAdapter's RecordCount property, divided by
   * our refreshInterval. */
  int recordsReadSinceLastRefresh = 0;
  prgBar.Minimum = 0;
  prgBar.Maximum = Convert.ToInt32(dbFile.RecordCount) / refreshInterval;

  bool EOF = false;
  while(!EOF)
  { 
      try
      {
          /* Though it seems like we have to read each record one at a time,
           * in reality DG stores the first 10 records the first time we read
           * and then afterwards we simply read from the cache. When those run out, 
           * DG will automatically grab another ten records from the database.
           * Note that 10 is our refresh interval, meaning that this I/O operation
           * occurs at the same time that we update our progress bar. If the blocking
           * factor was higher than our refresh interval, not only would we have to 
           * wait longer to read the first record but the progress bar would go longer
           * without being updated. */
          dbFile.ReadSequential(myDS, ReadSequentialMode.Next, LockRequest.NoWait);
          /* Perform some action on each record here... */
          recordsReadSinceLastRefresh ++;
          if (recordsReadSinceLastRefresh == refreshInterval)
          {
              recordsReadSinceLastRefresh = 0;
              prgBar.PerformStep();
              this.Refresh(); //Refreshes the form.
          }
      }
      catch(dgException dgEx)
      {
          if (dgEx.Error == dgErrorNumber.dgEaEOF)
              EOF = true;
          else
          {
              //Exit procedure or end application here.
          }
      }
  }
  dbFile.Close();
  db.Close();
```

### Example 21. MemberName property example.

```cs 
  /* We attempt to open the class variable FileAdapter "dbFile" 
   * which may or may not have been initialized another routine. */
  public void OpenFile(){
      AdgDataSet myDS = null;
      if (dbFile == null)
      {
          MessageBox.Show("FileAdapter not initialized.");
          return;
      }
      try
      {
          dbFile.OpenNewAdgDataSet(out myDS);
      }
      catch(dgException dgEx)
      {
          if (dgEx.Error == dgErrorNumber.dgEmMNOTFND)
          {
              MessageBox.Show("Member " + dbFile.MemberName + " not found!");
          }
          else if (dgEx.Error == dgErrorNumber.dgEmFNOTFND)
          {
              MessageBox.Show("File " + dbFile.FileName + " not found!");
          }
          else 
          {
              MessageBox.Show("Couldn't open file!" + dgEx.Message, "");
          } 
          // Exit routine or end application here.
      }
  }
 
```


### Example 23. GetPrintProperties method example.


```cs 
  /* Will open up "CustReport" and will write a single detail, and
   * change its background color. */
  AdgConnection dataBase = createAdgConnection("MyDatabaseName");
  FileAdapter printFile = new FileAdapter(dataBase, "*Libl/CustReport", "*First");
  printFile.AccessMode = AccessMode.PrintPreview;
  AdgDataSet dataSet;
  printFile.OpenNewAdgDataSet(out dataSet);

  DataRow dr = dataSet.PrepareRow("rptDetail");
  dr["prtCMName"] = "This line is light blue.";

  IPrintProperties ip = printFile.GetPrintProperties("rptDetail");
  int oleColor = ColorTranslator.ToOle(Color.LightBlue);
  ip.SetValue("lblRowColor", "BackColor", oleColor);

  dataSet.AddRow("rptDetail");
  printFile.SetFormat("rptDetail");
  printFile.AddRecord(dataSet);

  printFile.Close(); /* Shows print preview - can also accomplish this with
                      * ForceEOD, which doesn't close the file. */
  dataBase.Close();
```

### Example 24. FileAdapter FileName property example.

```cs 
  /* In this simple routine we wish to write the format names 
   * of a file to a combo box using the FileAdapter "dbFile" 
   * and its accompanying AdgDataSet "myDS", which may or 
   * may not have been initialized and opened elsewhere. */
  if (dbFile == null)
  {
      MessageBox.Show("Error- FileAdapter not initialized.");
      return;
  }
  if (dbFile.Status != FileAdapter.AdapterStatus.Open)
  {
      MessageBox.Show("Error- "+ dbFile.FileName + " not open.");
      return;
  }
  if (myDS == null)
  {
      MessageBox.Show("DataSet not initialized!");
      return;
  }

  for (int i = 0; i &lt; myDS.Formats; i ++)
  {
      /* List the format names in the combo box "cbFmtNames". */
      cbFmtNames.Items.Add(myDS.GetFormatName(i));
  }

```


### Example 24. FileAdapter FileLength property example.

```cs 
  FileAdapter dbFile = new FileAdapter();
  dbFile.SetConnection( createAdgConnection("MyDatabaseName") );
  dbFile.FileName = "*Libl/CMASTNEW";
  dbFile.MemberName = "CMMASTER";
  AdgDataSet myDS = null;
  dbFile.Open(myDS); /* Will not initialize the data set. */

  /* Figure out the number of records which were logically 
   * deleted but are still taking up space on the physical file.
   * FileLength returns the number of deleted and non-deleted 
   * records stored on a physical file, while RecordCount returns
   * the number of non-deleted records only. */
  long deletedRecords = dbFile.FileLength - dbFile.RecordCount;
  MessageBox.Show("Number of deleted records still taking up space in file \"" 
      + dbFile.FileName + "\" is " + deletedRecords.ToString());
  dbFile.Close();
  dbFile.Connection.Close();
```

### Example 25. Specifying FileName and MemberName properties after FileAdapter gets instanced.

```cs 
  AdgConnection dataBase = createAdgConnection("MyDatabaseName");
  FileAdapter dbFile = new FileAdapter(dataBase);
  dbFile.FileName = "*Libl/CMASTNEWL1";
  dbFile.MemberName = "CMMASTERL1";
```

### Example 25. Specifying Connection property after FileAdapter gets instanced.

```cs 
  AdgConnection dataBase = createAdgConnection("MyDatabaseName");
  FileAdapter dbFile = new FileAdapter();
  dbFile.SetConnection( dataBase;
  dbFile.FileName = "*Libl/CMASTNEWL1";
  dbFile.MemberName = "CMMASTERL1";
```

### Example 26. FileAdapter.ExactSeek Property usage example.

```cs 
  AdgConnection db = createAdgConnection("MyDatabaseName");
  using (FileAdapter dbFile = new FileAdapter(db, "*Libl/CMASTNEWL1", "CMMASTERL1"))
  {
      dbFile.AccessMode = AccessMode.Read;
      AdgDataSet myDS = null;
      dbFile.OpenNewAdgDataSet(out myDS);

      /* Seek the file pointer to just before Customer number 3000. */
      AdgKeyTable key = myDS.NewKeyTable("RCMMastL1");
      key.Row["CMCustNo"] = Convert.ToDecimal(3000);
      dbFile.SeekKey(SeekMode.SetGE, key);
      /* We check to see if we matched 3000 or if we went beyond it. */
      if (dbFile.ExactSeek)
          MessageBox.Show("Record 3000 exists.");
      else
          MessageBox.Show("Record 3000 not found.");
      /* Now we try to find Customer number 1125. */
      key.Row["CMCustNo"] = Convert.ToDecimal(1125);
      dbFile.SeekKey(SeekMode.SetGE, key);
      if (dbFile.ExactSeek)
          MessageBox.Show("Record 1125 exists.");
      else
          MessageBox.Show("Record 1125 not found.");
  }//Using statement automatically closes dbFile.
  db.Close();
```

### Example 26. DeleteRange method example.

```cs 
  AdgConnection db = createAdgConnection("MyDatabaseName");
  FileAdapter dbFile = new FileAdapter(db, "*Libl/CMASTNEWL1", "CMMASTERL1");
  dbFile.AccessMode = AccessMode.Delete | AccessMode.Read;

  AdgDataSet myDS = null;
  try
  {
      dbFile.OpenNewAdgDataSet(out myDS);
  }
  catch(dgException dgEx)
  {
      MessageBox.Show("Error opening file! " + dgEx.Message, "Error");
      //Exit procedure or end application here.
  }

  /* We erase all records with a customer number equal to
   * or greater than 5000 and less than, but not
   * equal to, 6000. */
  AdgKeyTable OneKey = myDS.NewKeyTable("RCMMastL1");
  OneKey.Row["CMCustNo"] = 5000;
  AdgKeyTable TwoKey = myDS.NewKeyTable("RCMMastL1");
  TwoKey.Row["CMCustNo"] = 6000;
  try
  {
      dbFile.DeleteRange(OneKey, RangeFirst.Include, TwoKey, RangeLast.Exclude);
  }
  catch(dgException dgEx)
  {
      MessageBox.Show("Error deleting records 5000-6000 :" +
          dgEx.Message, "Error");
  }

  dbFile.Close();
  db.Close();
```

### Example 27. DeleteKey method example.

```cs 
  AdgConnection db = createAdgConnection("MyDatabaseName");
  FileAdapter dbFile = new FileAdapter(db, "*Libl/CMASTNEWL1", "CMMASTERL1");
  /* Open a file for reading and deleting- this allows us to delete a record by its key value. */
  dbFile.AccessMode = AccessMode.Delete | AccessMode.Read;

  AdgDataSet myDS = null;
  try
  {
      dbFile.OpenNewAdgDataSet(out myDS);
  }
  catch(dgException dgEx)
  {
      MessageBox.Show("Error opening file! " + dgEx.Message, "Error");
      //Exit procedure or end application here.
  }

  /* We retrieve the record for customer number 82900 and delete it! */
  AdgKeyTable keyTbl = myDS.NewKeyTable("RCMMASTL1");
  keyTbl.Row["CMCustNo"] = 82900;
  dbFile.DeleteKey(keyTbl);

  dbFile.Close();
  db.Close();
```

### Example 28. DeleteCurrent method example.

```cs 
  AdgConnection db = createAdgConnection("MyDatabaseName");
  FileAdapter dbFile = new FileAdapter(db, "*Libl/CMASTNEWL1", "CMMASTERL1");
  dbFile.AccessMode = AccessMode.Read | AccessMode.Delete;

  AdgDataSet myDS = null;
  try
  {
      dbFile.OpenNewAdgDataSet(out myDS);
  }
  catch(dgException dgEx)
  {
      MessageBox.Show("Error opening file! " + dgEx.Message, "Error");
      //Exit procedure or end application here.
  }

  dbFile.ReadSequential(myDS, ReadSequentialMode.First, LockRequest.Default);

  /* We retrieve the record for customer number 7800... */
  AdgKeyTable keyTbl = myDS.NewKeyTable("RCMMASTL1");
  keyTbl.Row["CMCUSTNO"] = 7800;
  try
  {
      dbFile.ReadRandomKey(myDS, ReadRandomMode.Equal, LockRequest.Default, keyTbl);
      /*... and delete it! */
      dbFile.DeleteCurrent();
  }
  catch(dgException dgEx)
  {
      MessageBox.Show("Error deleting the record: " + dgEx.Message,
      dgEx.Error.ToString());
  }

  dbFile.Close();
  db.Close();
```

### Example 29. DeleteAllRecords method example.

```cs 
  /* We open the file in order to delete all of its records. */
  AdgConnection db = createAdgConnection("MyDatabaseName");
  FileAdapter dbFile = new FileAdapter(db, "*Libl/CMASTNEW", "CMMASTER");
  dbFile.AccessMode = AccessMode.Delete;
  /* Its generally good practice to make sure you have an exclusive lock
   * on a file that you are deleting all of the records from, but some
   * databases do not require it. */
  dbFile.OpenAttributes.ShareTypes = ShareTypes.Exclusive;
  AdgDataSet myDS = null;

  try
  {
      dbFile.Open(myDS);
  }
  catch(dgException dgEx)
  {
      db.Close();
      if (dgEx.Error == dgErrorNumber.dgEmBUSYOBJ)
      {
          MessageBox.Show("Couldn't open the file for exclusive access.", "Error opening file.");
          //Exit routine or procedure here to avoid preceding file operations.
      }
      else 
          throw dgEx;
  }
  dbFile.DeleteAllRecords();
  
  dbFile.Close();
  db.Close();
```

### Example 30. Connection property example.

```cs 
  /* Initialize a new fileadapter. Since the AdgConnection is needed
   * only for this file adapter, it is created and destroyed using the
   * FileAdapter's Connection property. */
  FileAdapter dbFile = new FileAdapter();
  dbFile.SetConnection( createAdgConnection("MyDatabaseName") );
  dbFile.FileName = "*Libl/CMASTNEWL2";
  dbFile.MemberName = "CMMASTERL2";
  dbFile.AccessMode = AccessMode.Read;

  AdgDataSet myDS = null;
  dbFile.OpenNewAdgDataSet(out myDS);

  /* Find first record beginning with M. */
  AdgKeyTable keyTbl = myDS.NewKeyTable("RCMMASTL2");
  keyTbl.Row["CMName"] = "M";
  dbFile.SeekKey(SeekMode.SetLL, keyTbl);

  dbFile.ReadSequential(myDS, ReadSequentialMode.Next, LockRequest.Read);
  string firstMCustomer = myDS.ActiveRow["CMName"].ToString();

  dbFile.Close(); /* Close file. */
  dbFile.Connection.Close(); /* Close database. */
```

### Example 31. Close method example.

```cs 
  AdgConnection db = createAdgConnection("MyDatabaseName");
  FileAdapter dbFile = new FileAdapter(db, "*Libl/CMASTNEWL1", "CMMASTERL1");
  dbFile.AccessMode = AccessMode.Read;
  AdgDataSet myDS = null;

  /* Though all open files will automatically be closed when a process
   * is terminated, it is good practice to close them as soon as you are
   * finished with them. You also may need to close a file in order
   * to reopen it with different attributes or to open it as a query file. */

  /* Read the first customer name listed for Texas. */
  string[] keys = new string[]{"CMCUSTNO"}; //The key fields used in our query.
  KeyUsages[] usages = new KeyUsages[]{KeyUsages.ASCEND}; //How we use them.

  dbFile.OpenSimpleQuery(ref myDS, "*UNIQUE", "CMSTATE=\"TX\"", keys, usages);
  dbFile.ReadSequential(myDS, ReadSequentialMode.First, LockRequest.Read);
  string FirstInTexas = myDS.ActiveRow["CMName"].ToString();

  /* Going to try a new query- first we close the file to avoid 
   * throwing an exception... */
  dbFile.Close();
  /* Read the first customer name listed in Tennessee. */ 
  dbFile.OpenSimpleQuery(ref myDS, "*UNIQUE", "CMSTATE=\"TN\"", keys, usages);
  dbFile.ReadSequential(myDS, ReadSequentialMode.First, LockRequest.Read);
  string FirstInTennessee = myDS.ActiveRow["CMName"].ToString();

  dbFile.Close();
  db.Close();
```

### Example 32. ChangeCurrent method example.

```cs 
  AdgConnection db = createAdgConnection("MyDatabaseName");
  FileAdapter dbFile = new FileAdapter(db, "*Libl/CMASTNEWL1", "CMMASTERL1");
  dbFile.AccessMode = AccessMode.Read | AccessMode.Change;

  AdgDataSet myDS = null;
  try
  {
      dbFile.OpenNewAdgDataSet(out myDS);
  }
  catch(dgException dgEx)
  {
      MessageBox.Show("Error opening file! " + dgEx.Message, "Error");
      //Exit procedure or end application here.
  }
  /* We read the first record of the file... */
  dbFile.ReadSequential(myDS, ReadSequentialMode.First, LockRequest.Default);
  myDS.SetActive(myDS.GetFormatName(0), 0); 
  /* ...and make the customer name all caps. */
  string CustName = System.Convert.ToString(myDS.ActiveRow["CMName"]);
  CustName = CustName.ToUpper();
  myDS.ActiveRow["CMName"] = CustName;
  try
  {
      /* Here we update the record. */
      dbFile.ChangeCurrent(myDS);
  }
  catch (dgException dgEx)
  {
      MessageBox.Show("Error updating record: " + dgEx.Message, "Error.");
      // Exit routine or take alternative action here.
      test.Actual = "Catch occured.";
  }

  dbFile.Close();
  db.Close();
```

### Example 33. AddRecord method example.

```cs 
  AdgConnection db = createAdgConnection("MyDatabaseName");
  FileAdapter dbFile = new FileAdapter(db, "*Libl/CMASTNEWL1", 
            "CMMASTERL1");
  dbFile.AccessMode = AccessMode.RWCD;

  AdgDataSet myDS = null;
  try
  {
     db.Open();
     dbFile.OpenNewAdgDataSet(out myDS);
  }
  catch(dgException dgEx)
  {
     MessageBox.Show("Error opening file! " + dgEx.Message, 
            "Error");
     //Exit procedure or end application here.
  }

  DataRow newRow = myDS.PrepareRow(0);
  newRow["CMCustNo"] = 50;
  newRow["CMName"] = "Amalgamated Software of North America";
  newRow["CMAddr1"] = "IH-10 West";
  newRow["CMCity"] = "San Antonio";
  newRow["CMState"] = "TX";
  newRow["CMCntry"] = "US";
  newRow["CMPostCode"] = "78230";
  newRow["CMActive"] = "1";
  newRow["CMFax"] = "2105554679";
  newRow["CMPhone"] = "555-4678";
  myDS.AddPreparedRowAndSetActive(0);
  try
  {
     dbFile.AddRecord(myDS);
  }
  catch (dgException dgEx)
  {
     MessageBox.Show("Adding new record was unsuccessful! "
        + dgEx.Message, "Error!");
     //Exit procedure or end application here.
  }
```

### Example 34. FileAdapter AccessMode property example.

```cs 
  FileAdapter dbFile = new FileAdapter();
  dbFile.SetConnection( createAdgConnection("MyDatabaseName") );
  dbFile.FileName = "*Libl/CMASTNEWL1";
  dbFile.MemberName = "CMMASTERL1";

  /* Open a file for reading and deleting- this allows us to delete a record by its key value. */
  dbFile.AccessMode = AccessMode.Read | AccessMode.Delete;
  AdgDataSet myDS = null;
  dbFile.OpenNewAdgDataSet(out myDS);

  /* We retrieve the record for customer number 82900 and delete it! */
  AdgKeyTable keyTbl = myDS.NewKeyTable("RCMMASTL1");
  keyTbl.Row["CMCustNo"] = 82900m;
  try
  {
      dbFile.DeleteKey(keyTbl);
  }
  catch(dgException dgEx)
  {
      if (dgEx.Error == dgErrorNumber.dgEaNOTFND)
      {
          MessageBox.Show("Record not found. ");
      }
  }
  dbFile.Close();
  dbFile.Connection.Close();
```

