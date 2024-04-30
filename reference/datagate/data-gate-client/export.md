---
title: Export class
---

Provides methods for exporting data in different formats.

**Namespace:** ASNA.DataGate.Client.CopyData
**Assembly:** ASNA.QSys.DataGate.Client.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>

## Methods

| Signature | Description |
| --- | --- |
| [With](#with-exportoptions-)([ExportOptions](/reference/data-gate-client/export-options.html)) | Starts an export operation with the specified options.
| [With](#with-exportoptions-nullable-)([ExportOptions](/reference/data-gate-client/export-options.html), [Nullable](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/nullable-value-types)) | Executes the export operation with the specified options and cancellation token.
| [With](#with-exportoptions-nullable-taskcreationoptions-)([ExportOptions](/reference/data-gate-client/export-options.html), [Nullable](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/nullable-value-types), [TaskCreationOptions](https://learn.microsoft.com/en-us/dotnet/api/system.threading.tasks.taskcreationoptions?view=net-8.0)) | Starts an export operation with the specified options, cancellation token, and task creation options.

### Task With([ExportOptions options](/reference/data-gate-client/export-options.html))

Starts an export operation with the specified options.

```cs
Task With(ExportOptions options)
```

#### Parameters
| Type | Parameter name | Description
| --- | --- | ---
| [ExportOptions](/reference/data-gate-client/export-options.html) | options | 

#### Returns
| Type | Description
| --- | ---
A task that represents the asynchronous export operation.

| [Task](https://docs.microsoft.com/en-us/dotnet/api/system.threading.tasks.taskscheduler) | A task that represents the asynchronous export operation.

### Task With([ExportOptions options](/reference/data-gate-client/export-options.html))

Executes the export operation with the specified options and cancellation token.

```cs
Task With(ExportOptions options)
```

### Task With([ExportOptions options](/reference/data-gate-client/export-options.html))

Starts an export operation with the specified options, cancellation token, and task creation options.

```cs
Task With(ExportOptions options)
```