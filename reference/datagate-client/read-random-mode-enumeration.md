---
title: ReadRandomMode Enumeration

---

Defines modes of operation for the [ FileAdapter.ReadRandomKey](file-adapter-class-read-random-key-method.html) and [ FileAdapter.ReadRandomRRN](file-adapter-class-read-random-rrn-method.html) methods.

```cs
 public enum ReadRandomMode;
```


## Remarks

The ReadRandomMode Enumeration&gt; enumeration is used as a parameter by the [ReadRandomKey](file-adapter-class-read-random-key-method.html) and [ReadRandomRRN](file-adapter-class-read-random-rrn-method.html) methods of the [FileAdapter](file-adapter-class.html) class. It defines operational modes for these methods as listed in the table below.

ReadRandomMode Enumeration defines values in which you can select one of the choices.
## Members



| Member | Description | Value |
| ---- | ---- | ---- |
| Equal | Find the first record with key (or RRN) equal to the search argument. | 13 |
| Greater | Find the first record with key (or RRN) greater than the Search argument. | 14 |
| GTEQ | Find the first record with key (or RRN) greater than or equal to the Search  									argument. | 15 |



## Examples


```cs 
  AdgConnection db = new AdgConnection("*Public/DG NET Local");
  FileAdapter dbFile = new FileAdapter(db, "*Libl/CMASTNEWL2", "CMMASTERL2");
  dbFile.AccessMode = AccessMode.RWCD;

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

  /* We retrieve the record for customer "Rand Of Distribix Fl Varnish"... */
  AdgKeyTable keyTbl = myDS.NewKeyTable("RCMMASTL2");
  keyTbl.Row["CMNAME"] = "Rand Of Distribix Fl Varnish";
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
[ReadRandomKey Method](file-adapter-class-read-random-key-method.html)
        <br />
      </span>
      <span>
[ReadRandomRRN Method](file-adapter-class-read-random-rrn-method.html)
      </span>

