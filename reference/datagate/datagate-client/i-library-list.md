---
title: "ILibraryList interface"
description: "Defines the contract for managing a library list in the ASNA DataGate client. "
last_modified_at: 2024-08-09T17:25:07Z
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
| [AddEntry](i-library-list-addentry.html#void-addentry-string-path-liblposition-pos-string-reflib)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [LiblPosition](/reference/datagate/datagate-client/libl-position.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Adds a library to the library list at a specified position.
| [EnumerateCurrentSystem](i-library-list-enumeratecurrentsystem.html#void-enumeratecurrentsystem-adgenumerator-enumerator)([AdgEnumerator](/reference/datagate/datagate-client/adg-enumerator.html)) | Enumerates the current system libraries as IAdgObject instances.
| [EnumerateCurrentUser](i-library-list-enumeratecurrentuser.html#void-enumeratecurrentuser-adgenumerator-enumerator)([AdgEnumerator](/reference/datagate/datagate-client/adg-enumerator.html)) | Enumerates the current user libraries as IAdgObject instances.
| [RemoveEntry](i-library-list-removeentry.html#void-removeentry-string-path)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Removes a library from the user portion of the library list.

