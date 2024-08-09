---
title: "IServerLicense interface      | QSYS API Reference Guide"
description: "Defines the contract for managing a server license in the ASNA DataGate client. "
last_modified_at: 2024-08-09T17:25:07Z
---

Defines the contract for managing a server license in the ASNA DataGate client.

**Namespace:** ASNA.DataGate.Client
**Assembly:** ASNA.QSys.DataGate.Client.dll

**Extends:** [IDisposable](https://learn.microsoft.com/en-us/dotnet/api/system.idisposable?view=net-8.0)
<br>
<br>

## Remarks
This interface provides properties to manage a server license in the ASNA DataGate client. 
It includes properties to get the source profile, product name, version, machine ID, key code, 
product info, customer, customer company, start date, expiration date, 
whether the license is a site license, whether the license is valid, and the user limit of the license.

<br>
<br>

## Properties

| Type | Name | Description
| --- | --- | --- 
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | Customer | Gets the customer of the server license. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | CustomerCompany | Gets the customer company of the server license. |
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | Expiration | Gets the expiration date of the server license. |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | IsSite | Gets a value indicating whether the server license is a site license. |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | IsValid | Gets a value indicating whether the server license is valid. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | KeyCode | Gets the key code of the server license. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | MachineID | Gets the machine ID of the server license. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | ProductInfo | Gets the product info of the server license. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | ProductName | Gets the product name of the server license. |
| [SourceProfile](/reference/datagate/datagate-providers/source-profile.html) | Source | Gets the source profile of the server license. |
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | Start | Gets the start date of the server license. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | UserLimit | Gets the user limit of the server license. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | Version | Gets the version of the server license. |
