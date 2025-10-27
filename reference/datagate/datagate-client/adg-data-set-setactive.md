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
| [SetActive](#bool-setactiveint32-int32)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Sets the active row for a given format index and rrn.
| [SetActive](#bool-setactivestring-int32)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Sets the active row for a given format name and rrn.

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

**SetActive** causes the specified **DataRow** object to be the current value of the `ActiveRow` property.  This is helpful when using `FileAdapter` methods which act upon the "active row" of the **AdgDataSet**, such as `AddRecord`, `ChangeCurrent`, and others.  Whereas many read-access methods of **FileAdapter** implicitly set the active row, **SetActive** allows the program to directly influence the active row.
 
**SetActive** returns a value of **False** if the **DataRow** specified by _rrn_ is not found. No validation of the _iFormat_ parameter is performed.  If _iFormat_ does not refer to a valid index, an exception will occur.



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

**SetActive** causes the specified DataRow object to be the current value of the `ActiveRow `property.  This is helpful when using `FileAdapter`methods which act upon the "active row" of the **AdgDataSet** , such as `AddRecord`, `ChangeCurrent`, and others. Whereas many read-access methods of **FileAdapter** implicitly set the active row, **SetActive** allows the program to directly influence the active row.

**SetActive** returns a value of **False** if the DataRow specified by _rrn_ is not found.  

No validation of the _strFormat_ parameter is performed. If strFormat is null or empty, uses CurrentFormatIndex.  If _strFormat_ does not refer to a valid format name, an exception will occur.



## See Also
- [AdgDataSet class](adg-data-set.html)
