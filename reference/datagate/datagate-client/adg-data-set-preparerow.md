---
title: "AdgDataSet.PrepareRow Method"
description: "Prepares a new or specified row for the DataTable associated with a format name or index."
---

## Definition

**Namespace:** ASNA.DataGate.Client  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Prepares a new or specified row for the DataTable associated with the specified format.

## Overloads

| Signature | Description |
| --- | --- |
| [PrepareRow](#datarow-preparerowstring)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Prepares a new row for the DataTable associated with the specified format name.
| [PrepareRow](#void-preparerowstring-datarow)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [DataRow](https://learn.microsoft.com/en-us/dotnet/api/system.data.datarow?view=net-8.0)) | Prepares the specified row for the DataTable associated with the specified format name.
| [PrepareRow](#datarow-preparerowint)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Prepares a new row for the DataTable associated with the specified format index.

## DataRow PrepareRow(String)

Prepares a new row for the DataTable associated with the specified format name.

```cs
DataRow PrepareRow(string strFormat)
```

#### Parameters

| Type | Parameter name | Description |
| --- | --- | --- |
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | strFormat | The format name of the DataTable. |

#### Returns

| Type | Description |
| --- | --- |
| [DataRow](https://learn.microsoft.com/en-us/dotnet/api/system.data.datarow?view=net-8.0) | A new row prepared for the DataTable associated with the specified format name. |

### Remarks
Resolves the format index with GetFormatIndex and delegates to the integer overload.

## void PrepareRow(String, DataRow)

Prepares the specified row for the DataTable associated with the specified format name.

```cs
void PrepareRow(string strFormat, DataRow row)
```

#### Parameters

| Type | Parameter name | Description |
| --- | --- | --- |
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | strFormat | The format name of the DataTable. |
| [DataRow](https://learn.microsoft.com/en-us/dotnet/api/system.data.datarow?view=net-8.0) | row | The row to prepare. |

### Remarks
Resolves the format index with GetFormatIndex, retrieves the AdgTable, and prepares the provided row.

## DataRow PrepareRow(Int32)

Prepares a new row for the DataTable associated with the specified format index.

```cs
DataRow PrepareRow(int iFormat)
```

#### Parameters

| Type | Parameter name | Description |
| --- | --- | --- |
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | iFormat | The format index of the DataTable. |

#### Returns

| Type | Description |
| --- | --- |
| [DataRow](https://learn.microsoft.com/en-us/dotnet/api/system.data.datarow?view=net-8.0) | A new row prepared for the DataTable associated with the specified format index. |

### Remarks
Retrieves the AdgTable for the index and prepares a new row, setting defaults and the active row.

## See Also
- [AdgDataSet class](adg-data-set.html)
