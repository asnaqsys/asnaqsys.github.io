---
title: "IntegratedFileSystem class    | QSYS API Reference Guide"
description: "Holds the Integrated File System (IFS) root folder. "
last_modified_at: 2024-08-09T16:18:25Z
---

Holds the Integrated File System (IFS) root folder.

**Namespace:** ASNA.QSys.Runtime.JobSupport
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [IntegratedFileSystem](#integratedfilesystemstring)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Initializes a new instance of the IntergratedFileSystem class for the specified root folder.

### IntegratedFileSystem([String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Initializes a new instance of the IntergratedFileSystem class for the specified root folder.

```cs
IntegratedFileSystem(String)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | ifsRootPath | The path to the system folder that serves as the root directory for IFS operations. The path is typically an absolute path.

## Properties

| Type | Name | Description
| --- | --- | --- 
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | IFSRootPath | Gets the path to the system folder that serves as the root directory for IFS operations. |
