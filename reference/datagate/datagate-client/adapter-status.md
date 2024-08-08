---
title: "AdapterStatus enum            | QSYS API Reference Guide"
description: "Enumerates the possible statuses of the FileAdapter. "
last_modified_at: 2024-08-08T21:41:32Z
---

Enumerates the possible statuses of the FileAdapter.

**Namespace:** ASNA.DataGate.Client
**Assembly:** ASNA.QSys.DataGate.Client.dll
<br>
<br>

## Remarks
The AdapterStatus enumeration is used to represent the current status of the FileAdapter. 
It has two possible values: Closed and Open. 
'Closed' indicates that the FileAdapter is not currently open for any operations. 
'Open' indicates that the FileAdapter is open and ready for operations.

<br>
<br>

## Enum Values

| Name | Description | Value
| --- | --- | --- 
| Closed | Indicates that the FileAdapter is not currently open for any operations. | 0 |
| Open | Indicates that the FileAdapter is open and ready for operations. | 1 |

## Examples

Here we want to use a **FileAdapter** object named "dbFile" but are unsure as to whether or not it is been initialized, so we check for null and use the Status property to make sure it is opened and open it if it isn't.

```cs 
  if (dbFile == null)
      dbFile = new FileAdapter();
  if (dbFile.Status == FileAdapter.AdapterStatus.Closed)
  {
      dbFile.SetConnection( myAdgConnection );
      dbFile.FileName = fileName;
      dbFile.MemberName = memberName;
      dbFile.OpenNewAdgDataSet(out myDataSet);
  }
  
```
