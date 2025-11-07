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

**GetFormatTable** is used to access the underlying DataTable object used to model a DataGate file format in **AdgDataSet**. It may be used to easily access useful DataTable properties, such as the Rows collection.

**GetFormatName** provides a way to obtain the format name, given an integer index. The number of formats defined in the **AdgDataSet** is given by the **Formats** property. Valid values for _iFormat_ are in the range `0 ≤ _iFormat_ < AdgDataSet.Formats`.  If _iFormat_ is an invalid index, **GetFormatName** throws dgException with the Error property set to dgEINVARG.

To use the file format name, use `GetFormatTable(string)` method.



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

**GetFormatTable** is used to access the underlying DataTable object used to model a DataGate file format in **AdgDataSet.** It may be used to easily access useful DataTable properties, such as the Rows collection.

If _strFormat_ is not a valid format name, **GetFormatTable** throws dgException with the Error property set to dgEINVARG.

To use the file format index, use `GetFormatTable(index)` method.


## See Also
- [AdgDataSet class](adg-data-set.html)
