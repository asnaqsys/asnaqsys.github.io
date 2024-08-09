---
title: "IOpenFile interface           | QSYS API Reference Guide"
description: "Defines the contract for managing an open file in the ASNA DataGate client. "
last_modified_at: 2024-08-09T17:25:07Z
---

Defines the contract for managing an open file in the ASNA DataGate client.

**Namespace:** ASNA.DataGate.Client
**Assembly:** ASNA.QSys.DataGate.Client.dll

**Extends:** doesn't extend any other interfaces.
<br>
<br>

## Remarks
This interface provides properties to manage an open file in the ASNA DataGate client. 
It includes properties to get the path of the open file, the number of valid fields in the open file, 
the ID, status, access mode, and share type of the open file, 
the number of I/O operations performed on the open file, and the relative record number (RRN) of the open file.

<br>
<br>

## Properties

| Type | Name | Description
| --- | --- | --- 
| [AccessMode](/reference/datagate/datagate-common/access-mode.html) | AccessMode | Gets the access mode of the open file. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | IOCount | Gets the number of I/O operations performed on the open file. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | ObjectID | Gets the ID of the open file. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | Path | Gets the path of the open file. |
| [Int64](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | RRN | Gets the relative record number (RRN) of the open file. |
| [ShareTypes](/reference/datagate/datagate-common/share-types.html) | ShareType | Gets the share type of the open file. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | Status | Gets the status of the open file. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | ValidFields | Gets the number of valid fields in the open file. |
