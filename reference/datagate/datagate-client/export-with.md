---
title: "Export.With Method"
description: "Starts a new task to export data with the specified options."
---

## Definition

**Namespace:** ASNA.DataGate.Client.CopyData  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Starts a new task to export data with the specified options.

<a id="task-with-exportoptions-options"></a>
## Task With(ExportOptions options)

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

## See Also
- [Export class](export.html)
