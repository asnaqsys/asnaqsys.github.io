---
title: What's new in Monarch Base 5.0
description: Step into the future with Monarch Base 5.0, as we unveil the latest enhancements and features that redefine the capabilities of our platform. This guide is meticulously crafted for developers, system administrators, and end-users, offering a deep dive into the groundbreaking improvements and new functionalities introduced in version 5.0. From cutting-edge technology integrations to significant performance upgrades, and user experience enhancements, Monarch Base 5.0 is designed to elevate your operational efficiency and productivity. Explore the comprehensive changes that set a new standard for what you can achieve with Monarch Base, ensuring you're fully equipped to leverage the full power of these updates in your projects and workflows.
---

The major new features on Monarch Base 5.0 are:
 * [Support for .NET 8.0](#support-for-net-80)
 * [Support for Reads with No-Lock on SQL Server](#read-with-nolock-on-sql-server)

Version 5.0 is backwards compatible with Version 4.0.


## Support for .NET 8.0
Monarch Base 5.0 is packaged with assemblies multitargeted for .NET 6.0 and .NET 8.0. 


## Read with NoLock on SQL Server
> DataGate can communicate **directly** with SQL Server using ADO.NET; this method of communication is known as _DataGate Linear_. To use _DataGate Linear_ set the ([SourceProfile](/reference/datagate/datagate-providers/source-profile.html)`.PlatformAttribute = "*SQLCLIENT"`.

Starting with version 5.0, _DataGate Linear_ supports reading records without locking them on files that were open for `update`. While this feature is supported on DataGate for IBM i, this was not possible when accessing SQL Server. Up to now, whenever a file was accessed for `update`, any read would alway apply a lock to the record read, with _DataGate Linear_, it is possible now to pass the parameter requesting the record not be locked. Notice that  DataGate for SQL Server (DSS) does not have this enhancment.

The feature comes with a restriction however.  It is not possible to switch between **sequential** reads with-lock and without-lock. In order to switch modes, a random-access operation is needed between the reads, this operation could be a seek (SETLL) or random-read (CHAIN).




