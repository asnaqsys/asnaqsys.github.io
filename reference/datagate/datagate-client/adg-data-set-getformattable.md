---
title: "AdgDataSet.GetFormatTable Method"
description: "Retrieves the DataTable associated with the specified format index or name."
---

## Definition

**Namespace:** ASNA.DataGate.Client  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Retrieves the DataTable associated with the specified format.

## Overloads

| Signature | Description |
| --- | --- |
| [GetFormatTable](#datatable-getformattableint)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Retrieves the DataTable associated with the specified format index.
| [GetFormatTable](#datatable-getformattablestring)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Retrieves the DataTable associated with the specified format name.

## DataTable GetFormatTable(Int32)

Retrieves the DataTable associated with the specified format index.

```cs
DataTable GetFormatTable(int iFormat)
```

#### Parameters

| Type | Parameter name | Description |
| --- | --- | --- |
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | iFormat | The format index of the DataTable to retrieve. |

#### Returns

| Type | Description |
| --- | --- |
| [DataTable](https://learn.microsoft.com/en-us/dotnet/api/system.data.datatable.select?view=net-8.0) | The DataTable associated with the specified format index. |

### Remarks
Validates the index and returns the DataTable for the AdgTable at that index; throws a dgException if out of range.

## DataTable GetFormatTable(String)

Retrieves the DataTable associated with the specified format name.

```cs
DataTable GetFormatTable(string strFormat)
```

#### Parameters

| Type | Parameter name | Description |
| --- | --- | --- |
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | strFormat | The format name of the DataTable to retrieve. |

#### Returns

| Type | Description |
| --- | --- |
| [DataTable](https://learn.microsoft.com/en-us/dotnet/api/system.data.datatable.select?view=net-8.0) | The DataTable associated with the specified format name. |

### Remarks
Calls GetFormatIndex to resolve the name into an index, then returns the DataTable for that index.

## See Also
- [AdgDataSet class](adg-data-set.html)
