---
title: "Migrating to SQL Server"
description: "Learn how to seamlessly migrate your database to Microsoft SQL Server. This guide covers preparation, execution, and optimization tips."
---

If the database is to be moved to SQL Server in the final stage of the application and will be accessed via DataGate Linear for SQL Server (DGL), then DGL restrictions apply to the migrated application.

Although DGL tries to make _SQL Server_ look like DB2 for IBM i, there are several features that cannot be implemented in a totally transparent fashion. [These differences](differences-dgi-dgl.html) may only affect the database Files themselves or they may also affect the (RPG and CL) Code and will require remediations.

Even when the migrated application is intended to run initially against DB2, if there is a good chance that in the future it may run against SQL Server, then it is good to contemplate the possible changes that will be necessary to adapt the application for SQL Server access and decide if these modifications should be done as part of the original code migration or be left for a future project.

The following items may have the most impact on the migrated code:
 - Some [Record Locking](mssql-record-locking.html) operations behave differently:
   + The Unlock op-code loses the 'current' position.
   + The Update op-code keeps the record locked.
   + Read operations can't use the `Access(*NoLock)` option.

 - [Multi-format](mssql-no-multi-format.html) files are not supported.

 - Renamed or retyped [Logical Fields are restricted](mssql-logical-field-restriction.html) and cannot be used as a key fields or be updated.

 - [Embedded SQL](mssql-embedded-sql.html) statements:
   + Syntax may need updating to comply with T-SQL.
   + Use of Library List must be resolved in code.

