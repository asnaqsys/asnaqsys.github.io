---
title: "IFileObject interface.CopyData Method"
description: "Copies data from the file to a new file."
---

## Definition

**Namespace:** ASNA.DataGate.Client  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Copies data from the file to a new file.

<a id="ifileobject-copydata-string-targetdir-string-newname-string-srcmember-string-newmember-copydataoptions-options-int-fromrrn-int-torrn-int-crecords"></a>
## IFileObject CopyData(string targetDir, string newName, string srcMember, string newMember, CopyDataOptions options, int fromRRN, int toRRN, int cRecords)

Copies data from the file to a new file. If this object does not represent a physical file, returns null.

```cs
IFileObject CopyData(string targetDir, string newName, string srcMember, string newMember, CopyDataOptions options, int fromRRN, int toRRN, int cRecords)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | targetDir | The target directory to copy the data to.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | newName | The name of the new file.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | srcMember | The source member to copy from.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | newMember | The new member to copy to.
| [CopyDataOptions](/reference/datagate/datagate-common/copy-data-options.html) | options | The options to use when copying the data.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | fromRRN | The relative record number to start copying from.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | toRRN | The relative record number to stop copying at.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | cRecords | The number of records to copy.

#### Returns

| Type | Description
| --- | ---
| [IFileObject](/reference/datagate/datagate-client/i-file-object.html) | The new file with the copied data, or null if this object does not represent a physical file.

## See Also
- [IFileObject interface class](i-file-object.html)
