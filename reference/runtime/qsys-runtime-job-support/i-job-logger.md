---
title: IJobLogger interface
description: Defines a generalized way to to add messages to a log.

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
