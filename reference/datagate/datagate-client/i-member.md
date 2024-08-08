---
title: "IMember interface             | QSYS API Reference Guide"
description: "Defines the contract for managing a member in the ASNA DataGate client. "
last_modified_at: 2024-08-08T21:41:32Z
---

Defines the contract for managing a member in the ASNA DataGate client.

**Namespace:** ASNA.DataGate.Client
**Assembly:** ASNA.QSys.DataGate.Client.dll

**Extends:** [IAdgObject](/reference/datagate/datagate-client/i-adg-object.html), [IComparable](https://learn.microsoft.com/en-us/dotnet/api/system.icomparable-1?view=net-8.0), [IConnectionHandler](/reference/datagate/datagate-client/i-connection-handler.html), [IDisposable](https://learn.microsoft.com/en-us/dotnet/api/system.idisposable?view=net-8.0)
<br>
<br>
### Thread Safety

In DG implementations of **IMember**, instance members are not guaranteed to be thread safe.

## Remarks
This interface provides properties and methods to manage a member in the ASNA DataGate client. 
It includes properties to get the number of active and deleted records in the member, 
and the extension of the member. It also provides methods to clear the member, 
removing all records, and to initialize the member with a specified number of records.

<br>
<br>

## Properties

| Type | Name | Description
| --- | --- | --- 
| [Int64](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | ActiveRecords | Gets the number of active records in the member. |
| [Int64](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | DeletedRecords | Gets the number of deleted records in the member. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | Extension | Gets or sets the extension of the member. |

## Methods

| Signature | Description |
| --- | --- |
| [Clear()](#void-clear) | Clears the member, removing all records.
| [Initialize](#void-initializeinitmemberoptions-options-long-records)([InitMemberOptions](/reference/datagate/datagate-client/init-member-options.html), [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64)) | Initializes the member with a specified number of records.

### void Clear()

Clears the member, removing all records.

```cs
void Clear()
```

### void Initialize([InitMemberOptions Options](/reference/datagate/datagate-client/init-member-options.html), [long Records](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Initializes the member with a specified number of records.

```cs
void Initialize(InitMemberOptions Options, long Records)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [InitMemberOptions](/reference/datagate/datagate-client/init-member-options.html) | Options | The options to use when initializing the member.
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | Records | The number of records to initialize the member with.
