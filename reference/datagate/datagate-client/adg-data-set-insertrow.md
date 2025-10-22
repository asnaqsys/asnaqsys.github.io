---
title: "AdgDataSet.InsertRow Method"
description: "Inserts a new row at the specified RRN in the DataTable for the given format name or index."
---

## Definition

**Namespace:** ASNA.DataGate.Client  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Inserts a new row at the specified relative record number (rrn) in the DataTable associated with the specified format.

## Overloads

| Signature | Description |
| --- | --- |
| [InsertRow](#void-insertrowstring-int)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Inserts a new row at the specified rrn for the given format name.
| [InsertRow](#void-insertrowint-int)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Inserts a new row at the specified rrn for the given format index.

## void InsertRow(String, Int32)

Inserts a new row at the specified rrn in the DataTable associated with the specified format name.

```cs
void InsertRow(string strFormat, int rrn)
```

#### Parameters

| Type | Parameter name | Description |
| --- | --- | --- |
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | strFormat | The format name of the DataTable. |
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | rrn | The relative record number at which to insert the new row. |

### Remarks
Resolves the format index via GetFormatIndex and calls the overload that takes an index.

## void InsertRow(Int32, Int32)

Inserts a new row at the specified rrn in the DataTable associated with the specified format index.

```cs
void InsertRow(int iFormat, int rrn)
```

#### Parameters

| Type | Parameter name | Description |
| --- | --- | --- |
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | iFormat | The format index of the DataTable. |
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | rrn | The relative record number at which to insert the new row. |

### Remarks
Retrieves the AdgTable for the index and calls its InsertRow method to insert a row at rrn.

## See Also
- [AdgDataSet class](adg-data-set.html)
