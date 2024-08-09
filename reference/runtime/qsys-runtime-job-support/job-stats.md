---
title: "JobStats class                | QSYS API Reference Guide"
description: "Tracks lifetime metrics for the job. "
last_modified_at: 2024-08-09T16:18:25Z
---

Tracks lifetime metrics for the job.

**Namespace:** ASNA.QSys.Runtime.JobSupport
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>

## Properties

| Type | Name | Description
| --- | --- | --- 
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | ActivationGroupsCreated | Gets the number of activation groups created by the job. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | ActivationsCreated | Gets the number of activations created by the job. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | DiskFileOpens | Gets the number of database file open operations performed by the job. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | PrintFileOpens | Gets the number of print file open operations performed by the job. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | WorkstnFileOpens | Gets the number of workstation file open operations performed by the job. |

## Methods

| Signature | Description |
| --- | --- |
| [Clone()](#jobstats-clone) | Gets a copy of the job metrics.
| [IncrementActivationGroupsCreated()](#void-incrementactivationgroupscreated) | Increment by one the number of activation groups created.
| [IncrementActivationsCreated()](#void-incrementactivationscreated) | Increment by one the number of activations created.
| [IncrementDiskFileOpens()](#void-incrementdiskfileopens) | Increment by one the number of database files opened.
| [IncrementPrintFileOpens()](#void-incrementprintfileopens) | Increment by one the number of print files opened.
| [IncrementWorkstnFileOpens()](#void-incrementworkstnfileopens) | Increment by one the number of workstation files opened.
| [ToString()](#string-tostring) | Gets a readable string of the job statistics.

### JobStats Clone()

Gets a copy of the job metrics.

```cs
JobStats Clone()
```

### void IncrementActivationGroupsCreated()

Increment by one the number of activation groups created.

```cs
void IncrementActivationGroupsCreated()
```

### void IncrementActivationsCreated()

Increment by one the number of activations created.

```cs
void IncrementActivationsCreated()
```

### void IncrementDiskFileOpens()

Increment by one the number of database files opened.

```cs
void IncrementDiskFileOpens()
```

### void IncrementPrintFileOpens()

Increment by one the number of print files opened.

```cs
void IncrementPrintFileOpens()
```

### void IncrementWorkstnFileOpens()

Increment by one the number of workstation files opened.

```cs
void IncrementWorkstnFileOpens()
```

### string ToString()

Gets a readable string of the job statistics.

```cs
string ToString()
```
