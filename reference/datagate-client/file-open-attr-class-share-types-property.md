---
title: FileOpenAttr.ShareTypes Property

---

Specify concurrent access on the open file.

```cs
 public ShareTypes ShareTypes { get; set; }
```

## Property Value

[ASNA.DataGate.Common.ShareTypes](share-types-enumeration.html). Specifies concurrent access locking on the open file.
## Remarks

Applications may need to open a file for access exclusively to prevent access by other processes as data is being updated. Other applications may need to place no restrictions on concurrent access so that updates are immediately available in the open file. These requirements and others for sharing open file resources can be controlled with the <span> **ShareTypes** </span> property.

Set the value of **ShareTypes** to request the type of sharing required by your application. The access restrictions requested will be enforced by the database when the file is opened and until the file is closed. If the file cannot be opened with the level of sharing specified by <span> **ShareTypes** </span>, then the [ FileAdapter.Open](file-adapter-class-open-method.html) method will throw an exception.
## Examples


```cs 
  /* We open the file in order to delete all of its records. */
  AdgConnection db = new AdgConnection("*Public/DG NET Local");
  FileAdapter dbFile = new FileAdapter(db, "*Libl/CMASTNEW", "CMMASTER");
  dbFile.AccessMode = AccessMode.Delete;
  /* Its generally good practice to make sure you have an exclusive lock
   * on a file that you are deleting all of the records from, but some
   * databases do not require it. */
  dbFile.OpenAttributes.ShareTypes = ShareTypes.Exclusive;
  AdgDataSet myDS = null;

  try
  {
      dbFile.Open(myDS);
      dbFile.DeleteAllRecords();
  }
  catch(dgException dgEx)
  {
      db.Close();
      if (dgEx.Error == dgErrorNumber.dgEmBUSYOBJ)
      {
          MessageBox.Show("Couldn't open the file for exclusive access.", "Error opening file.");
          //Exit routine or procedure here to avoid preceding file operations.
      }
      else 
          throw dgEx;
  }
  dbFile.DeleteAllRecords();

  dbFile.Close();
  db.Close();
```


## Requirements

**Namespace:** [ ASNA.DataGate.Providers](datagate-providers-namespace.html) 

**Assembly:** ASNA DataGate Client

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
## See Also


[FileOpenAttr Class](file-open-attr-class.html)
      <br />
[FileOpenAttr Class Members](file-open-attr-class-members.html)
      <br />
[Open Method](file-adapter-class-open-method.html)
      <br />
[ShareTypes Enumeration](share-types-enumeration.html)
      <br />
[ASNA.DataGate.Providers Namespace](datagate-providers-namespace.html)

