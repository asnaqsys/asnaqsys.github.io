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

Adding **DataRow** objects to **AdgDataSet**is generally a three step process.  In the first step a **DataRow** object is established as the "prepared row".  Secondly, fields represented in the **DataRow** columns are set to appropriate values. Finally, the **DataRow** is added to the **DataTable**.  **PrepareRow** performs the first step by creating the **DataRow** object.
 
The **DataRow** object returned by this method is not a member of the **DataTable** corresponding to the format specified, until it has been explicitly inserted via [AddPreparedRowAndSetActive](./adg-data-set-addpreparedrowandsetactive.html), [FileAdapter.AddRecord](./file-adapter-addrecord.html), or a method of **DataTable**.
 
Column data of the **DataRow** object returned by this method is initialized with the value of the **DefaultValue** property of the corresponding **DataColumn**. When an **AdgDataSet** is constructed (for example, by the `FileAdapter.OpenNewAdgDataSet`method), **DataColumn** objects are created to represent the fields of a record format. If a field is capable of containing "null" data (null-capable), the **DefaultValue**of that **DataColumn** is set to **System.DBNull.Value**. Otherwise, the **DefaultValue** is set to a reasonable "zero value" for the data type representing the field. The following table summarizes format field types, their corresponding natural .NET type representations, and the **DefaultValue** property contents used to initialize the column data in **PrepareRow**.

| Database Field DataTypes <br/> or null-capable | DataColumn <br/> .DataType | DataColumn <br/> .DefaultValue |
| --- | --- | --- |
| DataTypes.Binary | `System.Decimal` | `0` |
| DataTypes.Boolean | `System.Boolean` | `False` |
| DataTypes.Char | `System.String` | `""` (an empty string of length zero) |
| DataTypes.Date | `System.DateTime` | `System.DateTime.MinValue` |
| DataTypes.DBCS | `System.String` | `""` (an empty string of length zero) |
| DataTypes.Float | `System.Decimal` | `0` |
| DataTypes.Hex | Array of `System.Byte` | Array of length N, where N is the length in bytes of the field; each element is initialized to 0. |
| DataTypes.Integer | `System.Int` or `System.Short` | `0` |
| DataTypes.Packed | `System.Decimal` | `0` |
| DataTypes.Time | `System.DateTime` | `System.DateTime.MinValue` |
| DataTypes.Timestamp | `System.DateTime` | `System.DateTime.MinValue` |
| DataTypes.Zoned | `System.Decimal` | `0` |
| Any of the above types, null-capable | As above | `System.DBNull.Value` |

Note that **PrepareRow** performs no validation of the _strFormat_ parameter.



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

Adding **DataRow** objects to **AdgDataSet** is generally a three step process.  In the first step a **DataRow** object is established as the "prepared row".  Secondly, fields represented in the **DataRow** columns are set to appropriate values. Finally, the **DataRow** is added to the **DataTable**.

This version of **PrepareRow** stages a pre-existing **DataRow** object, rather than creating a new one.  Since a valid **DataRow** is not created, care should be taken to ensure that <i>row</i> is a valid **DataRow** object for the record format corresponding to <i>strFormat</i>.  A valid **DataRow** may be obtained from one of the other versions of **PrepareRow** or from .NET framework methods in the **System.Data **namespace.

The **DataRow** object returned by this method is not a member of the **DataTable** corresponding to the format specified, until it has been explicitly inserted via [AddPreparedRowAndSetActive](./adg-data-set-addpreparedrowandsetactive.html), [FileAdapter.AddRecord](./file-adapter-addrecord.html), or a method of **DataTable**.

Note that **PrepareRow** performs no validation of the _strFormat_ parameter.

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

Adding **DataRow** objects to **AdgDataSet** is generally a three step process.  In the first step a **DataRow** object is established as the "prepared row".  Secondly, fields represented in the **DataRow** columns are set to appropriate values. Finally, the **DataRow** is added to the **DataTable**. **PrepareRow** performs the first step by creating the **DataRow** object.

The **DataRow** object returned by this method is not a member of the **DataTable** corresponding to the format specified, until it has been explicitly inserted via [AddPreparedRowAndSetActive](./adg-data-set-addpreparedrowandsetactive.html), [FileAdapter.AddRecord](./file-adapter-addrecord.html), or a method of **DataTable**.

Column data of the **DataRow** object returned by this method is initialized with the value of the **DefaultValue** property of the corresponding **DataColumn**. When an **AdgDataSet** is constructed (for example, by the FileAdapter `OpenNewAdgDataSet` Method), **DataColumn** objects are created to represent the fields of a record format. If a field is capable of containing "null" data (null-capable), the **DefaultValue** of that **DataColumn** is set to **System.DBNull.Value**. Otherwise, the **DefaultValue** is set to a reasonable "zero value" for the data type representing the field. The following table summarizes format field types, their corresponding natural .NET type representations, and the **DefaultValue** property contents used to initialize the column data in **PrepareRow**.



| Database Field DataTypes <br/> or null-capable | DataColumn <br/> .DataType | DataColumn <br/> .DefaultValue |
| --- | --- | --- |
| DataTypes.Binary | `System.Decimal` | `0` |
| DataTypes.Boolean | `System.Boolean` | `False` |
| DataTypes.Char | `System.String` | `""` (an empty string of length zero) |
| DataTypes.Date | `System.DateTime` | `System.DateTime.MinValue` |
| DataTypes.DBCS | `System.String` | `""` (an empty string of length zero) |
| DataTypes.Float | `System.Decimal` | `0` |
| DataTypes.Hex | Array of `System.Byte` | Array of length N, where N is the length in bytes of the field; each element is initialized to 0. |
| DataTypes.Integer | `System.Int` or `System.Short` | `0` |
| DataTypes.Packed | `System.Decimal` | `0` |
| DataTypes.Time | `System.DateTime` | `System.DateTime.MinValue` |
| DataTypes.Timestamp | `System.DateTime` | `System.DateTime.MinValue` |
| DataTypes.Zoned | `System.Decimal` | `0` |
| Any of the above types, null-capable | As above | `System.DBNull.Value` |


Note that **PrepareRow** performs no validation of the _iFormat_ parameter.  The number of formats defined in the **AdgDataSet** is given by the `Formats` property. Valid values for _iFormat_ are in the range `0 ≤ _iFormat_ < AdgDataSet.Formats`.



## See Also
- [AdgDataSet class](adg-data-set.html)
