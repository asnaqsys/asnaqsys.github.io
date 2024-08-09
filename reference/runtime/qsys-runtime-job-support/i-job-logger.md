---
title: "IJobLogger interface          | QSYS API Reference Guide"
description: "Defines a generalized way to to add messages to a log. "
last_modified_at: 2024-08-09T17:25:29Z
---

Defines a generalized way to to add messages to a log.

**Namespace:** ASNA.QSys.Runtime.JobSupport
**Assembly:** ASNA.QSys.Runtime.dll

**Extends:** doesn't extend any other interfaces.
<br>
<br>

## Methods

| Signature | Description |
| --- | --- |
| [Add](#void-addmessagebase-entry)([MessageBase](/reference/runtime/qsys-runtime-job-support/message-base.html)) | Adds a message to the log.

### void Add([MessageBase entry](/reference/runtime/qsys-runtime-job-support/message-base.html))

Adds a message to the log.

```cs
void Add(MessageBase entry)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [MessageBase](/reference/runtime/qsys-runtime-job-support/message-base.html) | entry | The message to be logged.
