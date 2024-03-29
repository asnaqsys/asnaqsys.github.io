---
title: FileAdapter.ReadSequential Method

---

Read a single record from the file in sequential order.

```cs
 public void ReadSequential(
   AdgDataSet ds,
   ReadSequentialMode mode,
   LockRequest lr
);
```

## Parameters



 *ds* 

: The DataSet object ([AdgDataSet](adg-dataset-class.html)) to which a 
						single record will be added. 

 *mode* 

: [ReadSequentialMode](read-sequential-mode-enumeration.html).  
								Specifies the manner in which the record is to be located, relative to the 
								current position in the file (Current, Next, Previous) or at the beginning or 
								end of the file (First, Last). 

 *lr* 

: [LockRequest](lock-request-enumeration.html).  Specifies how 
										the record read is to be locked.
									


## Exceptions



| Exception Type | Condition |
| ---- | ---- |
| NullReferenceException | FileAdapter [open](file-adapter-class-open-method.html) method has not been called (file is not open). |
| dgException | See table below. |



ASNA.DataGate.Common.dgException is thrown to signal normal procedural conditions, in addition to error conditions. The following table summarizes these conditions, and the corresponding value of the dgException.Error property.
<br />



| Value of dgException.Error | Condition |
| ---- | ---- |
| dgEaEOF | The record access operation resulted in an end-of-file condition. This exception also occurs when the record access operation would place the current file position outside of the boundaries established by a prior **ReadRange** or **SeekRange** method call. |
| dgEaNOTFND | The record to be accessed was not found. It may have been deleted, it may never have existed, or the key may have been changed. |
| dgEaBUSYREC | Record is in use or locked by another process. You cannot access the requested record because it is being used by another database process. Certain DataGate providers may provide further details of the conflicting process in the Message and Text members of dgException. |



## Remarks

Reads a single record based on the file's access path, current position, and a read *mode* indicator. The *mode* parameter determines whether a record adjacent to the current record is read (Current, Next, Previous), or the first or last record in the file is read (First, Last). 

**ReadSequential** is subject to the restrictions of "range mode". Calls to the [ReadRange](file-adapter-class-read-range-method.html) or [SeekRange](file-adapter-class-seek-range-method.html) methods will restrict the records accessible to subsequent sequential access methods, including **ReadSequential** . If **ReadSequential** would otherwise return a record containing a key which falls outside of the current range, dgException will be thrown with an Error property value of dgEaEOF.

If the operation is successful, the record read is placed in the specified **AdgDataSet** object. The record is appended to a DataTable in the **AdgDataSet** corresponding to the record format. The record is appended as a DataRow object in the DataTable, and the [AdgDataSet.ActiveRow](adg-dataset-class-active-row-property.html) property will reference this DataRow on return. If the operation is unsuccessful, no record is appended to the table, and an exception is thrown.

A successful read operation optionally locks the record read as directed by the *lr* parameter and the locking properties of the file. 
## Examples


```cs 
   AdgConnection db = new AdgConnection("*Public/DG NET Local");
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

## Requirements

**Namespace:** [ASNA.DataGate.Client](datagate-client-namespace.html) 

**Assembly:** ASNA DataGate Client

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
## See Also


[FileAdapter Class](file-adapter-class.html)
      <br />
[FileAdapter Class Members](file-adapter-members.html)
      <br />
[ReadRange Method](file-adapter-class-read-range-method.html)
      <br />
[SeekRange Method](file-adapter-class-seek-range-method.html)
      <br />
[Open Method](file-adapter-class-open-method.html)
      <br />
[AdgDataSet Class](adg-dataset-class.html)
      <br />
[ActiveRow Property](adg-dataset-class-active-row-property.html)
      <br />
[ReadSequentialMode Enumeration](read-sequential-mode-enumeration.html)
      <br />
[LockRequest Enumeration](lock-request-enumeration.html)
      <br />
[ASNA.DataGate.Client Namespace](datagate-client-namespace.html)

---

