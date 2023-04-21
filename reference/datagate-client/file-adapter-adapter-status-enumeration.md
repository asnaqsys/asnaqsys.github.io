---
title: FileAdapter.AdapterStatus Enumeration

---

Indicates the status of the file: open or closed. 

```cs
 public FileAdapter.AdapterStatus Status { get: }
```

## Remarks

The **FileAdapter.AdapterStatus** enumeration is used as a parameter by the [ FileAdapter.Status Property](file-adapter-class-status-property.html) of the [FileAdapter Class](file-adapter-class.html).
## Members



| Member | Description | Value |
| ---- | ---- | ---- |
| Open | The file is open. | 1 |
| Closed | The file is closed. | 0 |



## Examples

Here we want to use a **FileAdapter** object named "dbFile" but are unsure as to whether or not it is been initialized, so we check for null and use the Status property to make sure it is opened and open it if it isn't.

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
[FileAdapter.Status Property](file-adapter-class-status-property.html) <br />[FileAdapter Members](file-adapter-members.html) <br />[ASNA.DataGate.Client Namespace](datagate-client-namespace.html)  

