---
title: "IPhysicalMember interface     | QSYS API Reference Guide"
description: "Defines the contract for managing a physical member in the ASNA DataGate client. "
last_modified_at: 2024-08-09T17:25:07Z
---

Defines the contract for managing a physical member in the ASNA DataGate client.

**Namespace:** ASNA.DataGate.Client
**Assembly:** ASNA.QSys.DataGate.Client.dll

**Extends:** doesn't extend any other interfaces.
<br>
<br>

## Remarks
This interface provides properties to manage a physical member in the ASNA DataGate client. 
It includes properties to get the path, number of valid fields, ID, number of clients using the physical member, 
total number of shared reads, number of exclusive record locks, number of waits, number of unlocked exclusive locks, 
number of unlocked shared reads, number of patients, relative record number (RRN), number of deleted records, 
type, status, and user record length of the physical member.

<br>
<br>

## Properties

| Type | Name | Description
| --- | --- | --- 
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | Clients | Gets the number of clients using the physical member. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | DeletedRecords | Gets the number of deleted records in the physical member. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | ExclusiveRecordLocks | Gets the number of exclusive record locks on the physical member. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | ObjectID | Gets the ID of the physical member. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | Path | Gets the path of the physical member. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | Patients | Gets the number of patients on the physical member. |
| [Int64](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | RRN | Gets the relative record number (RRN) of the physical member. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | Status | Gets the status of the physical member. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | TotalShareReads | Gets the total number of shared reads on the physical member. |
| [AdgObjectTypes](/reference/datagate/datagate-common/adg-object-types.html) | Type | Gets the type of the physical member. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | UnlockedExclusives | Gets the number of unlocked exclusive locks on the physical member. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | UnlockedShareReads | Gets the number of unlocked shared reads on the physical member. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | UserRecordLength | Gets the user record length of the physical member. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | ValidFields | Gets the number of valid fields in the physical member. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | WaitsRecord | Gets the number of waits on the physical member. |
