---
title: "Input-Only Physical Field Restrictions"
description: "Learn about the restriction and considerations for using input-only physical fields in database design, including their impact on data integrity and application functionality."
---

## Overview

On the IBM i, all physical fields have a usage of input-output. On SQL Server there are certain kinds of table columns that cannot be updated and DataGate will report them as input only.


Although DGL tries to make _SQL Server_ look like DB2 for IBM i, there are several restrictions imposed on the usage of logical fields when they change the name or the type of their corresponding base physical field.  


## Input-Only Table Columns

These are the SQL types and constraints in tables and views that DataGate Linear recognizes as INPUT-only fields:

 - Rowversion columns
 - IDENTITY columns
 - *Computed* columns
 - Join file fields

While DataGate does not create these type of columns, sometimes it is necesary or convinient to add them by hand as part of a remediation or optimization process.  For example, remediating a logical key field that is retyped will [require a computed field](mssql-logical-field-restriction.html) like this one:

```SQL
    USE [MyLibrary]
    ALTER TABLE [dbo].[MYPHYSICAL] ADD LOGABC10 AS (SUBSTRING(PHYABC, 1, 10))  PERSISTED
```

Understanding that these usages are outside the realm of DataGate, care should be taken when copying these tables via DataGate as the new tables will not be true copies of the original ones. When tables and views containing these types of columns are copied or imported via DG, the copied fields will retain the INPUT attribute, but the underlying column will usually lose the original SQL type or constraint.  For example, *rowversion* columns are exposed as input-only hex(8) fields by DataGate, so the copied column will be a write-able binary(8), with DG-defined metadata imbuing the INPUT field attribute.
