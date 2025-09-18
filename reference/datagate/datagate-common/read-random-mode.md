---
title: "ReadRandomMode enum           | QSYS API Reference Guide"
description: "Specifies the mode for reading data randomly. "
last_modified_at: 2024-08-09T17:25:07Z
---

Specifies the mode for reading data randomly.

**Namespace:** ASNA.DataGate.Common
**Assembly:** ASNA.QSys.DataGate.Client.dll
<br>
<br>

## Enum Values

| Name | Description | Value
| --- | --- | --- 
| Equal | Specifies that the reading starts from the record that equals the key. | 13 |
| Greater | Specifies that the reading starts from the record that is greater than the key. | 14 |
| GTEQ | Specifies that the reading starts from the record that is greater than or equal to the key. | 15 |

## Examples


```cs 
  AdgConnection db = createAdgConnection("*Public/DG NET Local");
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

> See [AdgConnection Example](/reference/datagate/datagate-client/adg-connection.html#create-an-adgconnection) for an implementation of `createAdgConnection()`
