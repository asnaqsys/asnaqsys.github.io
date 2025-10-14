---
title: "FileAdapter.ChangeCurrent Method"
description: "Changes the current record in the file using the provided AdgDataSet."
---

## Definition

**Namespace:** ASNA.DataGate.Client  
**Assembly:** ASNA.QSys.DataGate.Client.dll


Changes the current record in the file using the provided AdgDataSet.

```cs
void ChangeCurrent(AdgDataSet ds)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [AdgDataSet](/reference/datagate/datagate-client/adg-data-set.html) | ds | The AdgDataSet containing the data for the new record.


## Remarks
**ChangeCurrent** updates the contents of the current record of an open file.  The current record is usually the record most recently accessed (by<code>read</code>or<code>seek</code>method). 

Before issuing a ChangeCurrent, the record must be locked for update. On non-SQL Server providers, upon completion of **ChangeCurrent**, the record is unlocked but on SQL Server the record is kept locked until a further read or unlock operation. Locking the record for update is performed by reading to the record without specifying the "no lock" option.

The AdgDataSet should contain the data for the new record in its tables. The structure of the AdgDataSet should match the structure of the file that the FileAdapter is working with.


## See Also

[FileAdapter Class](file-adapter.html)
