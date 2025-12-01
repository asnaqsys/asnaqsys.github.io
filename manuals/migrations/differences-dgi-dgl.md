---
title: "DataGate for IBM i vs. DataGate Linear: Key Differences"
description: "Understand the crucial differences between DataGate for IBM i and DataGate Linear for SQL Server. This guide highlights their unique features, uses, and which to choose for your needs."
---

## Overview

The following tables describe the differences Between DataGate for IBM i (DG/400) and DataGate Linear for SQL Server (DGL).  Each item that requires significant remediation of migrated RPG **code** is marked in <span style="background-color:red"> red </span>.

Other differences may require additional artifacts in SQL Server, for example, logical fields whose type differs from that of the corresponding physical field cannot be updated and would require a trigger to reflect in the physical file any changes to the logical field.

For reference, here are the [Maximum capacity specifications for SQL Server](https://learn.microsoft.com/en-us/sql/sql-server/maximum-capacity-specifications-for-sql-server).

## Object Considerations

| **ITEM** | **DG/400** | **DGL** | **Code Remediation** |
| ---      | ---        | ---     | ---        |
| Name length for Libraries and Files | 10 characters | 31 characters |  |
| File types | Physical<br><br>Simple logical<br><br>Join logical<br><br>Print <br><br>Multiformat logical <br><br> --- | Physical<br><br>Simple logical<br><br>Join logical<br><br>Print <br><br>  --- <br><br> SqlLogical |  <br><br><br><br><br><br><br><br>  <span style="background-color:red">Yes</span> <br><br>  |
| Max record length | 32,766 bytes | 32,766 bytes.<br>SQL Server has a limit of 8,060 bytes for in-row data, if a DG file is created that would exceed that limit then large fields can be pushed off-row.  |  |
| Library implemented as: | Library | Database |  |
| Object text (description) | 49 characters | 49 characters |  |
| Stored Procedures | Any IBM i HLL language and SQL | Programmed in Transact-SQL |  <span style="background-color:red">Yes</span> |
| Triggers | Any IBM i HLL language and SQL | Programmed in Transact-SQL | <span style="background-color:red">Yes</span> |
| Field Reference File (FRF) | A physical file can refer to any number of FRF, which are any physical file in any library. However, DG/400 will report only those coming from the file stated in the DDS REF keyword. | Refers to the collection of 'User Defined Data Types', which is one per Database (i.e.: Library).  This collection is surfaced via the special file '`*FieldRef`' which is the **_ONLY_** file usable as a FRF. |  |

## Index (Keys) Considerations

| **ITEM** | **DG/400** | **DGL** | **Affects Code** |
| ---      | ---        | ---     | ---        |
| Indexed logical files per physical file |  3,686   | 249 | 
| Imposing 'uniqueness' via select/omit rules in logical files | Supported | Not directly supported. <br/>See **work-around**  note below. | 
| Logical field used as a key field must be based on a physical field with the same name | No  | Yes.  Notice that this eliminates the possibility of using Renamed, Concatenated and Sub-stringed fields as keys. | 
| Maximum number of key fields per key |   120  | 32  | <span style="background-color:red"> Possibly</span>
| Maximum length of key in bytes | 2,000 | 900 | <span style="background-color:red"> Possibly </span>

**Work-around:**

As a work-around to support "Imposing 'uniqueness' via select/omit rules in logical files":

1.  Change the logical file definition to allow duplicate keys.
2.  Create the logical file.
3.  Alter the SQL view with the **`SCHEMABINDING`** attribute.
4.  Add a Unique, Clustered Index to the SQL view (logical file).
5.  Make sure the **`ARITHABORT SET`** option is on/true for the database.

## Data Access Considerations

| **ITEM** | **DG/400** | **DGL** | **Affects Code** | 
| ---      | ---        | ---     | ---        |
| Arrival Access | Relative Record Number is used for Sequential and Random access. | Only Consecutive access is supported, but there is no guaranteed order of retrieval unless the file is indexed.  The only random operation allowed is SetLL and this is only when used with \*Start and \*End. No other kind of seeking (SetGT,CHAIN) is allowed. | <span style="background-color:red">Yes</span>
| Format Name (see Note below) | Given by file creator. | **Always 'R' followed by File Name.**<br><br>Note to ECR Users: The Format can be renamed in the DclDiskFile, using the `RNMFMT` keyword by providing a new name, it is not necessary to provide the existing Name in the `RNMFMT`. This allows the creation of single-source apps that can compile against DG/400 and DGL. | 
| Open Query File | Implemented with OpenQry. | Select expression is used as the `WHERE` clause of a `SELECT`.  The key field list is used as the `ORDER BY` clause.<br><br>The SELECT expression is passed directly to the SQL analyzer with no interpretation.  The expression must follow valid SQL Server syntax.  Pay special attention to uses of logical operators.  Use `'AND'` and `'OR'`, do not use `'&'` and `'|'`. | <span style="background-color:red">Possibly</span>

_**Note -**   Multi-format logical files are not supported on SQL Server. The migrated code is normalized for SQL Server especially when I/O commands target single-format record format names instead of the file name but this does **not** change the application's behavior when accessing files on the IBM i.  
  
If the Rename keyword is present in the legacy file description, the migrated `RNMFMT` keyword will contain the legacy New Format Name.  If the Rename keyword is **not** present in the legacy file description, the migrated `RNMFMT` keyword will contain the files Externally Described Record Format name._

## Locking Considerations

### **Record Locking**

These operation behave different.

| **ITEM** | **DG/400** | **DGL** | **Affects Code** |
| ---      | ---        | ---     | ---        |
| Unlock Record Operation| Cursor position is unchanged. | The file **loses it 'current' position** after the _Unlock_ | <span style="background-color:red">Yes</span>
| Update Record Operation | The record just updated is released. | The record just updated is **kept locked**. | <span style="background-color:red">Yes</span>
| `Access(*NoLock)` option on _Read_ operations | Supported. | It is not possible to switch between sequential reads with-lock and without-lock. In order to switch modes, a random-access operation is needed between the reads, this operation could be a seek (SETLL) or random-read (CHAIN).  | <span style="background-color:red">Possibly</span>

These operations behave in an equivalent way.

| **ITEM** | **DG/400** | **DGL** | **Affects Code** |
| ---      | ---        | ---     | ---        |
| Range operations | When the end of the range is reached, the file has no 'current' position. | When the end of the range is reached, the file has no 'current' position. |
| Hit `EOF` on a sequential read operation | Lose Record position. | Lose Record position. |
| Other operations like `SetLL` | Unlock Record. | Unlock Record. |



### Object Locking

For DGL, object locking is implemented only for Data Area objects.

## Field Considerations

| **ITEM** | **DG/400** | **DGL** | **Affects Code** | 
| ---      | ---        | ---     | ---        |
| Field Name Length | 10 Characters | 31 Characters | 
| Fields per file |   8,000  | 1,024 | <span style="background-color:red"> Possibly </span>
| Re-typing logical fields | Unrestricted | Logical fields whose type differs from that of the corresponding physical field cannot be updated |
| Column Heading Definitions | Up to 3 31-characters | The 3 headings are concatenated into the MS Access CAPTION field | 
| Text Description | Up to 49 characters | Up to 49 characters | 
| Allows Nulls | Yes | Yes |


### Supported Types

| **ITEM** | **DG/400** | **DGL** | **Affects Code** | 
| ---      | ---        | ---     | ---        |
| \- Char | `*CHAR` | char | 
| \- Packed | `*PACKED` | decimal | 
| \- Zoned | `*ZONED` | numeric | 
| \- Binary | `*BINARY` | numeric | 
| \- Float | `*FLOAT` | Float(4): float<br><br>Float(8): real | 
| \- Integer | `*INTEGER` | Integer(2): smallint<br><br>Integer(4): int | 
| \- Date | `*DATE` | `ASNA_DSS.DATE`<br><br>datetime: 00:00:00 | 
| \- Time | `*TIME` | `ASNA_DSS.TIME`<br><br>`datetime: 1899/12/30` | 
| \- Timestamp | `*TIMESTAMP` | datetime | 
| \- Hex | `*HEX` | binary | 
| \- DBCS | `*DBCS` | nchar | 
| \- Unicode | `*DBCS` | nchar | 
| \- Boolean | `*CHAR(1)` | Bit | 
| Variable length Field | Char<br><br>Hex<br><br>Dbcs | varchar<br><br>varbinary<br><br>varnchar | 


### Field Value Sizes

| **ITEM** | **DG/400** | **DGL** | **Affects Code** | 
| ---      | ---        | ---     | ---        |
| Date value range | 0001-01-01 to<br><br>9999-12-31 | Datetime: 1753-01-01 to 9999-12-31 (0001-01-01 maps to 1753-01-01)<br><br>Smalldatetime: 1900-01-01 to 2079-06-06 |
| Decimal number storage | Packed: 1 nibble per digit<br><br>Zoned: 1 byte per digit<br><br>Binary 1 - 4 digits: 2 bytes<br><br>Binary 5 - 9 digits: 4 bytes | Decimal / Numeric<br><br>1 - 9 digits: 4 + 1 bytes<br><br>10 - 19 digits: 8 + 1 bytes<br><br>20 - 29 digits: 12 + 1 bytes<br><br>30 - 38 digits: 16  +1 bytes |
| Date storage | 1 byte per digit / character | Datetime: 8 bytes<br><br>ASNA\_DSS\_DATE: 8 bytes<br><br>SmallDatetime: 4 bytes | 


## Join Considerations

| **ITEM** | **DG/400** | **DGL** | **Affects Code** |
| ---      | ---        | ---     | ---        |
| Supports Use Default for Joins by: | DDS Keyword `JOINDFLT`<br><br>When a record is not found in the secondary file, logical fields whose base is that file will be populated with the default values specified in the physical file definition. | Creating a Left Outer Join instead of an Inner Join.<br><br>From SQL Docs:<br><br>_`LEFT JOIN` or `LEFT OUTER JOIN`_<br><br>_The result set of a left outer join includes all the rows from the left table specified in the `LEFT OUTER` clause, not just the ones in which the joined columns match. When a row in the left table has no matching rows in the right table, the associated result set row contains null values for all select list columns coming from the right table._ | 
| Supports 'Join Duplicates By' | DDS Keyword `JDUP` | Not supported. Duplicate rows in the 'secondary' tables may be returned in random order. | 

  

## Calling Programs/Procedures Considerations

| **ITEM** | **DG/400** | **DGL** | **Affects Code** | 
| ---      | ---        | ---     | ---        |
| Maximum Number of Parameters | 36  | 1024 | 
| Maximum Length of Stored Procedure Name | N/A | 31  | 
| Parameter Direction | \*Input, \*Output, *Both | \*Input, \*Both | 

