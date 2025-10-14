---
title: "FileAdapter.OpenNewAdgDataSet Method"
description: "Opens a new AdgDataSet for the FileAdapter."
---

## Definition

**Namespace:** ASNA.DataGate.Client  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Opens a file and creates a AdgDataSet corresponding to the record formats of the opened file.

```cs
void OpenNewAdgDataSet(AdgDataSet& ds)
```

#### Parameters

| Type | Parameter name | Description |
| --- | --- | --- |
| [AdgDataSet&](/reference/datagate/datagate-client/adg-data-set.html) | ds | The created AdgDataSet that corresponds to the formats of the file opened. |

## Remarks

[Open](./file-adapter-open.html), **OpenNewAdgDataSet**, and [OpenSimpleQuery](./file-adapter-opensimplequery.html) are the three methods available for opening database files with `FileAdapter`.

<b>OpenNewAdgDataSet</b> opens the file and creates an <b>AdgDataSet</b> instance used by **FileAdapter** for containing file record data for access operations.  The <b>AdgDataSet</b> instance so created is guaranteed to reflect the current record formats of the file.  This is in contrast to the <b>Open</b> method, which accepts a pre-existing <b>AdgDataSet</b> instance parameter, and it is the responsibility of the program to determine the compatibility of the <b>AdgDataSet</b> and file record formats. Generally, <b>OpenNewAdgDataSet</b> is designed for use in applications, whereas <b>Open</b> is suitable for development environments such as Visual RPG.

**Open** and **OpenNewAdgDataSet** observe the current value of the `AccessMode` property.  This property specifies how access to the file is enforced by the database. For example, to allow records to be deleted by the <b>FileAdapter</b>, use a value for **AccessMode** that includes the `AccessMode.Delete` flag.

**Open** and **OpenNewAdgDataSet** also observe the `OpenAttributes` property, to effect other characteristics of the opened file.  These characteristics include "record blocking" for read access, and "level checking" for file format verification.  The value of <b>OpenAttributes</b>is an object of type `FileOpenAttr`.

Record blocking can significantly improve sequential access efficiency especially when utilized against a network database. If the value of `FileOpenAttr.BlockingFactor` is set in the object referenced by <b>OpenAttributes</b>, then read-access record blocking will be used to access the opened file.

If the user provides a value to the `FileOpenAttr.FormatIDs` property of the object referenced by **OpenAttributes**, then the given format identifier(s) will be used to "level check" the format(s) of the file.  If the file is not at the same level when the open operation occurs, the database will return an error.



## See Also
- [FileAdapter class](file-adapter.html)
- [Open](./file-adapter-open.html)
- [OpenSimpleQuery](./file-adapter-opensimplequery.html)
