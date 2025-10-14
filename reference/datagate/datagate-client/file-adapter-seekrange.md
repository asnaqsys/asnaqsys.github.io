---
title: "FileAdapter.SeekRange Method"
description: "Positions the file pointer at the first record in the specified range in the file."
---

## Definition

**Namespace:** ASNA.DataGate.Client  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Positions the file pointer at the first record in the specified range in the file that the FileAdapter is working with.

```cs
void SeekRange([RangeMode mode, AdgKeyTable firstKey, RangeFirst rangeFirst, AdgKeyTable lastKey, RangeLast rangeLast)
```

#### Parameters

| Type | Parameter name | Description |
| --- | --- | --- |
| [RangeMode](/reference/datagate/datagate-common/range-mode.html) | mode | The SeekMode to use when seeking the record. |
| [AdgKeyTable](/reference/datagate/datagate-client/adg-key-table.html) | firstKey | The AdgKeyTable containing the key of the first record in the range to seek. |
| [RangeFirst](/reference/datagate/datagate-common/range-first.html) | rangeFirst | The RangeFirst value indicating whether to include the first record in the seek. |
| [AdgKeyTable](/reference/datagate/datagate-client/adg-key-table.html) | lastKey | The AdgKeyTable containing the key of the last record in the range to seek. |
| [RangeLast](/reference/datagate/datagate-common/range-last.html) | rangeLast | The RangeLast value indicating whether to include the last record in the seek. |


## Example
```cs
    AdgConnection db = createAdgConnection("MyDatabaseName");
    FileAdapter dbFile = new FileAdapter(db, "*Libl/CSMASTERL1", "CSMASTERL1");
    dbFile.AccessMode = AccessMode.Read;
    AdgDataSet myDS = null;
    dbFile.OpenNewAdgDataSet(out myDS);

    /* The code below will find all of the sales for all customers with a number from 300 to 1400, 
    * and read all the customer numbers from lowest to highest. */
    AdgKeyTable key1 = myDS.NewKeyTable("RCSMASTL1");
    key1.Row["CSCUSTNO"] = Convert.ToDecimal(300);
    key1.KeyPartCount = 1;
    AdgKeyTable key2 = myDS.NewKeyTable("RCSMASTL1");
    key2.Row["CSCUSTNO"] = Convert.ToDecimal(1400);
    key2.KeyPartCount = 1;
    dbFile.SeekRange(RangeMode.First, key1, RangeFirst.Include, key2, RangeLast.Include);

    /* Read until we go past record 1400. */
    bool EOF = false;
    decimal Total = 0;
    while(!EOF)
    {
        try
        {
            dbFile.ReadSequential(myDS, ReadSequentialMode.Next, LockRequest.NoWait);
            for (int j=1; j <= 12; j++)
            {
                string number = j.ToString();
                if (number.Length < 2)
                    number = "0" + number;
                Total += Convert.ToDecimal(myDS.ActiveRow["CSSALES" + number]); 
            }
        }
        catch(dgException dgEx)
        {
            if (dgEx.Error == dgErrorNumber.dgEaEOF)
                EOF = true;
            else
                throw dgEx; //Throw exception if we didn't expect it.
        }
    }
    Console.WriteLine ($"Total sales for customers 300 to 1400 totaled {Total}"); 
    dbFile.Close();
    db.Close();
```

## Remarks
 
The `ReadRange`and **SeekRange** methods initiate a "range mode" for accessing records from an open file.  Under this mode, subsequent **FileAdapter** sequential read methods (`ReadSequential`and `ReadSequentialEqual`) restrict access to only records with keys that fall in the range specified by the key parameters.  This mode allows programs to more efficiently access a certain set of records, especially when combined with the network record blocking feature (see `FileOpenAttr.BlockingFactor`).

The _firstKey_ and _lastKey_ parameters specify the range, along with the _rangeFirst_ and _rangeLast_ mode parameters.  If the _lastKey_ value specifies a key value which sorts prior to the _firstKey_ value, the range specifies an empty set of records.  Special values for the _rangeFirst_ and _rangeLast_ parameters allow the range to be extended to the beginning of the file (**RangeFirst.Top**) and the end of the file (**RangeLast.Bottom**).  When one of these values is specified, the corresponding key value parameter is ignored.

**SeekRange** positions the file cursor on the first or last record in the range, as specified by the _mode_ parameter (**RangeMode.First** or **RangeMode.Last**, respectively).  If the range specifies an empty set of records, this method throws dgException with the Error property set to dgEaNOTFND.

Note that if **FileAdapter** was already in range mode, this method will cancel it and initiate a new range mode as specified.

## See Also
- [FileAdapter class](file-adapter.html)
