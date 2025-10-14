---
title: "FileAdapter.ReadRandomKey Method"
description: "Reads a record from the file that the FileAdapter is working with using the specified key."
---

## Definition

**Namespace:** ASNA.DataGate.Client  
**Assembly:** ASNA.QSys.DataGate.Client.dll


Reads a record from the file that the FileAdapter is working with using the specified key.

```cs
void ReadRandomKey(AdgDataSet ds, ReadRandomMode mode, LockRequest lr, AdgKeyTable keyTable)
```

#### Parameters

| Type | Parameter name | Description |
| --- | --- | --- |
| [AdgDataSet](/reference/datagate/datagate-client/adg-data-set.html) | ds | The AdgDataSet to fill with the data from the record read. |
| [ReadRandomMode](/reference/datagate/datagate-common/read-random-mode.html) | mode | The ReadRandomMode to use when reading the record. |
| [LockRequest](/reference/datagate/datagate-common/lock-request.html) | lr | The LockRequest to use when reading the record. |
| [AdgKeyTable](/reference/datagate/datagate-client/adg-key-table.html) | keyTable | The AdgKeyTable containing the key of the record to read. |


## Example
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
        Console.Writeline("Error finding the record: " + dgEx.Message);
    }

    dbFile.Close();
    db.Close();
```

## Remarks
 
**ReadRandomKey** reads a database file record using the specified key and mode as a point of reference.  A record is read which contains a key value equal to, greater than or equal to, or greater than the specified _keyTable_ parameter, dependent on the value of the _mode_ parameter – Equal, GTEQ, or Greater, respectively.  If no such record exists in the file, the method throws dgException with an Error property value of dgEaNOTFND.
 
If the operation is successful, the record read is placed in the specified **AdgDataSet** object.  The record is appended to a DataTable in the **AdgDataSet** corresponding to the record format.  The record is appended as a DataRow object in the DataTable, and the `AdgDataSet.ActiveRow` property will reference this row on return.
 
A successful read operation optionally locks the record read as directed by the _lr_ parameter and the locking properties of the file.
 
Calling this method cancels "range mode". A prior successful call to `ReadRange` or `SeekRange` places the **FileAdapter** in range mode, in which only records with keys in a specified range are accessed.  This method cancels the restriction.

## See Also
- [FileAdapter class](file-adapter.html)
