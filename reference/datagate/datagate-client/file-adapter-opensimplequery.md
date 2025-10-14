---
title: "FileAdapter.OpenSimpleQuery Method"
description: "Opens the FileAdapter with a simple query."
---

## Definition

**Namespace:** ASNA.DataGate.Client  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Opens the FileAdapter with a simple query.

```cs
### void OpenSimpleQuery(AdgDataSet& ds, string queryFile, string query, String[] keyNames, KeyUsages[] keyFlags)
```

#### Parameters

| Type | Parameter name | Description |
| --- | --- | --- |
| [AdgDataSet&](/reference/datagate/datagate-client/adg-data-set.html) | ds | The AdgDataSet to use for the FileAdapter. |
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | queryFile | The file to query. |
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | query | The query to execute. |
| [String[]](https://docs.microsoft.com/en-us/dotnet/api/system.string) | keyNames | The names of the keys to use in the query. |
| [KeyUsages[]](/reference/datagate/datagate-common/key-usages.html) | keyFlags | The flags to use for the keys in the query. |


## Remarks
 
**OpenSimpleQuery** opens the file and creates an **AdgDataSet** instance. This **AdgDataSet** is suitable for passing to **FileAdapter** access methods where file record data is processed. The **AdgDataSet** returned by **OpenSimpleQuery** is guaranteed to reflect record formats of the query file.
 
Selection expressions are evaluated during file open time. Therefore, a runtime error will be generated during the opening of the file when a selection expression error is encountered.
 
The selection criteria is specified as a single expression describing the values used to determine which records are selected. Any logical expression formed using relational operators can be specified (such as equal and/or not equal). The syntax of this expression is identical to that used for defining select/omit expressions when creating a logical file.

An retrival order sequence can also be provided by specifying the key fields via the _KeyNams_ parameter.  Sequential reading through the file adapter will retrive records according to the _KeyNames_ and _KeyFlags_.

Note that the length of the _KeyNames_ and _KeyFlags_ array parameters should be equal.


## See Also
- [FileAdapter class](file-adapter.html)
- [Open](./file-adapter-open.html)
- [OpenNewAdgDataSet](./file-adapter-opennewadgdataset.html)

