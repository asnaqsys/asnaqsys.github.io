---
title: "Configure MS SQL Server for DataGate Linear"
description: "Learn how to configure Microsoft SQL Server for DGLinear integration. This guide covers setup, optimization, and troubleshooting tips."
---

DataGate Linear is the implementation of DataGate used to communicate to SQL Server directly via ADO.NET.  

DG Linear is implemented as part of the ASNA.QSys.DataGte.Client .NET assembly and is supported by the configuration table `___ASNA_SysVal` stored in the master database.


## Configuration Table
The `___ASNA_SysVal` table contains a set of values that are used to configure the behavior of DataGate on SQL Server.

| Name | Default Value | Description
| ---- | ------------- | -----------
System Library List |  | Specifies the DSS/SQL instance's System Library List; equivalent to the IBMi's QSYSLIBL system value. Comma separated, ordered list of database names, or null. SQL instance scope.
User Library List |  | Specifies the DSS/SQL instance's User Library List; equivalent to the IBMi's QUSRLIBL system value. Comma separated, ordered list of database names, or null. SQL instance scope.
New Column Collation | NULL | Sets the default collation specified in the COLLATION clause of CREATE TABLE statements used to create DataGate physical files. If null or not available, the target DB's collation or SQL_Latin1_General_CP_CS_AS is used. SQL instance or database scope.
Propagate Libl Changes to DSS | NULL | When 'TRUE', and the legacy DSS 'master.dbo.ASNA_Libl' table exists, changes to library list values will propagate to the appropriate corresponding entry in the legacy table.  Otherwise, only the system value changes.
\# Prefix Substitution | _# | Specifies a string used to substitute the prefix '#' in DataGate object names, to avoid unintentional use of the SQL Server "temporary table" feature.  Default value is "_#".  Disable substitution by specifying NULL or empty string.  SQL instance scope.
Qtemp Library | QTEMP | Enable DSS support for a DataGate QTEMP library. Specify a database name to enable. If configured, the specified database may only be accessed in DataGate with the QTEMP library designation. SQL instance scope.
Enable Multimember | TRUE | Enable DSS support for multiple members in a single file, for most file types. Specify 'TRUE' or 'FALSE'; otherwise defaults to 'FALSE'.  SQL instance scope.

The following script can be used to create the `___ASNA_SysVal` table.

```sql
USE [master]
GO
SET ANSI_NULLS ON
GO
SET QUOTED_IDENTIFIER ON
GO
IF NOT EXISTS (SELECT * FROM sys.objects WHERE object_id = OBJECT_ID(N'[dbo].[___ASNA_SysVal]') AND type in (N'U'))
BEGIN
  CREATE TABLE [dbo].[___ASNA_SysVal]
  (
    [Name] [nvarchar](128) NOT NULL,
    [Value] [nvarchar](2048) NULL,
    [Description] [nvarchar](256) NULL
  )
  ON [PRIMARY]

  INSERT [dbo].[___ASNA_SysVal] ([Name], [Value], [Description]) VALUES (N'System Library List', NULL, N'Specifies the DSS/SQL instance''s System Library List; equivalent to the IBMi''s QSYSLIBL system value. Comma separated, ordered list of database names, or null. SQL instance scope.')
  INSERT [dbo].[___ASNA_SysVal] ([Name], [Value], [Description]) VALUES (N'User Library List', NULL, N'Specifies the DSS/SQL instance''s User Library List; equivalent to the IBMi''s QUSRLIBL system value. Comma separated, ordered list of database names, or null. SQL instance scope.')
  INSERT [dbo].[___ASNA_SysVal] ([Name], [Value], [Description]) VALUES (N'New Column Collation', NULL, N'Sets the default collation specified in the COLLATION clause of CREATE TABLE statements used to create DataGate physical files. If null or not available, the target DB''s collation or SQL_Latin1_General_CP_CS_AS is used. SQL instance or database scope.')
  INSERT [dbo].[___ASNA_SysVal] ([Name], [Value], [Description]) VALUES (N'Propagate Libl Changes to DSS', NULL, N'When ''TRUE'', and the legacy DSS ''master.dbo.ASNA_Libl'' table exists, changes to library list values will propagate to the appropriate corresponding entry in the legacy table.  Otherwise, only the system value changes.')
  INSERT [dbo].[___ASNA_SysVal] ([Name], [Value], [Description]) VALUES (N'# Prefix Substitution', N'_#', N'Specifies a string used to substitute the prefix ''#'' in DataGate object names, to avoid unintentional use of the SQL Server "temporary table" feature.  Default value is "_#".  Disable substitution by specifying NULL or empty string.  SQL instance scope.')
  INSERT [dbo].[___ASNA_SysVal] ([Name], [Value], [Description]) VALUES (N'Qtemp Library', N'QTEMP', N'Enable DSS support for a DataGate QTEMP library. Specify a database name to enable. If configured, the specified database may only be accessed in DataGate with the QTEMP library designation. SQL instance scope.')
  INSERT [dbo].[___ASNA_SysVal] ([Name], [Value], [Description]) VALUES (N'Enable Multimember', 'TRUE', N'Enable DSS support for multiple members in a single file, for most file types. Specify ''TRUE'' or ''FALSE''; otherwise defaults to ''FALSE''.  SQL instance scope.')
END
GO
```
