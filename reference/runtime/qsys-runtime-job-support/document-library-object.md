---
title: "DocumentLibraryObject class   | QSYS API Reference Guide"
description: "Provides functionality to manipulate Document Library Objects (DLO). "
last_modified_at: 2024-08-09T17:25:29Z
---

Provides functionality to manipulate Document Library Objects (DLO).

**Namespace:** ASNA.QSys.Runtime.JobSupport
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [DocumentLibraryObject](#documentlibraryobjectstring)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Initializes a new instance of the DocumentLibraryObject class.

### DocumentLibraryObject([String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Initializes a new instance of the DocumentLibraryObject class.

```cs
DocumentLibraryObject(String)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | dlsRootName | The name of the folder, within the Job's IFS Root, serving as the root of the DLS objects.

## Properties

| Type | Name | Description
| --- | --- | --- 
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | IFSRoot | Gets the Current Job IFS root path. |

## Methods

| Signature | Description |
| --- | --- |
| [Check](#void-checkstring-dloname-string-parentfolder-dlotype-objecttype)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [DLOType](/reference/runtime/qsys-runtime-job-support/dlo-type.html)) | Checks that an object exists in the DLO Root, if the object does not exists it throws a CPF exception.
| [CreateFolder](#void-createfolderstring-newfolder-string-parentfolder)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Creates a Folder in another folder within the DLO Root.
| [GetDLORoot()](#string-getdloroot) | Gets the absolute DLO folder path.
| [Move](#void-movestring-docname-string-fromfolder-string-tofolder-string-newname)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Move a document to a new folder and can rename the document in the process.
| [Rename](#void-renamestring-dloname-string-newname-string-parentfolder)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Changes the name of a document or folder.

### void Check([string dloName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string parentFolder](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [DLOType objectType](/reference/runtime/qsys-runtime-job-support/dlo-type.html))

Checks that an object exists in the DLO Root, if the object does not exists it throws a CPF exception.

```cs
void Check(string dloName, string parentFolder, DLOType objectType)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | dloName | Object Name to look for.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | parentFolder | Containing object's parent folder.
| [DLOType](/reference/runtime/qsys-runtime-job-support/dlo-type.html) | objectType | Type of object to look for.

### void CreateFolder([string newFolder](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string parentFolder](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Creates a Folder in another folder within the DLO Root.

```cs
void CreateFolder(string newFolder, string parentFolder)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | newFolder | Name of new folder to create.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | parentFolder | Parent Folder of new folder.

### string GetDLORoot()

Gets the absolute DLO folder path.

```cs
string GetDLORoot()
```

### void Move([string docName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string fromFolder](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string toFolder](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string newName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Move a document to a new folder and can rename the document in the process.

```cs
void Move(string docName, string fromFolder, string toFolder, string newName)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | docName | Name of Document to be moved.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | fromFolder | Current Document's parent folder. Use *NONE for DLO root folder.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | toFolder | New Folder to contain Document. Use *NONE for DLO root folder.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | newName | New Document Name. Use *SAME to keep original Name of Document.

### void Rename([string dloName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string newName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string parentFolder](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Changes the name of a document or folder.

```cs
void Rename(string dloName, string newName, string parentFolder)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | dloName | Original Document Name.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | newName | New Document Name.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | parentFolder | Document's containing folder.
