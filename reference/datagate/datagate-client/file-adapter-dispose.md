---
title: "FileAdapter.Dispose Method"
description: "Releases all resources used by the FileAdapter."
---

## Definition

**Namespace:** ASNA.DataGate.Client  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Closes the FileAdapter and releases all resources used by it.

## Overloads

| Signature | Description |
| --- | --- |
| [Dispose()](#void-dispose) | Releases all resources used by the FileAdapter.
| [Dispose](#void-disposebool)([Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Releases the unmanaged resources used by the FileAdapter and optionally releases the managed resources.


## void Dispose()

Releases all resources used by the FileAdapter.

```cs
void Dispose()
```

## void Dispose(bool)

Releases the unmanaged resources used by the FileAdapter and optionally releases the managed resources.

#### Remarks
Use the **Close** or **Dispose** methods to close a file opened by a previous call to one of the open methods (`Open`,`OpenNewAdgDataSet`). After a successful **Close** or **Dispose** call, the file may be subsequently reopened using the same **FileAdapter** object’s open methods.

```cs
void Dispose(bool isDisposing)
```

#### Parameters

| Type | Parameter name | Description |
| --- | --- | --- |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | isDisposing | true to release both managed and unmanaged resources; false to release only unmanaged resources. |

#### Remarks
Use the **Close** or **Dispose** methods to close a file opened by a previous call to one of the open methods (`Open`,`OpenNewAdgDataSet`). After a successful **Close** or **Dispose** call, the file may be subsequently reopened using the same **FileAdapter** object’s open methods.
 
**Dispose** releases unmanaged resources associated with the **FileAdapter**, via the **Dispose** method.


## See Also
- [FileAdapter class](file-adapter.html)
