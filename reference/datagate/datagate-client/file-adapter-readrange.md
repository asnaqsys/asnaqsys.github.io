---
title: "FileAdapter.ReadRange Method"
description: "Reads a range of records from the file that the FileAdapter is working with using the specified keys."
---
## Definition

**Namespace:** ASNA.DataGate.Client  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Establishes a range of records and reads the first one in the range.

This method is useful for reading a specific range of records from a file, starting at a given index and reading a specified number of records. It is commonly used when you need to process a subset of data, such as paginated results or batch operations.

```cs
void ReadRange(AdgDataSet ds, RangeMode mode, LockRequest lr, 
               AdgKeyTable firstKey, RangeFirst rangeFirst, 
               AdgKeyTable lastKey, RangeLast rangeLast)
```

#### Parameters

| Type | Parameter name | Description |
| --- | --- | --- |
| [AdgDataSet](/reference/datagate/datagate-client/adg-data-set.html) | ds | The AdgDataSet to fill with the data from the records. |
| [RangeMode](/reference/datagate/datagate-common/range-mode.html) | mode | The RangeMode to use when reading the records. |
| [LockRequest](/reference/datagate/datagate-common/lock-request.html) | lr | The LockRequest to use when reading the records. |
| [AdgKeyTable](/reference/datagate/datagate-client/adg-key-table.html) | firstKey | The AdgKeyTable containing the key of the first record in the range to read. |
| [RangeFirst](/reference/datagate/datagate-common/range-first.html) | rangeFirst | The RangeFirst value indicating whether to include the first record in the read. |
| [AdgKeyTable](/reference/datagate/datagate-client/adg-key-table.html) | lastKey | The AdgKeyTable containing the key of the last record in the range to read. |
| [RangeLast](/reference/datagate/datagate-common/range-last.html) | rangeLast | The RangeLast value indicating whether to include the last record in the read. |


## Example

```cs
    AdgConnection db = createAdgConnection("MyDatabaseName");
    FileAdapter dbFile = new FileAdapter(db, "*Libl/CMASTNEWL1", "CMMASTERL1");
    dbFile.AccessMode = AccessMode.Read;

    AdgDataSet myDS = null;
    try
    {
        dbFile.OpenNewAdgDataSet(out myDS);
    }
    catch(dgException dgEx)
    {
        Console.WriteLine("Error opening file! " dgEx.Message);
        //Exit procedure or end application here.
    }

    /* Read all records with a customer number greater than, but not equal to 10000 and less than or equal to, 40000. */
    AdgKeyTable OneKey = myDS.NewKeyTable("RCMMastL1");
    OneKey.Row["CMCustNo"] = 10000;
    AdgKeyTable TwoKey = myDS.NewKeyTable("RCMMastL1");
    TwoKey.Row["CMCustNo"] = 40000;

    try
    {
        dbFile.ReadRange(myDS, RangeMode.First, LockRequest.Read, 
                         OneKey, RangeFirst.Exclude, 
                         TwoKey, RangeLast.Include);
    }
    catch(dgException dgEx)
    {
        Console.WriteLine("Error getting records 10000-40000 :" + dgEx.Message);
        //Exit procedure or end application here.
    }

    decimal totalSum = 0;
    decimal activeSum = 0;
    bool EOF = false;
    while(!EOF)
    {
        try
        {
            dbFile.ReadSequential(myDS, ReadSequentialMode.Next, LockRequest.NoWait);
            if (Convert.ToChar(myDS.ActiveRow["CMActive"]).ToString() == "1")
                activeSum ++;
            totalSum ++;
        }
        catch(dgException dgEx)
        {
            if (dgEx.Error == dgErrorNumber.dgEaEOF)
                EOF = true;
            else
                //Exit procedure or end application here.
        }
    }

    decimal percent = (activeSum/totalSum) * 100;
    Console.WriteLine($"{percent}% of the customers sampled are active.");
    dbFile.Close();
    db.Close(); 
```

## Remarks
 
The **ReadRange** and `SeekRange` methods initiate a "range mode" for accessing records from an open file.  Under this mode, subsequent **FileAdapter** sequential read methods (`ReadSequential`and `ReadSequentialEqual`) restrict access to only records with keys that fall in the range specified by the key parameters.  This mode allows DCS programs to more efficiently access a certain set records, especially when combined with the network record blocking feature (see `FileOpenAttr.BlockingFactor`).
 
The _firstKey_ and _lastKey_ parameters specify the range, along with the _rangeFirst_ and _rangeLast_ mode parameters.  If the _lastKey_ value specifies a key value which sorts prior to the _firstKey_ value, the range specifies an empty set of records.  Special values for the _rangeFirst_ and _rangeLast_ parameters allow the range to be extended to the beginning of the file (**RangeFirst.Top**) and the end of the file (**RangeLast.Bottom**).  When one of these values is specified, the corresponding key value parameter is ignored.
 
**ReadRange** reads the first or last record in the range, as specified by the mode parameter (**RangeMode.First** or **RangeMode.Last**, respectively).  If the range specifies an empty set of records, this method throws dgException with the Error property set to dgEaNOTFND.
 
If the operation is successful, the record read is placed in the specified **AdgDataSet** object.   The record is appended to a DataTable in the **AdgDataSet** corresponding to the record format.  The record is appended as a DataRow object in the DataTable, and the `AdgDataSet.ActiveRow` property will reference this DataRow on return.
 
A successful read operation optionally locks the record read as directed by the _lr_ parameter and the locking properties of the file.
 
Note that if **FileAdapter** was already in range mode, this method will cancel it and initiate a new range mode as specified.
 
Use the **ReadRange** method in conjunction with the `DeleteRange` method to optimize processing and to enhance client/server performance with all supported database engines with dynamic Network Blocking.


## See Also
- [FileAdapter class](file-adapter.html)
