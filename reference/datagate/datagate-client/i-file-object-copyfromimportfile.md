---
title: "IFileObject interface.CopyFromImportFile Method"
description: "Copies data from an import file to the file."
---

## Definition

**Namespace:** ASNA.DataGate.Client  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Copies data from an import file to the file.

<a id="ifileobject-copyfromimportfile-string-filepath-copyfromimportfileoptions-options"></a>
## IFileObject CopyFromImportFile(string filePath, CopyFromImportFileOptions options)

Copies data from an import file to the file.

```cs
IFileObject CopyFromImportFile(string filePath, CopyFromImportFileOptions options)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | filePath | The path of the import file.
| [CopyFromImportFileOptions](/reference/datagate/datagate-client/copy-from-import-file-options.html) | options | The options to use when copying the data.

#### Returns

| Type | Description
| --- | ---
| [IFileObject](/reference/datagate/datagate-client/i-file-object.html) | The file with the copied data.

## See Also
- [IFileObject interface class](i-file-object.html)
