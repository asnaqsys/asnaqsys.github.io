---
title: "IDirectory interface          | QSYS API Reference Guide"
description: "Defines the contract for managing a directory in the ASNA DataGate client. "
last_modified_at: 2024-08-08T21:41:32Z
---

Defines the contract for managing a directory in the ASNA DataGate client.

**Namespace:** ASNA.DataGate.Client
**Assembly:** ASNA.QSys.DataGate.Client.dll

**Extends:** [IAdgObject](/reference/datagate/datagate-client/i-adg-object.html), [IComparable](https://learn.microsoft.com/en-us/dotnet/api/system.icomparable-1?view=net-8.0), [IConnectionHandler](/reference/datagate/datagate-client/i-connection-handler.html), [IDisposable](https://learn.microsoft.com/en-us/dotnet/api/system.idisposable?view=net-8.0)
<br>
<br>
In DG implementations of **IDirectory** , instance members are not guaranteed to be thread safe.

## Remarks
This interface provides properties and methods to manage a directory in the ASNA DataGate client. 
It includes properties to get the list of items in the directory, the remote path name of the directory, 
and the enumerator for the directory. It also provides methods to attach a remote directory, 
create a subdirectory, enumerate the items in the directory, repair the objects in the directory, 
and enumerate the items in the directory using specified file types.

<br>
<br>

## Properties

| Type | Name | Description
| --- | --- | --- 
| [IEnumerable](https://learn.microsoft.com/en-us/dotnet/api/system.collections.generic.ienumerable-1?view=net-8.0) | Enumerator | Gets the enumerator for the directory. |
| [ArrayList](https://learn.microsoft.com/en-us/dotnet/api/system.collections.arraylist?view=net-8.0) | ItemList | Gets the list of items in the directory. This property is obsolete, use 'Items' instead. |
| [List\<IAdgObject\>](https://docs.microsoft.com/en-us/dotnet/api/system.collections.generic.list-1) | Items | Gets the list of items in the directory. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | RemotePathName | Gets the remote path name of the directory. |

## Methods

| Signature | Description |
| --- | --- |
| [AttachRemoteDirectory](#void-attachremotedirectorystring-remotepathname)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Attaches a remote directory to the current directory.
| [CreateSubDirectory](#idirectory-createsubdirectorystring-name)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Creates a subdirectory in the current directory.
| [Enumerate](#void-enumerateadgenumerator-enumerator)([AdgEnumerator](/reference/datagate/datagate-client/adg-enumerator.html)) | Enumerates the items in the directory using the specified enumerator.
| [Enumerate](#void-enumerateadgenumerator-enumerator-filetypes-ftype-bool-sysobjs)([AdgEnumerator](/reference/datagate/datagate-client/adg-enumerator.html), [FileTypes](/reference/datagate/datagate-common/file-types.html), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Enumerates the items in the directory using the specified enumerator and file types.
| [RepairObjects](#void-repairobjectsrepairoptions-repairoptions-adgobserver-observer)([RepairOptions](/reference/datagate/datagate-common/repair-options.html), [AdgObserver](/reference/datagate/datagate-client/adg-observer.html)) | Repairs the objects in the directory using the specified repair options and observer.

### void AttachRemoteDirectory([string remotePathName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Attaches a remote directory to the current directory.

```cs
void AttachRemoteDirectory(string remotePathName)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | remotePathName | The path name of the remote directory to attach.

### IDirectory CreateSubDirectory([string Name](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Creates a subdirectory in the current directory.

```cs
IDirectory CreateSubDirectory(string Name)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | Name | The name of the subdirectory to create.

#### Returns

| Type | Description
| --- | ---
| [IDirectory](/reference/datagate/datagate-client/i-directory.html) | The created subdirectory.

### void Enumerate([AdgEnumerator enumerator](/reference/datagate/datagate-client/adg-enumerator.html))

Enumerates the items in the directory using the specified enumerator.

```cs
void Enumerate(AdgEnumerator enumerator)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [AdgEnumerator](/reference/datagate/datagate-client/adg-enumerator.html) | enumerator | The enumerator to use.

### void Enumerate([AdgEnumerator enumerator](/reference/datagate/datagate-client/adg-enumerator.html), [FileTypes fType](/reference/datagate/datagate-common/file-types.html), [bool sysObjs](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Enumerates the items in the directory using the specified enumerator and file types.

```cs
void Enumerate(AdgEnumerator enumerator, FileTypes fType, bool sysObjs)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [AdgEnumerator](/reference/datagate/datagate-client/adg-enumerator.html) | enumerator | The enumerator to use.
| [FileTypes](/reference/datagate/datagate-common/file-types.html) | fType | The file types to enumerate.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | sysObjs | Whether to include system objects in the enumeration.

### void RepairObjects([RepairOptions repairOptions](/reference/datagate/datagate-common/repair-options.html), [AdgObserver observer](/reference/datagate/datagate-client/adg-observer.html))

Repairs the objects in the directory using the specified repair options and observer.

```cs
void RepairObjects(RepairOptions repairOptions, AdgObserver observer)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [RepairOptions](/reference/datagate/datagate-common/repair-options.html) | repairOptions | The repair options to use.
| [AdgObserver](/reference/datagate/datagate-client/adg-observer.html) | observer | The observer to use.
