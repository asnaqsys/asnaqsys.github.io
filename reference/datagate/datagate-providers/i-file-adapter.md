---
title: "IFileAdapter interface        | QSYS API Reference Guide"
description: "Provides an interface for file operations. "
last_modified_at: 2024-08-08T21:41:32Z
---

Provides an interface for file operations.

**Namespace:** ASNA.DataGate.Providers
**Assembly:** ASNA.QSys.DataGate.Client.dll

**Extends:** doesn't extend any other interfaces.
<br>
<br>

## Properties

| Type | Name | Description
| --- | --- | --- 
| [AccessMode](/reference/datagate/datagate-common/access-mode.html) | AccessMode | Gets or sets the access mode for the file. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | FileName | Gets or sets the name of the file. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | MemberName | Gets or sets the name of the member. |
| [FileOpenAttr](/reference/datagate/datagate-providers/file-open-attr.html) | OpenAttributes | Gets or sets the attributes for opening the file. |

## Methods

| Signature | Description |
| --- | --- |
| [Open](#void-openadgdataset-ds)([AdgDataSet](/reference/datagate/datagate-client/adg-data-set.html)) | Opens the file with the specified dataset.
| [ReadSequentialEqual](#void-readsequentialequaladgdataset-ds-readsequentialmode-rm-lockrequest-lr)([AdgDataSet](/reference/datagate/datagate-client/adg-data-set.html), [ReadSequentialMode](/reference/datagate/datagate-common/read-sequential-mode.html), [LockRequest](/reference/datagate/datagate-common/lock-request.html)) | Reads the file sequentially with the specified dataset, read mode, and lock request.

### void Open([AdgDataSet ds](/reference/datagate/datagate-client/adg-data-set.html))

Opens the file with the specified dataset.

```cs
void Open(AdgDataSet ds)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [AdgDataSet](/reference/datagate/datagate-client/adg-data-set.html) | ds | The dataset to use when opening the file.

### void ReadSequentialEqual([AdgDataSet ds](/reference/datagate/datagate-client/adg-data-set.html), [ReadSequentialMode rm](/reference/datagate/datagate-common/read-sequential-mode.html), [LockRequest lr](/reference/datagate/datagate-common/lock-request.html))

Reads the file sequentially with the specified dataset, read mode, and lock request.

```cs
void ReadSequentialEqual(AdgDataSet ds, ReadSequentialMode rm, LockRequest lr)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [AdgDataSet](/reference/datagate/datagate-client/adg-data-set.html) | ds | The dataset to use when reading the file.
| [ReadSequentialMode](/reference/datagate/datagate-common/read-sequential-mode.html) | rm | The read mode to use when reading the file.
| [LockRequest](/reference/datagate/datagate-common/lock-request.html) | lr | The lock request to use when reading the file.
