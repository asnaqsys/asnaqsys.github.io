---
title: "LockRequest enum              | QSYS API Reference Guide"
description: "Specifies the type of lock to request on a resource. "
last_modified_at: 2024-08-08T21:41:32Z
---

Specifies the type of lock to request on a resource.

**Namespace:** ASNA.DataGate.Common
**Assembly:** ASNA.QSys.DataGate.Client.dll
<br>
<br>

## Enum Values

| Name | Description | Value
| --- | --- | --- 
| Default | No specific lock request. The default behavior is used. | 0 |
| NoLock | No lock is requested on the resource. | 8 |
| NoWait | Requests a lock without waiting if the lock is not immediately available. | 1 |
| Read | Requests a read lock on the resource. | 2 |
| ReadWrite | Requests both a read and write lock on the resource. | 6 |
| Write | Requests a write lock on the resource. | 4 |

## Example 1. Requesting to avoid locking records in a file, while we read sequentially through it.

```cs 
  AdgConnection db = new AdgConnection("*Public/DG NET Local");
  FileAdapter dbFile = new FileAdapter(db, "*Libl/CMASTNEWL1", "CMMASTERL1");
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

  /* We're only checking these records and don't want to waste time by
   * locking every one, so we use LockRequest.NoLock. 
   * Note that a quicker way to find a record with such a specific 
   * criteria is to use the OpenSimpleQuery method of FileAdapter. 
   * This is merely an example. */
  bool EOF = false;
  while(! EOF)
  {
      try
      {
          dbFile.ReadSequential(myDS, ReadSequentialMode.Next, LockRequest.NoLock);
          if (Convert.ToDecimal(myDS.ActiveRow["CMCUSTNO"]) &gt; 30000 &amp;&amp;
              Convert.ToString(myDS.ActiveRow["CMNAME"]).StartsWith("A"))
          {
              /* We read once backwards to get the record again, and this
               * time we lock it. */
              dbFile.ReadSequential(myDS, ReadSequentialMode.Previous, LockRequest.Default);
              break;
          }
      }
      catch(dgException dgEx)
      {
          if (dgEx.Error == dgErrorNumber.dgEaEOF)
              EOF = true;
          else
              throw dgEx;
      }
  }
  if (EOF)
      MessageBox.Show("End of file was reached- record not found.", "Record not found.");
  else
  {
      /* We now make the name all lower case before updating the file. */
      myDS.ActiveRow["CMName"] = myDS.ActiveRow["CMName"].ToString().ToLower();

      MessageBox.Show("Customer number " + 
      Convert.ToDecimal(myDS.ActiveRow["CMCUSTNO"]).ToString() +
          ", \"" + Convert.ToString(myDS.ActiveRow["CMName"]) + 
          "\", met the search requirements.", "Customer found.");
  }

```

## Example 2. First read with NoLock request, immediately read backwards without locking.


```cs 
  AdgConnection db = new AdgConnection("*Public/DG NET Local");
  FileAdapter dbFile = new FileAdapter(db, "*Libl/CMASTNEWL1", "CMMASTERL1");
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

  /* We're only checking these records and don't want to waste time by
   * locking every one, so we use LockRequest.NoLock. 
   * Note that a quicker way to find a record with such a specific 
   * criteria is to use the OpenSimpleQuery method of FileAdapter. 
   * This is merely an example. */
  bool EOF = false;
  while(! EOF)
  {
      try
      {
          dbFile.ReadSequential(myDS, ReadSequentialMode.Next, LockRequest.NoLock);
          if (Convert.ToDecimal(myDS.ActiveRow["CMCUSTNO"]) &gt; 30000 &amp;&amp;
              Convert.ToString(myDS.ActiveRow["CMNAME"]).StartsWith("A"))
          {
              /* We read once backwards to get the record again, and this
               * time we lock it. */
              dbFile.ReadSequential(myDS, ReadSequentialMode.Previous, LockRequest.Default);
              break;
          }
      }
      catch(dgException dgEx)
      {
          if (dgEx.Error == dgErrorNumber.dgEaEOF)
              EOF = true;
          else
              throw dgEx;
      }
  }
  if (EOF)
      MessageBox.Show("End of file was reached- record not found.", "Record not found.");
  else
  {
      /* We now make the name all lower case before updating the file. */
      myDS.ActiveRow["CMName"] = myDS.ActiveRow["CMName"].ToString().ToLower();

      MessageBox.Show("Customer number " + 
      Convert.ToDecimal(myDS.ActiveRow["CMCUSTNO"]).ToString() +
          ", \"" + Convert.ToString(myDS.ActiveRow["CMName"]) + 
          "\", met the search requirements.", "Customer found.");
  }

```
