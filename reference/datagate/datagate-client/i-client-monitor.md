---
title: "IClientMonitor interface      | QSYS API Reference Guide"
description: "Defines the contract for monitoring a client in the ASNA DataGate client. "
last_modified_at: 2024-08-09T17:25:07Z
---

Defines the contract for monitoring a client in the ASNA DataGate client.

**Namespace:** ASNA.DataGate.Client
**Assembly:** ASNA.QSys.DataGate.Client.dll

**Extends:** [IDisposable](https://learn.microsoft.com/en-us/dotnet/api/system.idisposable?view=net-8.0)
<br>
<br>

## Remarks
This interface provides properties and methods to monitor a client in the ASNA DataGate client. 
It includes properties to get the client's application name, current function, status, start time, 
process name, user name, job name, server user name, client number, current locks, library list, 
and current open files. It also provides a method to forcibly terminate the client.

<br>
<br>

## Properties

| Type | Name | Description
| --- | --- | --- 
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | Application | Gets the name of the application using this client. |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | CacheData | Gets or sets a value indicating whether data should be cached. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | CurrentFunction | Gets the name of the function at the current time. |
| [IEnumerable\<ILock\>](https://learn.microsoft.com/en-us/dotnet/api/system.collections.generic.ienumerable-1?view=net-8.0) | CurrentLocks | Gets all locks created by this client. |
| [IEnumerable\<IOpenFile\>](https://learn.microsoft.com/en-us/dotnet/api/system.collections.generic.ienumerable-1?view=net-8.0) | CurrentOpenFiles | Gets all files opened by this client. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | Job | Gets the job associated with this client. |
| [ILibraryList](/reference/datagate/datagate-client/i-library-list.html) | LibraryList | Gets the Library List in use by the client. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | Number | Gets the number associated with this client. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | Process | Gets the process running this client. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | ServerUser | Gets the server user associated with this client. |
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | Started | Gets the DateTime when the client started. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | Status | Gets the status of the client. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | User | Gets the user name associated with this client. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | ValidFields | Gets the number of valid fields in the client. |

## Methods

| Signature | Description |
| --- | --- |
| [Kill](#void-killint-delay)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Forcibly terminates the current client.

### void Kill([int delay](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Forcibly terminates the current client.


#### Remarks
This method will forcibly terminate the client after the specified delay. Use this method with caution as it can lead to data loss if the client is in the middle of a transaction.

```cs
void Kill(int delay)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | delay | Wait time in milliseconds before terminating the client.
