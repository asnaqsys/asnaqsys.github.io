---
title: "What's new in Monarch Base 5.0"
description: "Version 5.0 brings exciting updates. Learn about the latest features, enhancements, and how they can elevate your project's efficiency."
---

The major new features on Monarch Base 5.0 are:
 * [Support for .NET 8.0](#support-for-net-80)
 * [Support for Reads with No-Lock on SQL Server](#read-with-nolock-on-sql-server)

Version 5.0 is backwards compatible with Version 4.0.


## Support for .NET 8.0
Monarch Base 5.0 is packaged with assemblies multitargeted for .NET 6.0 and .NET 8.0. 


## Read with NoLock on SQL Server
> DataGate can communicate **directly** with SQL Server using ADO.NET; this method of communication is known as _DataGate Linear_. To use _DataGate Linear_ set the ([SourceProfile](/reference/datagate/datagate-providers/source-profile.html)`.PlatformAttribute = "*SQLCLIENT"`.

Starting with version 5.0, _DataGate Linear_ supports reading records without locking them on files that were open for `update`. While this feature is supported on DataGate for IBM i, this was not possible when accessing SQL Server. Up to now, whenever a file was accessed for `update`, any read would always apply a lock to the record read. Now with _DataGate Linear_ it is possible to pass the parameter requesting the record not be locked. Notice that  DataGate for SQL Server (DSS) does not have this enhancement.

The feature comes with a restriction however.  It is not possible to switch between **sequential** reads with-lock and without-lock. In order to switch modes, a random-access operation is needed between the reads, this operation could be a seek (SETLL) or random-read (CHAIN).




