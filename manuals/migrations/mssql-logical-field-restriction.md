---
title: "Logical Field Restrictions when moving to SQL Server"
description: "This document examines the constraints and considerations associated with logical field restrictions when migrating databases to SQL Server, offering insights into compatibility, performance, and data integrity challenges."
---

## Overview

Although DGL tries to make _SQL Server_ look like DB2 for IBM i, there are several restrictions imposed on the usage of logical fields when they change the name or the type of their corresponding base physical field.  

## Renamed Key Fields
A logical field whose name has changed from its physical base field cannot be used as a key field in the logical file.

## Computed Key Fields
When a logical field is retyped, most typically because the field is a concatenation or substring of the underlying physical fields, then the logical field becomes read-only and, additionally, it cannot be used as a key field.  

One way of remediating the usage of a retyped field as a key field is to use a computed field.

Assume this DDS logical field definition fragment:
```
|...+....1....+....2....+....3....+....4....+....5....+....6....+....7....+....8
     A          R LOGFMT                    PFILE(MYPHISICAL)
     A            FLD1      R
     A            FLD2      R
     A            FLD3      R
     A            LOGABC10           I      SST(PHYABC 1 10)
     A          K LOGABC10
     A ...
```

Add a persisted computed field to the underlying Table with the name of the logical field like this:
```SQL
    USE [MyLibrary]
    ALTER TABLE [dbo].[MYPHYSICAL] ADD LOGABC10 AS (SUBSTRING(PHYABC, 1, 10))  PERSISTED
```

And then use the computed field as the key field of the logical file

There are some caveats to consider when using this technique:

1.	Programs that use the physical file will now be reading the logical field, if this is undesirable, then a RNMFLDS (Rename Fields) command must be included in the program to hide the field from the physical file format, something like this:
```    RnmFlds Fmt( MYPHYSICAL_Rec )   Flds (LOGABC10,  *NONE)```

2.	It is assumed that the logical field name is not already present on the table, otherwise, a new name should be used for the computed field and the field renamed via RNMFLDS in all of the programs that use it.

Please note the [restrictions](mssql-input-only-physical-fields.html)  on using input-only physical fields.
