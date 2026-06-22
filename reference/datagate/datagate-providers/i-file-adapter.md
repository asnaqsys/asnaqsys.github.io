---
title: "IFileAdapter interface"
description: "Provides an interface for file operations. "
last_modified_at: 2024-08-09T17:25:07Z
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
| [Open](i-file-adapter-open.html#void-open-adgdataset-ds)([AdgDataSet](/reference/datagate/datagate-client/adg-data-set.html)) | Opens the file with the specified dataset.
| [ReadSequentialEqual](i-file-adapter-readsequentialequal.html#void-readsequentialequal-adgdataset-ds-readsequentialmode-rm-lockrequest-lr)([AdgDataSet](/reference/datagate/datagate-client/adg-data-set.html), [ReadSequentialMode](/reference/datagate/datagate-common/read-sequential-mode.html), [LockRequest](/reference/datagate/datagate-common/lock-request.html)) | Reads the file sequentially with the specified dataset, read mode, and lock request.

