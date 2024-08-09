---
title: "ILock interface               | QSYS API Reference Guide"
description: "Defines the contract for managing a lock in the ASNA DataGate client. "
last_modified_at: 2024-08-09T16:18:40Z
---

Defines the contract for managing a lock in the ASNA DataGate client.

**Namespace:** ASNA.DataGate.Client
**Assembly:** ASNA.QSys.DataGate.Client.dll

**Extends:** doesn't extend any other interfaces.
<br>
<br>

## Remarks
This interface provides properties to manage a lock in the ASNA DataGate client. 
It includes properties to get the path of the locked object, the number of valid fields in the locked object, 
the ID, type, and subtype of the locked object, whether the lock is waiting, 
and the number of various types of locks on the object.

<br>
<br>

## Properties

| Type | Name | Description
| --- | --- | --- 
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | Exlusive | Gets the number of exclusive locks on the object. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | ExlusiveRead | Gets the number of exclusive read locks on the object. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | ObjectID | Gets the ID of the locked object. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | Path | Gets the path of the locked object. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | ShareNoUpdate | Gets the number of shared no-update locks on the object. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | ShareRead | Gets the number of shared read locks on the object. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | ShareUpdate | Gets the number of shared update locks on the object. |
| [AdgSubTypes](/reference/datagate/datagate-common/adg-sub-types.html) | SubType | Gets the subtype of the locked object. |
| [AdgObjectTypes](/reference/datagate/datagate-common/adg-object-types.html) | Type | Gets the type of the locked object. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | ValidFields | Gets the number of valid fields in the locked object. |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | Waiting | Gets a value indicating whether the lock is waiting. |
