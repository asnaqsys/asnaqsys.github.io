---
title: "FileAdapter.ReadSequential Method"
description: "Reads a record from the file that the FileAdapter is working with sequentially."
---

## Definition

**Namespace:** ASNA.DataGate.Client  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Reads a record from the file that the FileAdapter is working with sequentially.

```cs
void ReadSequential(AdgDataSet ds, ReadSequentialMode mode), LockRequest lr)
```

#### Parameters

| Type | Parameter name | Description |
| --- | --- | --- |
| [AdgDataSet](/reference/datagate/datagate-client/adg-data-set.html) | ds | The AdgDataSet to fill with the data from the record. |
| [ReadSequentialMode](/reference/datagate/datagate-common/read-sequential-mode.html) | mode | The ReadSequentialMode to use when reading the record. |
| [LockRequest](/reference/datagate/datagate-common/lock-request.html) | lr | The LockRequest to use when reading the record. |


## Example

```cs
   AdgConnection db = createAdgConnection("MyDatabaseName");
   FileAdapter dbFile = new FileAdapter(db, "*Libl/CMASTNEWL1", "CMMASTERL1");
   dbFile.AccessMode = AccessMode.Read;
   AdgDataSet myDS = null;
   dbFile.OpenNewAdgDataSet(out myDS);

   /* Read the first record (in terms of Customer number, which CMASTNEWL1 is keyed by.) */
   dbFile.ReadSequential(myDS, ReadSequentialMode.First, LockRequest.Default);
   string FirstCustomerName = myDS.ActiveRow["CMCustNo"].ToString();

   /* Seek the file pointer to just before Customer number 1500. */
   AdgKeyTable key = myDS.NewKeyTable("RCMMastL1");
   key.Row["CMCustNo"] = Convert.ToDecimal(1500);
   dbFile.SeekKey(SeekMode.SetLL, key);
   /* We read the next record to get customer number 1500.*/
   dbFile.ReadSequential(myDS, ReadSequentialMode.Next, LockRequest.Default);
   string OneThousandFiveHundrethCustomerName = myDS.ActiveRow["CMName"].ToString();
```

## Remarks

Reads a single record based on the file's access path, current position, and a read _mode_ indicator. The _mode_ parameter determines whether a record adjacent to the current record is read (Current, Next, Previous), or the first or last record in the file is read (First, Last). This method is commonly used to iterate through records in a file, either forward or backward, depending on the mode specified

**ReadSequential** is subject to the restrictions of "range mode". Calls to the `ReadRange`or `SeekRange` methods will restrict the records accessible to subsequent sequential access methods, including **ReadSequential**.  If **ReadSequential** would otherwise return a record containing a key which falls outside of the current range, dgException will be thrown with an Error property value of dgEaEOF.

If the operation is successful, the record read is placed in the specified **AdgDataSet** object. The record is appended to a DataTable in the **AdgDataSet** corresponding to the record format. The record is appended as a DataRow object in the DataTable, and the `AdgDataSet.ActiveRow`property will reference this DataRow on return. If the operation is unsuccessful, no record is appended to the table, and an exception is thrown.

A successful read operation optionally locks the record read as directed by the _lr_ parameter and the locking properties of the file.


## See Also
- [FileAdapter class](file-adapter.html)
