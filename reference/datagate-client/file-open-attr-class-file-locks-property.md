---
title: FileOpenAttr.FileLocks Property

---

Specify record locking mechanisms in opened files. 

## Property Value

[ASNA.DataGate.Common.FileLocks](file-locks-enumeration.html). The record locking mechanism to use.
## Remarks

This property allows some control over the record locking behavior of [ FileAdapter](file-adapter-class.html) access methods. This control is dependent upon the database provider being accessed. For example, the IBM i database does not support "manual" locking.

When set to the Manual value, record locking in the opened file will only occur if explicitly specified in the **FileAdapter** access method. Also, records locked in access methods can only be unlocked explicitly with the [ReleaseCurrent](file-adapter-class-release-current-method.html) or [ReleaseRRN](file-adapter-class-release-rrn-method.html) methods.

When set to the Auto value, record locking occurs automatically in **FileAdapter** access methods unless overridden by the [LockRequest](lock-request-enumeration.html) parameter. Also, locked records are automatically unlocked when another record is accessed.
## Examples


```cs 
  /* Using the FileLocks property of a FileAdapter's OpenAttributes,
   * you can set file locking to manual, which allows you to lock more
   * than one record at a time. Note that manual file locking
   * is database dependent- for instance, it will work with a Acceler8
   * database but not with an IBM i. */
  AdgConnection db = new AdgConnection("*Public/DG NET Local");
  FileAdapter dbFile = new FileAdapter(db, "*Libl/CMASTNEWL1", "CMMASTERL1");
  dbFile.OpenAttributes.FileLocks = FileLocks.Manual;
  dbFile.AccessMode = AccessMode.RWCD;

  AdgDataSet myDS = null;
  dbFile.OpenNewAdgDataSet(out myDS);
  AdgKeyTable keyTbl = myDS.NewKeyTable("RCMMASTL1");

  /* In the code below, we read records for customer numbers
   * 400 - 800. When it ends, we will still have locks on customer numbers
   * 500 and 700. */
  try
  {
      /* Read customer number 400 but don't lock it. */
      keyTbl.Row["CMCUSTNO"] = 400;
      dbFile.ReadRandomKey(myDS, ReadRandomMode.Equal, LockRequest.NoLock, keyTbl);

      /* Read customer number 500 and lock it. */
      keyTbl.Row["CMCUSTNO"] = 500;
      dbFile.ReadRandomKey(myDS, ReadRandomMode.Equal, LockRequest.Read, keyTbl);

      /* Read customer number 600 and lock it. */
      dbFile.ReadSequential(myDS, ReadSequentialMode.Next, LockRequest.Read);

      /* Read customer number 700 and lock it. */
      dbFile.ReadSequential(myDS, ReadSequentialMode.Next, LockRequest.Read);

      /* Read customer number 800 without locking it. */
      dbFile.ReadSequential(myDS, ReadSequentialMode.Next, LockRequest.NoLock);

      /* Unlock customer number 600. */
      keyTbl.Row["CMCUSTNO"] = 600;
      dbFile.ReadRandomKey(myDS, ReadRandomMode.Equal, LockRequest.NoLock, keyTbl);
      dbFile.ReleaseCurrent();

  }
  catch(dgException dgEx)
  { 
      MessageBox.Show("Couldn't find one or more records. " + dgEx.Message,
          dgEx.Error.ToString());
  }

  dbFile.Close(); /* Release all locks. */
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
[FileAdapter Class](file-adapter-class.html)
      <br />
[FileAdapter Members](file-adapter-members.html)
      <br />
[ReleaseCurrent Method](file-adapter-class-release-current-method.html)
      <br />
[ReleaseRRN Method](file-adapter-class-release-rrn-method.html)
      <br />
[LockRequest Enumeration](lock-request-enumeration.html)
      <br />
[FileLocks Enumeration](file-locks-enumeration.html)
      <br />
[ASNA.DataGate.Providers Namespace](datagate-providers-namespace.html)

