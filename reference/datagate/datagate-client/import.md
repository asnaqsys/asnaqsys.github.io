---
title: "Import class"
description: "Provides functionality for importing data into the application. "
last_modified_at: 2024-08-09T17:25:07Z
---

Provides functionality for importing data into the application.

**Namespace:** ASNA.DataGate.Client.CopyData
**Assembly:** ASNA.QSys.DataGate.Client.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>

## Remarks
The Import class provides methods for importing data from various formats such as XML and CSV.
It uses the ImportOptions class to specify options for the import operation, such as the target member where the data will be imported, the source path from where the data will be imported, whether the target member should be cleared before the import, whether the target connection should be used for the import, and whether detailed feedback should be provided during the import operation.
The class also provides methods for validating the import options and for performing the actual import operation.

<br>
<br>

## Methods

| Signature | Description |
| --- | --- |
| [With](import-with.html#task-with-importoptions-options)([ImportOptions](/reference/datagate/datagate-client/import-options.html)) | Initiates an import operation with the specified import options.

