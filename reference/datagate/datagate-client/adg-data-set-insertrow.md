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
 **InsertRow** inserts a prepared row into the table specified by _strFormat_ at the position indicated by the _rrn_. A prepared row can be created using one of the `PrepareRow Method`methods of `AdgDataSet`.
 
The usual pattern of use involves first staging the prepared DataRow object via **PrepareRow**, setting the field values in the DataRow as necessary, then calling **InsertRow** to insert the row into the table.
 
Note that prior to calling this method, you must call **PrepareRow** to stage a prepared row for insertion to the table. Also, upon return from this method, the prepared row of the table remains the row added to the table. Calling **InsertRow**, `AddRow`or `AddPreparedRowAndSetActive`again before calling **PrepareRow **will cause an exception.

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

 **InsertRow** inserts a prepared row to the table specified by _iFormat_ at the position indicated by the _rrn_. A prepared row can be created using one of the `PrepareRow` methods of `AdgDataSet`.

 
The usual pattern of use involves first staging the prepared DataRow object via **PrepareRow** , setting the field values in the DataRow as necessary, then calling **InsertRow**  to insert the row into the table.
 
 Note that prior to calling this method, you must call **PrepareRow** to stage a prepared row for insertion to the table.  Also, upon return from this method, the prepared row of the table remains the row added to the table. Calling **InsertRow**, `AddRow` or `AddPreparedRowAndSetActive` again before calling **PrepareRow** will cause an exception.



## See Also
- [AdgDataSet class](adg-data-set.html)
