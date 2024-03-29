---
title: AccessMode Enumeration

---

Options for restricting access to open files.<span style="MARGIN-BOTTOM: 0.8em" />

```cs
 public enum AccessMode;
```


## Remarks

**AccessMode** defines flag values which can be used alone or combined to create a custom value to suit an application’s requirements for accessing a particular file. Many common combinations, such as ReadWrite and <span>RWCD</span>, are predefined by the enumeration.

The [AccessMode](file-adapter-class-access-mode-property.html) property of <span> **FileAdapter** </span> contains a value of AccessMode, which should be set prior to calling <span> **FileAdapter’s** </span>[Open](file-adapter-class-open-method.html), [ OpenNewAdgDataSet](file-adapter-class-open-new-adg-dataset-method.html), or [ OpenSimpleQuery](file-adapter-class-open-simple-query-method.html) to provide the requested access restrictions on the opened file. 
## Members



| Member | Description | Value |
| ---- | ---- | ---- |
| Arrival | Records are read from the file in relative record order (where supported). | 2 |
| CacheWrites | <p>A file’s data buffers are not written immediately to disk after each Add, Delete or Update operation. The target machine's inherent caching is enabled. | 32 |
| Change | Records in the file may be updated (changed). | 4 |
| CommitmentControl | The file is enabled for Commitment Control. | 16 |
| Delete | Records in the file may be deleted. | 8 |
| OutPut | Reserved for future use. | 76 |
| OutPutCache | Reserved for future use. | 108 |
| PrintPreview | PrinterFile output can be previewed prior to printing. | 256 |
| Read | Records may be read from the file. | 128 |
| ReadWrite | Records may be read from the file and new records may be added. (Read + Write). | 192 |
| ReadWriteCache | Records may be read from the file and new records may be added. The target machine's inherent caching is enabled for added records. (Read + Write + CacheWrites). | 224 |
| RWCD | Records in the file may be read, updated, deleted and added. (Read + Change + Delete + Write). | 204 |
| RWCDCache | Records in the file may be read, updated, deleted and added. The target machine's inherent caching is enabled for added, deleted and changed records. (Read + Change + Delete + Write + CacheWrites). | 236 |
| Write | New records may be added to the file. | 64 |
| WriteCache | Only new records may be added to a File and they are not written immediately to disk after each Add operation. The target machine's inherent caching is enabled. (Write + CacheWrites). | 96 |



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

## Requirements

**Namespace:** [ASNA.DataGate.Common](datagate-common-namespace.html) <span style="FONT-SIZE: 8pt; FONT-FAMILY: Verdana"> <p /></span> 

**Assembly:** ASNA DataGate Client (in ASNA.DataGate.Client.dll)

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10

## See Also


[AdgConnection Class](adg-connection-class.html)
      <br />
[File Adapter Class](file-adapter-class.html)
      <br />
[AccessMode Property](file-adapter-class-access-mode-property.html)
      <br />
[Open Method](file-adapter-class-open-method.html)
      <br />
[OpenNewAdgDataSet Method](file-adapter-class-open-new-adg-dataset-method.html)
      <br />
[OpenSimpleQuery Method](file-adapter-class-open-simple-query-method.html)
      <br />
[ASNA.DataGate.Common Namespace](datagate-common-namespace.html)

