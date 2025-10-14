---
title: "RangeLast enum                | QSYS API Reference Guide"
description: "Specifies the last range of a sequence. "
last_modified_at: 2024-08-09T17:25:07Z
---

Specifies the last range of a sequence.

**Namespace:** ASNA.DataGate.Common
**Assembly:** ASNA.QSys.DataGate.Client.dll
<br>
<br>

## Enum Values

| Name | Description | Value
| --- | --- | --- 
| Bottom | The range ends at the bottom. | 4 |
| Exclude | The last element is excluded from the range. | 0 |
| Include | The last element is included in the range. | 1 |
| SameAsFirst | The last element is the same as the first element in the range. | 8 |

## Examples

```cs 
  AdgConnection db = createAdgConnection("MyLocalDB");
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
   * than, but not equal to 10000 and less than or equal
   * to, 40000. */
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

  MessageBox.Show(Convert.ToDecimal((activeSum/totalSum) * 100) + 
      "% of the customers sampled are active.");
  dbFile.Close();
  db.Close(); 
```

> See [AdgConnection Example](/reference/datagate/datagate-client/adg-connection.html#create-an-adgconnection) for an implementation of `createAdgConnection()`
