---
title: "FileAdapter.DeleteKey Method"
description: "Deletes the record with the specified key from the file that the FileAdapter is working with."
last_modified_at: 2025-09-26
---

## Definition

**Namespace:** ASNA.DataGate.Client  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Deletes the record with the specified key from the file that the FileAdapter is working with.

```cs
public void DeleteKey(AdgKeyTable keyTable)
```

#### Parameters

| Type | Parameter name | Description |
| --- | --- | --- |
| [AdgKeyTable](/reference/datagate/datagate-client/adg-key-table.html) | keyTable | The AdgKeyTable containing the key of the record to delete. |

## Remarks
 
**DeleteKey** deletes a record in the open file containing a specified key. First, a search for a record containing the key is performed. If such a record is not found, the method throws dgException with an Error number indicating the condition. If the record is found, it is deleted.

The file should be opened with the `AccessMode` property set to a value including the `AccessMode.Delete`flag in order to permit delete access to the file.


## See Also
- [FileAdapter class](file-adapter.html)
