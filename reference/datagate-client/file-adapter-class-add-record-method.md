---
title: FileAdapter.AddRecord Method

---

Adds a record to a file.

```cs
 public void AddRecord(
AdgDataSet ds
)
```

## Parameters



 *ds* 

: The DataSet object ( **ASNA.DataGate.Client.AdgDataSet)**  to which 
						a single record will be added.
					


## Exceptions

ASNA.DataGate.Common.dgException is thrown to signal normal procedural conditions, in addition to error conditions. The following table summarizes these conditions, and the corresponding value of the dgException.Error property.
<br />



| Value of<br /> 							dgException.Error | Condition |
| ---- | ---- |
| dgEaEOF | The record access operation resulted in an end-of-file condition. This exception also occurs when the record access operation would place the current file position outside of the boundaries established by a prior [ ReadRange](file-adapter-class-read-range-method.html) or [SeekRange](file-adapter-class-seek-range-method.html) method call. |
| dgEaNOTFND | The record to be accessed was not found. It may have been deleted, it may never have existed, or the key may have been changed. |
| dgEaBUSYREC | Record is in use or locked by another process. You cannot access the requested record because it is being used by another database process. Certain DataGate providers may provide further details of the conflicting process in the Message and Text members of dgException. |



<br />

## Examples


```cs 
  AdgConnection db = new AdgConnection("*Public/DG NET Local");
  FileAdapter dbFile = new FileAdapter(db, "*Libl/CMASTNEWL1", 
            "CMMASTERL1");
  dbFile.AccessMode = AccessMode.RWCD;

  AdgDataSet myDS = null;
  try
  {
     db.Open();
     dbFile.OpenNewAdgDataSet(out myDS);
  }
  catch(dgException dgEx)
  {
     MessageBox.Show("Error opening file! " + dgEx.Message, 
            "Error");
     //Exit procedure or end application here.
  }

  DataRow newRow = myDS.PrepareRow(0);
  newRow["CMCustNo"] = 50;
  newRow["CMName"] = "Amalgamated Software of North America";
  newRow["CMAddr1"] = "IH-10 West";
  newRow["CMCity"] = "San Antonio";
  newRow["CMState"] = "TX";
  newRow["CMCntry"] = "US";
  newRow["CMPostCode"] = "78230";
  newRow["CMActive"] = "1";
  newRow["CMFax"] = "2105554679";
  newRow["CMPhone"] = "555-4678";
  myDS.AddPreparedRowAndSetActive(0);
  try
  {
     dbFile.AddRecord(myDS);
  }
  catch (dgException dgEx)
  {
     MessageBox.Show("Adding new record was unsuccessful! "
        + dgEx.Message, "Error!");
     //Exit procedure or end application here.
  }
```


## Requirements

**Namespace:** [ASNA.DataGate.Client](datagate-client-namespace.html) 

**Assembly:** ASNA DataGate Client

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
## See Also


[FileAdapter Class](file-adapter-class.html)
      <br />
[FileAdapter Class Members](file-adapter-members.html)
      <br />
[ReadRange Method](file-adapter-class-read-range-method.html)
      <br />
[SeekRange Method](file-adapter-class-seek-range-method.html) <br />[ASNA.DataGate.Client Namespace](datagate-client-namespace.html)<br />[AdgDataSet Class](adg-dataset-class.html)

