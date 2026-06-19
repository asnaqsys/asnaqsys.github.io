---
title: "IFileObject interface.Copy Method"
description: "Copies the file to a new location with a new name."
---

## Definition

**Namespace:** ASNA.DataGate.Client  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Copies the file to a new location with a new name.

<a id="ifileobject-copy-string-targetdir-string-newname"></a>
## IFileObject Copy(string targetDir, string newName)

Copies the file to a new location with a new name.

```cs
IFileObject Copy(string targetDir, string newName)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | targetDir | The target directory to copy the file to.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | newName | The new name of the file.

#### Returns

| Type | Description
| --- | ---
| [IFileObject](/reference/datagate/datagate-client/i-file-object.html) | The copied file.

## See Also
- [IFileObject interface class](i-file-object.html)
