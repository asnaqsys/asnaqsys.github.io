---
title: "AdgDataSet.SetActive Method"
description: "Sets the active row to the specified RRN in the DataTable for the given format name or index."
---

## Definition

**Namespace:** ASNA.DataGate.Client  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Sets the active row to the row at the specified relative record number (rrn) in the DataTable associated with the specified format.

## Overloads

| Signature | Description |
| --- | --- |
| [SetActive](#bool-setactiveint-int)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Sets the active row for a given format index and rrn.
| [SetActive](#bool-setactivestring-int)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Sets the active row for a given format name and rrn.

## bool SetActive(Int32, Int32)

Sets the active row to the row at the specified rrn in the DataTable associated with the specified format index.

```cs
bool SetActive(int iFormat, int rrn)
```

#### Parameters

| Type | Parameter name | Description |
| --- | --- | --- |
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | iFormat | The format index of the DataTable. |
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | rrn | The relative record number of the row to set as active. |

#### Returns

| Type | Description |
| --- | --- |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | True if the active row was successfully set; otherwise, false. |

### Remarks
If iFormat is less than 0, uses CurrentFormatIndex. Otherwise, retrieves the AdgTable for the index and sets the active row internally.

## bool SetActive(String, Int32)

Sets the active row to the row at the specified rrn in the DataTable associated with the specified format name.

```cs
bool SetActive(string strFormat, int rrn)
```

#### Parameters

| Type | Parameter name | Description |
| --- | --- | --- |
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | strFormat | The format name of the DataTable. |
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | rrn | The relative record number of the row to set as active. |

#### Returns

| Type | Description |
| --- | --- |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | True if the active row was successfully set; otherwise, false. |

### Remarks
If strFormat is null or empty, uses CurrentFormatIndex; otherwise, resolves the name to an index and delegates to the integer overload.

## See Also
- [AdgDataSet class](adg-data-set.html)
