---
title: RangeMode Enumeration

---

For [FileAdapter](file-adapter-class.html) range methods, defines how to access the first record in the range.

```cs
 public enum RangeMode;
```


## Remarks

<span> **RangeMode** </span> is used as a parameter for the **FileAdapter** methods which establish a range: [ReadRange](file-adapter-class-read-range-method.html) and [SeekRange](file-adapter-class-seek-range-method.html). In addition to establishing the range, these methods position the file to one end of the range based on the value of <span> **RangeMode** </span>.

For <span> **ReadRange** </span>, **RangeMode** determines whether to read the first or last record in the range.

For <span> **SeekRange** </span>, **RangeMode** determines whether to locate the file cursor on the first or last record in the range.

<span> **RangeMode** </span> defines values in which you can select one of the choices.
## Members

<br />



| Member | Description | Value |
| ---- | ---- | ---- |
| First | The first record in a range to access. | 5 |
| Last | The last record in a range to access. | 6 |



## Examples


```cs 
  AdgConnection db = new AdgConnection("*Public/DG NET Local");
  FileAdapter dbFile = new FileAdapter(db, "*Libl/CMASTNEWL1", "CMMASTERL1");
  dbFile.AccessMode = AccessMode.Read;

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

  /* We read all records with a customer number greater
   * than, but not equal to 6000 and less than or equal
   * to, 7000. */
  AdgKeyTable OneKey = myDS.NewKeyTable("RCMMastL1");
  OneKey.Row["CMCustNo"] = 10000;
  AdgKeyTable TwoKey = myDS.NewKeyTable("RCMMastL1");
  TwoKey.Row["CMCustNo"] = 40000;

  try
  {
      dbFile.ReadRange(myDS, RangeMode.First, 
      LockRequest.Read, OneKey, 
      RangeFirst.Exclude, TwoKey,
      RangeLast.Include);
  }
  catch(dgException dgEx)
  {
      MessageBox.Show("Error getting records 10000-40000 :" +
          dgEx.Message, "Error");
      //Exit procedure or end application here.
  }

  int totalSum = 0;
  int activeSum = 0;
  bool EOF = false;
  while(!EOF)
  {
      try
      {
          dbFile.ReadSequential(myDS, ReadSequentialMode.Next, LockRequest.NoWait);
          if (Convert.ToChar(myDS.ActiveRow["CMActive"]) == '1')
              activeSum ++;
          totalSum ++;
      }
      catch(dgException dgEx)
      {
          if (dgEx.Error == dgErrorNumber.dgEaEOF)
              EOF = true;
          else
          {
              //Exit procedure or end application here.
          }
      }
  }
  if (totalSum &gt; 0)
  {
      string percent = Convert.ToString((Convert.ToDecimal(activeSum)
          /Convert.ToDecimal(totalSum)) * 100);
      percent = percent.Substring(0, percent.IndexOf('.'));
      MessageBox.Show(percent + "% of the customers sampled are active.");
  }
  else
      MessageBox.Show("Unable to access any customers!");
  dbFile.Close();
  db.Close(); 
```

## Requirements

**Namespace:** [ASNA.DataGate.Common](datagate-common-namespace.html) 

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10

**Assembly:** ASNA DataGate Client (in ASNA.DataGate.Client.dll)
## See Also


[ASNA.DataGate.Common Namespace](datagate-common-namespace.html)
      <br />
[FileAdapter Class](file-adapter-class.html)
      <br />
[SeekRange Method](file-adapter-class-seek-range-method.html)
      <br />
[ReadRange Method](file-adapter-class-read-range-method.html)

