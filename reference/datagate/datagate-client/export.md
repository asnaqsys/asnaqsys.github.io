---
title: "Export class                  | QSYS API Reference Guide"
description: "Provides functionality for exporting data to XML or CSV format. This class includes methods for creating tasks to perform the export, logging messages"
last_modified_at: 2024-08-09T17:25:07Z
---

Provides functionality for exporting data to XML or CSV format.
This class includes methods for creating tasks to perform the export, logging messages, writing to a database file, and transforming the data to XML or CSV format.

**Namespace:** ASNA.DataGate.Client.CopyData
**Assembly:** ASNA.QSys.DataGate.Client.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>

## Methods

| Signature | Description |
| --- | --- |
| [With](#task-withexportoptions-options)([ExportOptions](/reference/datagate/datagate-client/export-options.html)) | Starts a new task to export data with the specified options.

### Task With([ExportOptions options](/reference/datagate/datagate-client/export-options.html))

Starts a new task to export data with the specified options.


#### Remarks
This method is used to start a new task to export data with the specified options.The task is started with a default cancellation token, which means the task cannot be canceled.The method calls the overloaded  method with the specified options and the default cancellation token.

```cs
Task With(ExportOptions options)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [ExportOptions](/reference/datagate/datagate-client/export-options.html) | options | The options for the data export.

#### Returns

| Type | Description
| --- | ---
| [Task](https://docs.microsoft.com/en-us/dotnet/api/system.threading.tasks.taskscheduler) | A task that represents the asynchronous data export operation.
