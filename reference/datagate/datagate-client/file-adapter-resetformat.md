---
title: "FileAdapter.ResetFormat Method"
description: "Resets the format of the file that the FileAdapter is working with to the default format."
---

## Definition

**Namespace:** ASNA.DataGate.Client  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Resets the format of the file that the FileAdapter is working with to the default format.

```cs
public void ResetFormat()
```


## Example

```cs
    AdgConnection db = createAdgConnection("MyDatabaseName");
    FileAdapter dbFile = new FileAdapter(db, "Examples/Sales", "MemberX");
    dbFile.AccessMode = AccessMode.Read;
    AdgDataSet myDS = null;
    dbFile.OpenNewAdgDataSet(out myDS);

    /* Here we find the name of the customer whose sales (not counting returns) were
    * the best on average in January from 2018 to 2024. This example assumes
    * there are no customer numbers in the second format which are not found in the
    * first format, and that there are no years on record past 2018 to 2024.
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
    do {
        dbFile.ReadSequential(myDS,ReadSequentialMode.Next, LockRequest.Read);
    } while(dbFile.CurrentFormatIndex != 0);

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
            /* there could be as many as seven records from 2018 - 2024. */
            currentAverage = total / 7;
            if (currentAverage > maxAverage)
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
    Console.WriteLine($"Highest average January sales customer from 2018 - 2024 is '{maxName}', with an average of {maxAverage}.");
    dbFile.Close();
    db.Close();
```

## Remarks
 
By default, when reading multi-format files, records of all formats are accessible. The **SetFormat** method of **FileAdapter** can be used to restrict access to only records of a certain format. The **ResetFormat** method is used to return the access mode to the default, non-format specific behavior. It is commonly used in scenarios where you need to process records from different formats in sequence or switch back to the original format after custom processing.

## See Also
- [FileAdapter class](file-adapter.html)
