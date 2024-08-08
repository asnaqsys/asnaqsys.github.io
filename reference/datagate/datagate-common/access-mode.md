---
title: "AccessMode enum               | QSYS API Reference Guide"
description: "Specifies the access mode for a data operation. "
last_modified_at: 2024-08-08T21:41:32Z
---

Specifies the access mode for a data operation.

**Namespace:** ASNA.DataGate.Common
**Assembly:** ASNA.QSys.DataGate.Client.dll
<br>
<br>

## Enum Values

| Name | Description | Value
| --- | --- | --- 
| Arrival | Specifies arrival access. | 2 |
| CacheWrites | Specifies cache writes access. | 32 |
| Change | Specifies change access. | 4 |
| CommitmentControl | Specifies commitment control access. | 16 |
| Delete | Specifies delete access. | 8 |
| Output | Specifies output access. | 76 |
| OutputCache | Specifies output cache access. | 108 |
| PrintPreview | Specifies print preview access. | 256 |
| Read | Specifies read access. | 129 |
| ReadWrite | Specifies read/write access. | 193 |
| ReadWriteCache | Specifies read/write cache access. | 225 |
| RWCD | Specifies RWCD access. | 205 |
| RWCDCache | Specifies RWCDCache access. | 237 |
| SetLLAsILE | Specifies SetLLAsILE access. | 1 |
| Write | Specifies write access. | 64 |
| WriteCache | Specifies write cache access. | 96 |
| WriteCacheArrival | Specifies write cache arrival access. | 98 |

## Examples 

```cs 
  AdgConnection db = new AdgConnection("*Public/DG NET Local");
  FileAdapter dbFile = new FileAdapter(db, "*Libl/CMASTNEWL1", "CMMASTERL1");
  /* We need to open this file for Read as well as as Delete
   * in order search for the key value. */
  dbFile.AccessMode = AccessMode.Delete | AccessMode.Read;

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

  /* We retrieve the record for customer number 82900 and delete it! */
  AdgKeyTable keyTbl = myDS.NewKeyTable("RCMMASTL1");
  keyTbl.Row["CMCUSTNO"] = 82900;
  try
  {
      dbFile.DeleteKey(keyTbl);
  }
  catch(dgException dgEx)
  {
      /* We catch the dgException only if it was caused by
       * the key value not being found. */
      if (dgEx.Error != dgErrorNumber.dgEaNOTFND)
          throw dgEx;
  }
  dbFile.Close();
  db.Close();
```
