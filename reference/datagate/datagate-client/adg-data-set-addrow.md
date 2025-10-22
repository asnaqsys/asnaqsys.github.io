---
title: "AdgDataSet.AddRow Method"
description: "Adds a new row to the DataTable associated with a format name or index."
---

## Definition

**Namespace:** ASNA.DataGate.Client  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Adds a new row to the DataTable associated with the specified format.

## Overloads

| Signature | Description |
| --- | --- |
| [AddRow](#void-addrowstring)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Adds a new row to the DataTable associated with the specified format name.
| [AddRow](#void-addrowint)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Adds a new row to the DataTable associated with the specified format index.

## void AddRow(String)

Adds a new row to the DataTable associated with the specified format name.

```cs
void AddRow(string strFormat)
```

#### Parameters

| Type | Parameter name | Description |
| --- | --- | --- |
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | strFormat | The format name of the DataTable. |

### Remarks
This method first calls GetFormatIndex with the provided format name to retrieve the corresponding format index, then calls AddRow with the retrieved format index to add a new row.

## void AddRow(Int32)

Adds a new row to the DataTable associated with the specified format index.

```cs
void AddRow(int iFormat)
```

#### Parameters

| Type | Parameter name | Description |
| --- | --- | --- |
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | iFormat | The format index of the DataTable. |

### Remarks
Retrieves the AdgTable instance for the provided format index and calls its AddRow method to add a new row.

## See Also
- [AdgDataSet class](adg-data-set.html)
