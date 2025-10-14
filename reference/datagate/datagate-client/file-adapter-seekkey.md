---
title: "FileAdapter.SeekKey Method"
description: "Positions the file pointer at the record with the specified key in the file that the FileAdapter is working with."
---

## Definition

**Namespace:** ASNA.DataGate.Client  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Positions the file pointer at the record with the specified key in the file that the FileAdapter is working with.

```cs
void SeekKey(SeekMode mode, AdgKeyTable keyTable)
```

#### Parameters

| Type | Parameter name | Description |
| --- | --- | --- |
| [SeekMode](/reference/datagate/datagate-common/seek-mode.html) | mode | The SeekMode to use when seeking the record. |
| [AdgKeyTable](/reference/datagate/datagate-client/adg-key-table.html) | keyTable | The AdgKeyTable containing the key of the record to seek. |

## Example

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
    * 3000, which we read by reading the current record. */
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

## Remarks

**SeekKey** positions the file pointer to a particular record using the specified _keyTable_ and _mode_ as a point of reference.  The record pointed to by **SeekKey** will contain a key value equal to, greater than or equal to, or greater than the specified _keyTable_ parameter, dependent on the value of the _mode_ parameter.  Optionally, the file pointer may be placed on the first or last record of the file, by specifying a _mode _value of **SeekMode.First** or **SeekMode.Last**, respectively.  If the record sought does not exist in the file, the method throws dgException with an Error property value of dgEaNOTFND.

When **SeekMode.SetLL** or **SeekMode.SetGT** values for _mode_ are specified and the record sought is not found, the file pointer is placed at the end of the file, and then dgException is thrown.

Calling this method cancels "range mode".  A prior successful call to **ReadRange** or **SeekRange** places the **FileAdapter** in range mode, in which only records with keys in a specified range are accessed. This method cancels the restriction.


## See Also
- [FileAdapter class](file-adapter.html)
