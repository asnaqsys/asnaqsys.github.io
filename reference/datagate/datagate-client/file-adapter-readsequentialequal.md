---
title: "FileAdapter.ReadSequentialEqual Method"
description: "Reads a record from the file that the FileAdapter is working with sequentially and equal to the specified key."
---

## Definition

**Namespace:** ASNA.DataGate.Client  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Reads a record from the file that the FileAdapter is working with sequentially and equal to the specified key.

```cs
public void ReadSequentialEqual(AdgDataSet ds, ReadEqualMode mode, LockRequest lr, AdgKeyTable keyTable)
```

#### Parameters

| Type | Parameter name | Description |
| --- | --- | --- |
| [AdgDataSet](/reference/datagate/datagate-client/adg-data-set.html) | ds | The AdgDataSet to fill with the data from the record. |
| [ReadEqualMode](/reference/datagate/datagate-common/read-equal-mode.html) | mode | The ReadEqualMode to use when reading the record. |
| [LockRequest](/reference/datagate/datagate-common/lock-request.html) | lr | The LockRequest to use when reading the record. |
| [AdgKeyTable](/reference/datagate/datagate-client/adg-key-table.html) | keyTable | The AdgKeyTable containing the key of the record to read. |

## Example
```cs
    AdgConnection db = createAdgConnection("MyDatabaseName");
    FileAdapter dbFile = new FileAdapter(db, "*Libl/CSMASTERL1", "CSMASTERL1");
    dbFile.AccessMode = AccessMode.Read;
    AdgDataSet myDS = null;
    dbFile.OpenNewAdgDataSet(out myDS);

    /* We read all of the records for customer 300 in order to get their sales */
    AdgKeyTable custNoKey = myDS.NewKeyTable("RCSMastL1");
    custNoKey.Row["CSCustNo"] = Convert.ToDecimal(300);
    custNoKey.KeyPartCount = 1; //Only use the first field of the key.
    decimal totalSales = 0;
    int saleRecordsRead = 0;
    bool EOF = false;
    /* Because ReadSequentialEqual will return EOF if the record it immediately gets is not equal to 
     * its search key, we need to first seek to an equal record. */ 
    dbFile.SeekKey(SeekMode.SetLL, custNoKey);
    while(!EOF) {
        try {
            dbFile.ReadSequentialEqual(myDS, ReadEqualMode.NextEqual, LockRequest.Read, custNoKey);
            if (Convert.ToDecimal(myDS.ActiveRow["CSType"]) == 1) {  // This is a Sales record
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
        }
        catch(dgException dgEx) {
            if (dgEx.Error == dgErrorNumber.dgEaEOF) {
                EOF = true;
            }
            else {
                Console.WriteLine ("Error getting next record for customer 300:" + dgEx.Message);
                //Exit procedure or end application here.
            }
        }
    }
    /* Compute additional results. */
    . . .
```

## Remarks

Reads a single record based on the file's access path, current record key value, and a read _mode_ indicator.  Optionally read a record with a key value equal to the specified key.  Also, the behavior of this method is influenced by **FileAdapter** "range mode" (see also `ReadRange` and `SeekRange`).

Commonly, the **ReadSequentialEqual** method is used to read a record adjacent to the current record that has the same key value as the current record.  To do this, specify the desired _mode_ parameter, and set the `KeyPartCount`property of the **AdgKeyTable** object passed in the key parameter to zero.

To use **ReadSequentialEqual** to read a record which contains a particular key value, specify the key value in the **AdgKeyTable** object passed in the _keyTable_ parameter.

**ReadSequentialEqual** is subject to the restrictions of "range mode".  Calls to the **ReadRange** or **SeekRange** methods will restrict the records accessible to subsequent sequential access methods, including **ReadSequentialEqual**.  If **ReadSequentialEqual** would otherwise return a record containing a key which falls outside of the current range, dgException will be thrown with an Error property value of dgEaEOF.

If the operation is successful, the record read is placed in the specified **AdgDataSet** object. The record is appended to a DataTable in the **AdgDataSet** corresponding to the record format. The record is appended as a DataRow object in the DataTable, and the `AdgDataSet.ActiveRow`property will reference this DataRow on return.  If the operation is unsuccessful, no record is appended to the table, and an exception is thrown.

A successful read operation optionally locks the record read as directed by the _lr_ parameter and the locking properties of the file.



## See Also
- [FileAdapter class](file-adapter.html)
