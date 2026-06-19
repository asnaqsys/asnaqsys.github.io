---
title: "IAdgObject interface.Duplicate Method"
description: "Duplicates the ADG object."
---

## Definition

**Namespace:** ASNA.DataGate.Client  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Duplicates the ADG object.

<a id="void-duplicate-string-scopepath-string-targetpath-string-newname-duplicateoptions-options"></a>
## void Duplicate(string ScopePath, string TargetPath, string NewName, DuplicateOptions options)

Duplicates the ADG object.

#### Remarks
This method is used to create a duplicate of the ADG object. The ScopePath parameter specifies the path of the object to duplicate. The TargetPath parameter specifies the path where the duplicate object will be placed. The NewName parameter specifies the name for the duplicate object. The options parameter specifies the options for the duplication operation, such as whether to overwrite existing objects.

```cs
void Duplicate(string ScopePath, string TargetPath, string NewName, DuplicateOptions options)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | ScopePath | The scope path of the object to duplicate.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | TargetPath | The target path where the duplicate object will be placed.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | NewName | The new name for the duplicate object.
| [DuplicateOptions](/reference/datagate/datagate-common/duplicate-options.html) | options | The options for the duplication operation.

## See Also
- [IAdgObject interface class](i-adg-object.html)
