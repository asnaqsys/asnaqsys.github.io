---
title: "JobLogger class               | QSYS API Reference Guide"
description: "Defines the core behavior of a job message logger and provides a base for derived classes. "
last_modified_at: 2024-08-09T17:25:29Z
---

Defines the core behavior of a job message logger and provides a base for derived classes.

**Namespace:** ASNA.QSys.Runtime.JobSupport
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>

## Properties

| Type | Name | Description
| --- | --- | --- 
| [MessageLoggingLevel](/reference/runtime/qsys-runtime-job-support/message-logging-level.html) | LogLevel | Gets the logger's level setting.  |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | MinPriority | Gets the minimum priority needed on a message for it to get logged. |

## Methods

| Signature | Description |
| --- | --- |
| [Add](#void-addmessagebase-entry)([MessageBase](/reference/runtime/qsys-runtime-job-support/message-base.html)) | Adds a message to the log.
| [BeginLogging()](#void-beginlogging) | When overridden in a derived class, logging of messages gets started for the log.
| [EndLogging()](#void-endlogging) | When overridden in a derived class, logging of messages is stopped.
| [Get()](#ijoblogger-get) | Gets the logger.
| [ShouldLog](#bool-shouldlogmessagebase-msg)([MessageBase](/reference/runtime/qsys-runtime-job-support/message-base.html)) | Determines if a message should be added to the log.

### void Add([MessageBase entry](/reference/runtime/qsys-runtime-job-support/message-base.html))

Adds a message to the log.

```cs
void Add(MessageBase entry)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [MessageBase](/reference/runtime/qsys-runtime-job-support/message-base.html) | entry | The message to be logged.

### void BeginLogging()

When overridden in a derived class, logging of messages gets started for the log.

```cs
void BeginLogging()
```

### void EndLogging()

When overridden in a derived class, logging of messages is stopped.

```cs
void EndLogging()
```

### IJobLogger Get()

Gets the logger.

```cs
IJobLogger Get()
```

### bool ShouldLog([MessageBase msg](/reference/runtime/qsys-runtime-job-support/message-base.html))

Determines if a message should be added to the log.

```cs
bool ShouldLog(MessageBase msg)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [MessageBase](/reference/runtime/qsys-runtime-job-support/message-base.html) | msg | Message in question.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | true if the message should be logged; otherwise false.
