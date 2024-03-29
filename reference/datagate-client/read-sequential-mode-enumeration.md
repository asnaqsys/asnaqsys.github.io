---
title: ReadSequentialMode Enumeration

---

Defines modes of operation for the [ FileAdapter.ReadSequential](file-adapter-class-read-sequential-method.html) method.

```cs
 public enum ReadSequentialMode;
```


## Remarks

The **ReadSequentialMode** enumeration is used as a parameter by the [ReadSequential](file-adapter-class-read-sequential-method.html) method of the [FileAdapter](file-adapter-class.html) class. It defines operational modes for this method, as listed in the table below.

**ReadSequentialMode** defines values in which you can select one of the choices.
## Members



| Member | Description | Value |
| ---- | ---- | ---- |
| Current | Read the current record. | 3 |
| First | Read the first record. | 5 |
| Last | Read the last record. | 6 |
| Next | Read the next record. | 1 |
| Previous | Read the previous record. | 2 |



## Examples


```cs 
  AdgConnection db = new AdgConnection("*Public/DG NET iSeries");
  FileAdapter dbFile = new FileAdapter(db, "*Libl/CMASTNEWL1", "CMMASTERL1");
  dbFile.AccessMode = AccessMode.ReadWrite; 
  AdgDataSet myDS = null;

  dbFile.OpenNewAdgDataSet(out myDS);
  /* We read the first customer for this file (customer number 100)-
   * the record is represented in myDS's active row property. */
  dbFile.ReadSequential(myDS, ReadSequentialMode.First, LockRequest.Read);

  /* We read the next customer for this file (customer number 200). */
  dbFile.ReadSequential(myDS, ReadSequentialMode.Next, LockRequest.Read);

  /* We read the last record in the file (should be customer number 100000). */
  dbFile.ReadSequential(myDS, ReadSequentialMode.Last, LockRequest.Read);

  /* We read the previous record (which gives us customer number 99900).
   * We also lock the record. */
  dbFile.ReadSequential(myDS, ReadSequentialMode.Previous, LockRequest.Write);

  /* We unlock the record so that other users can view or update it. */
  dbFile.ReleaseCurrent();

  /* ... Some time passes... */

  /* We lock the current record by reading it again. */
  dbFile.ReadSequential(myDS, ReadSequentialMode.Current, LockRequest.Write);

  /* Close this file and open a different one. */
  dbFile.Close();
  dbFile.FileName = "*Libl/CSMASTERL1";
  dbFile.MemberName = "CSMASTERL1";

  dbFile.OpenNewAdgDataSet(out myDS);

  /* We read randomly to find the record for customer number 500.
   * In this file, several records may have that customer number. */
  AdgKeyTable keyTbl = myDS.NewKeyTable("RCSMastL1"); //New file, so reinstantiate key table.
  keyTbl.Row["CSCustNo"] = 500;
  keyTbl.KeyPartCount = 1;
  dbFile.ReadRandomKey(myDS, ReadRandomMode.Equal, LockRequest.Read, keyTbl);

  /* Now we get customer number 80000 by setting the file pointer to
   * just past it and then reading backwards once. */
  keyTbl.Row["CSCUSTNO"] = 80000;
  dbFile.SeekKey(SeekMode.SetGT, keyTbl);
  dbFile.ReadSequential(myDS, ReadSequentialMode.Previous, LockRequest.Read);
  
```

## Requirements

**Namespace:** [ASNA.DataGate.Common](datagate-common-namespace.html) 

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10

**Assembly:** ASNA DataGate Client (in ASNA.DataGate.Client.dll)
## See Also


[ASNA.DataGate.Common Namespace](datagate-common-namespace.html)
      <br />
      <span>
[FileAdapter Class](file-adapter-class.html)
        <br />
      </span>
      <span>
[ReadSequential Method](file-adapter-class-read-sequential-method.html)
      </span>

