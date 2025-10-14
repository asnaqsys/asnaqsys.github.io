---
title: "FileAdapter.CheckKey Method"
description: "Checks the validity of the provided key table."
---

## Definition

**Namespace:** ASNA.DataGate.Client  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Checks for the existance of a record with the provided key.  

```cs
public void CheckKey(AdgKeyTable keyTable)
```

#### Parameters

| Type | Parameter name | Description |
| --- | --- | --- |
| [AdgKeyTable](/reference/datagate/datagate-client/adg-key-table.html) | keyTable | The AdgKeyTable to check. |

## Remarks
This operation can be used instead of the [SeekKey](./file-adapter-seekkey.html) operation (SETLL in RPG) when the operation is only utilized to see if a record is present in the file. While `SeekKey` positions the cursor close to the supplied key and sets the exact match flag, `CheckKey` only verifies if there is a record with the exact key provided. For large files on SQL Server, `CheckKey` is much faster than `SeekKey`.



## See Also
- [FileAdapter class](file-adapter.html)
