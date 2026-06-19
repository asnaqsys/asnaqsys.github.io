---
title: "Import.With Method"
description: "Initiates an import operation with the specified import options."
---

## Definition

**Namespace:** ASNA.DataGate.Client.CopyData  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Initiates an import operation with the specified import options.

<a id="task-with-importoptions-options"></a>
## Task With(ImportOptions options)

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

## See Also
- [Import class](import.html)
