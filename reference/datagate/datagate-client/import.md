---
title: "Import class                  | QSYS API Reference Guide"
description: "Provides functionality for importing data into the application. "
last_modified_at: 2024-08-09T16:18:40Z
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
| [With](#task-withimportoptions-options)([ImportOptions](/reference/datagate/datagate-client/import-options.html)) | Initiates an import operation with the specified import options.

### Task With([ImportOptions options](/reference/datagate/datagate-client/import-options.html))

Initiates an import operation with the specified import options.


#### Remarks
This method initiates an import operation with the specified import options.The import operation is performed asynchronously and the method returns a task that represents the operation.The import options specify the target member where the data will be imported, the source path from where the data will be imported, whether the target member should be cleared before the import, whether the target connection should be used for the import, and whether detailed feedback should be provided during the import operation.The method creates a new cancellation token and passes it to the import operation. This cancellation token can be used to cancel the import operation if necessary.

```cs
Task With(ImportOptions options)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [ImportOptions](/reference/datagate/datagate-client/import-options.html) | options | The options for the import operation.

#### Returns

| Type | Description
| --- | ---
| [Task](https://docs.microsoft.com/en-us/dotnet/api/system.threading.tasks.taskscheduler) | A task that represents the asynchronous import operation.
