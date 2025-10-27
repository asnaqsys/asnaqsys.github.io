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
| [AddRow](#void-addrowint32)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Adds a new row to the DataTable associated with the specified format index.

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
This method first calls [GetFormatIndex](./adg-data-set-getformatindex.html) with the provided format name to retrieve the corresponding format index, then calls [AddRow](#void-addrowint32) with the retrieved format index to add a new row.

**AddRow** appends a prepared row to the table specified by _strFormat_.  A prepared row can be created, or an existing DataRow can be set as a prepared row, using one of the [PrepareRow](adg-data-set-preparerow.html) methods of **AdgDataSet**.

The usual pattern of use involves first staging the prepared DataRow object via **PrepareRow** , setting the field values in the DataRow as necessary, then calling **AddRow** or [AddPreparedRowAndSetActive](adg-data-set-addpreparedrowandsetactive.html) to append the row to the table.

Note that prior to calling this method, you must call **PrepareRow** to stage a prepared row for insertion to the table. Also, upon return from this method, the prepared row of the table remains the row added to the table. Calling **AddRow** or **AddPreparedRowAndSetActive** again before calling **PrepareRow** will cause an exception.



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
 
 **AddRow** appends a prepared row to the table specified by _iFormat_. A prepared row can be created, or an existing DataRow can be set as a prepared row, using one of the [PrepareRow](adg-data-set-preparerow.html) methods of **AdgDataSet**.  
 
The usual pattern of use involves first staging the prepared DataRow object via **PrepareRow** , setting the field values in the DataRow as necessary, then calling **AddRow** or [AddPreparedRowAndSetActive](adg-data-set-addpreparedrowandsetactive.html) to append the row to the table.
 
 Note that prior to calling this method, you must call **PrepareRow** to stage a prepared row for insertion to the table.  Also, upon return from this method, the prepared row of the table remains the row added to the table. Calling **AddRow** or **AddPreparedRowAndSetActive** again before calling **PrepareRow** will cause an exception.


## See Also
- [AdgDataSet class](adg-data-set.html)
