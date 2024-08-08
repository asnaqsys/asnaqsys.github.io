---
title: "ILibraryList interface        | QSYS API Reference Guide"
description: "Defines the contract for managing a library list in the ASNA DataGate client. "
last_modified_at: 2024-08-08T21:41:32Z
---

Defines the contract for managing a library list in the ASNA DataGate client.

**Namespace:** ASNA.DataGate.Client
**Assembly:** ASNA.QSys.DataGate.Client.dll

**Extends:** [IDisposable](https://learn.microsoft.com/en-us/dotnet/api/system.idisposable?view=net-8.0)
<br>
<br>
## Thread Safety

In DG implementations of **ILibraryList** , instance members are not guaranteed to be thread safe.

## Remarks
This interface provides properties and methods to manage a library list in the ASNA DataGate client. 
It includes properties to get and set the current system and user libraries as pathnames, 
and the system and user libraries configuration as pathnames. It also provides methods to enumerate 
the current system and user libraries as IAdgObject instances, and to add and remove libraries from the library list.

<br>
<br>

## Properties

| Type | Name | Description
| --- | --- | --- 
| [IEnumerable\<String\>](https://learn.microsoft.com/en-us/dotnet/api/system.collections.generic.ienumerable-1?view=net-8.0) | CurrentSystemLibraries | Gets the current system libraries as pathnames. |
| [IEnumerable\<String\>](https://learn.microsoft.com/en-us/dotnet/api/system.collections.generic.ienumerable-1?view=net-8.0) | CurrentUserLibraries | Gets or sets the current user libraries as pathnames. |
| [IEnumerable\<String\>](https://learn.microsoft.com/en-us/dotnet/api/system.collections.generic.ienumerable-1?view=net-8.0) | SystemLibrariesConfig | Gets or sets the system libraries configuration as pathnames. |
| [IEnumerable\<String\>](https://learn.microsoft.com/en-us/dotnet/api/system.collections.generic.ienumerable-1?view=net-8.0) | UserLibrariesConfig | Gets or sets the user libraries configuration as pathnames. |

## Methods

| Signature | Description |
| --- | --- |
| [AddEntry](#void-addentrystring-path-liblposition-pos-string-reflib)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [LiblPosition](/reference/datagate/datagate-client/libl-position.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Adds a library to the library list at a specified position.
| [EnumerateCurrentSystem](#void-enumeratecurrentsystemadgenumerator-enumerator)([AdgEnumerator](/reference/datagate/datagate-client/adg-enumerator.html)) | Enumerates the current system libraries as IAdgObject instances.
| [EnumerateCurrentUser](#void-enumeratecurrentuseradgenumerator-enumerator)([AdgEnumerator](/reference/datagate/datagate-client/adg-enumerator.html)) | Enumerates the current user libraries as IAdgObject instances.
| [RemoveEntry](#void-removeentrystring-path)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Removes a library from the user portion of the library list.

### void AddEntry([string path](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [LiblPosition pos](/reference/datagate/datagate-client/libl-position.html), [string refLib](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Adds a library to the library list at a specified position.

```cs
void AddEntry(string path, LiblPosition pos, string refLib)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | path | The path of the library to add.
| [LiblPosition](/reference/datagate/datagate-client/libl-position.html) | pos | The position to add the library at.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | refLib | Optional reference library.

### void EnumerateCurrentSystem([AdgEnumerator enumerator](/reference/datagate/datagate-client/adg-enumerator.html))

Enumerates the current system libraries as IAdgObject instances.

```cs
void EnumerateCurrentSystem(AdgEnumerator enumerator)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [AdgEnumerator](/reference/datagate/datagate-client/adg-enumerator.html) | enumerator | The enumerator to use.

### void EnumerateCurrentUser([AdgEnumerator enumerator](/reference/datagate/datagate-client/adg-enumerator.html))

Enumerates the current user libraries as IAdgObject instances.

```cs
void EnumerateCurrentUser(AdgEnumerator enumerator)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [AdgEnumerator](/reference/datagate/datagate-client/adg-enumerator.html) | enumerator | The enumerator to use.

### void RemoveEntry([string path](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Removes a library from the user portion of the library list.

```cs
void RemoveEntry(string path)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | path | The path of the library to remove.
