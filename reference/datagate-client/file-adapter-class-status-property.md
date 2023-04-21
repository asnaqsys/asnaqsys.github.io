---
title: FileAdapter.Status Property

---

<span>Indicates the status of the file; whether it is open or closed. </span> 

```cs
 public FileAdapter.AdapterStatus Status { get; }
```

## Property Value

[FileAdapter.AdapterStatus](file-adapter-adapter-status-enumeration.html). Returns a value indicating whether the file is Open(1) or Closed(0).
## Remarks

The value of **Status** is one of the **FileAdapter.AdapterStatus** values.
## Examples

Here we want to use a fileAdapter object named "dbFile" but are unsure as to whether or not it is been initialized, so we check for null and use the Status property to make sure it is opened and open it if it isn't.

```cs 
  if (dbFile == null)
      dbFile = new FileAdapter();
  if (dbFile.Status == FileAdapter.AdapterStatus.Closed)
  {
      dbFile.Connection = myAdgConnection;
      dbFile.FileName = fileName;
      dbFile.MemberName = memberName;
      dbFile.OpenNewAdgDataSet(out myDataSet);
  }
  
```


## Requirements

**Namespace:** [ASNA.DataGate.Client](datagate-client-namespace.html) 

**Assembly:** ASNA DataGate Client

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
## See Also


[FileAdapter Class](file-adapter-class.html)
      <br />
[FileAdapter Members](file-adapter-members.html)
      <br />
      [FileAdapter.AdapterStatus 
					Enumeration](file-adapter-adapter-status-enumeration.html)
      <br />
      [ASNA.DataGate.Client 
					Namespace](datagate-client-namespace.html)  

