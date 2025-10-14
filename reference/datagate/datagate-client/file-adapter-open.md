---
title: "FileAdapter.Open Method"
description: "Opens the FileAdapter with the specified AdgDataSet."
---

## Definition

**Namespace:** ASNA.DataGate.Client  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Opens the FileAdapter with the specified AdgDataSet.

```cs
void Open(AdgDataSet ds)
```


#### Parameters

| Type | Parameter name | Description |
| --- | --- | --- |
| [AdgDataSet](/reference/datagate/datagate-client/adg-data-set.html) | ds | The AdgDataSet to use for the FileAdapter. |


## Remarks

**Open**, `OpenNewAdgDataSet`, and `OpenSimpleQuery` are the three methods available for opening database files with `FileAdapter`.
**Open**, [OpenNewAdgDataSet](./file-adapter-opennewadgdataset.html), and [OpenSimpleQuery](./file-adapter-opensimplequery.html) are the three methods available for opening database files with `FileAdapter`.

**Open** is designed for use with development environments capable of independently creating **AdgDataSet** instances.  The method is passed an instance of **AdgDataSet** which is presumed to match the database file being opened.  Application developers can open files as effectively and easily using the [OpenNewAdgDataSet](./file-adapter-opennewadgdataset.html) method.

**Open** and **OpenNewAdgDataSet** observe the current value of the `AccessMode` property. This property specifies how access to the file is enforced by the database.  For example, to allow records to be deleted by the *FileAdapter*, use a value for **AccessMode** that includes the `AccessMode.Delete` flag.

**Open** and **OpenNewAdgDataSet** also observe the `OpenAttributes` property, to effect other characteristics of the opened file.  These characteristics include "record blocking" for read access, and "level checking" for file format verification.  The value of **OpenAttributes** is an object of type `FileOpenAttr`.

Record blocking can significantly improve sequential access efficiency, especially when utilized against a database server on the network.  If the value of `FileOpenAttr.BlockingFactor` is set in the object referenced by **OpenAttributes**, then read-access record blocking will be used to access the opened file.

If the user provides a value to the `FileOpenAttr.FormatIDs` property of the object referenced by **OpenAttributes**, then the given format identifier(s) will be used to "level check" the format(s) of the file.  If the file is not at the same level when the open operation occurs, the database will return an error.


## See Also
- [FileAdapter class](file-adapter.html)
- [OpenNewAdgDataSet](./file-adapter-opennewadgdataset.html)
- [OpenSimpleQuery](./file-adapter-opensimplequery.html)
